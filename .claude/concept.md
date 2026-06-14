# Origami (Kanji Radicals Dataset) — Concept Doc

## Goal

Assemble a unified and canonical dataset of kanji radicals, covering the most important radical systems (Kangxi, Hadamitzky, and Classic Nelson). For each radical in each system, the dataset enumerates:

- the standard form and all variant forms
- for each form, all Unicode code points that represent that form (where available)

---

## Context

This dataset is consumed by Shiro, which enriches it uniformly (e.g. Unicode metadata such as block/plane, image derivations like SVG → bitmap, and indexing).

Design goal: Origami contains only irreducible knowledge about radicals; all derivable data is handled by Shiro.

---

## Radical Systems

The following three radical systems are covered:

- Kangxi
- Hadamitzky
- Nelson

> Note that the Nelson radical system here refers to the "classic" Nelson radical system with the Radical Priority System introduced in "The Modern Reader's Japanese-English Character Dictionary" from 1962.

---

## Core Model

```
Radical Layer  →  Form Layer  ←  Unicode Layer
```

### Radical Layer

- Contains radical systems (e.g. Kangxi, Hadamitzky)
- Each radical entry represents one radical in a given system
- Each radical has:
  - one main form
  - zero or more variant forms
- Each referenced form (main or variant) points to exactly one form entry in the form layer
- Radical systems are independent; relationships between systems are implicit via shared forms

### Form Layer

- Central pivot of the model
- Contains canonical visual identities of radicals
- Each form consists of:
  - a stable, opaque identifier
  - an SVG depiction of the form
- Each form represents exactly one distinct visual shape (no duplicates)
- Forms may or may not have a Unicode representation

### Unicode Layer

- Contains Unicode code points mapped to forms
- Each entry consists of:
    - a Unicode code point (hex value)
    - a reference to a form
- Each Unicode code point maps to exactly one form
- Multiple Unicode code points may map to the same form (implicit isomorphs)
- The mapping from Unicode code points to forms is curated and manually determined
    - Unicode itself does not define forms
    - The mapping is based on observed glyph shapes in reference material (e.g. dictionaries) and common font renderings

---

## Data Structure Example

`forms/index.json`:

```json
[
  { "id": "f001" },
  { "id": "f002" }
]
```

`forms/fXXX.svg`:

```svg
<svg xmlns="http://w3.org" width="100" height="100"></svg>
```

`unicode/index.json`:

```json
[
  { "code": "4eba", "form": "f001" },
  { "code": "2f08", "form": "f001" },
  { "code": "2f09", "form": "f002" }
]
```

`radicals/kangxi.json`:

```json
[
  {
    "id": "9",
    "form_standard": "f001",
    "form_variants": ["f002"]
  }
]
```

`radicals/hadamitzky.json`:

```json
[
  {
    "id": "1a",
    "form_standard": "f002",
    "form_variants": []
  }
]
```

`radicals/nelson.json`:

```json
[
  {
    "id": "22",
    "form_standard": "f002",
    "form_variants": []
  }
]
```

**Notes:**

- All JSON files should have a corresponding JSON Schema.
- Whether the SVG representations in the `forms/` directory are needed or not is not yet clear (see [Open Questions](#open-questions)).

---

## Open Questions

- Unicode coverage: are all radicals including their variants in the covered radical systems represented in Unicode?
  - What defines "all" (some similar shapes may or may not be regarded as the same form)? Probably requires defining a canonical source (radical table) for each radical system and take this as the ground truth for this radical system.
  - This canonical source should likely be the original printed book where the radical system was introduced (authoritative and unambiguous)
  - Thus, this is a manual process, going through the canonical radical tables adn comparing the forms with the relevant Unicode code blocks
    - Consider building semi-automation around it (e.g. a loop showing a photo screenshot of the next character, prompt for the Unicode mapping, verification and confirmation, and insertion into data set)
    - This could actually be the first (or main) step in building the data set
- Unicode coverage follow up: result of the *Unicode coverage* question defines whether SVG representations are needed at all or not in the data
  - If Unicode coverage complete, no need for SVG representations as any radical can be rendered by any font
  - If Unicode coverage not complete, two new questions arise:
    1. How to obtain SVG representations of radicals that are not covered by Unicode (pre-rendered files, non-Unicode font that allows rendering them - investigate where tools like the Outlier Kanji Dictionary get their SVG representations of non-Unicode characters from)?
    2. How to generate the SVG representations of those radicals that are covered by Unicode (extraction, tooling, font, etc.)?
- Form and position: should the position of a radical within a kanji (e.g. left, right, top, bottom) be part of the form?
  - For example, ⻖ (U+2ED6) usually appears as the left side of a kanji and ⻏ (U+2ECF) appears on the right side, but the strokes themselves have the same shape. So, should these map to two different shapes or to the same shape? In the New Nelson they are depicted as two different forms that are either on the left or right side of the bounding box. Hadamitzky seems to use only the left version (⻖ U+2ED6). Both radical variants have representations in Unicode (⻖ U+2ED6 and ⻏ U+2ECF), however, they both look exactly the same and the shape is horizontally centred in the bounding box, not either left or right (at least in the current font they are rendered with).
