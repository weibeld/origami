# CLAUDE.md — Origami

## Project

Origami (formerly codenamed Nara) assembles a unified, canonical dataset of kanji radicals covering the Kangxi, Hadamitzky, and Classic Nelson radical systems (see `.claude/concept.md` for the full concept and data model).

## Working files in `.claude/`

- **`research.md`** — Origami-specific research (e.g. how to obtain glyphs for non-Unicode radical forms). Not destined for the knowledge base.
- **`knowledge.md`** — general (non-Origami-specific) research. Content here is being progressively migrated into `kb/` as standalone knowledge-base entries, with migrated content deleted from this file once moved.
- **`kb/`** — provisional mini knowledge base: one file per concept/topic, each self-contained (no internal cross-links between entries, since retrieval will be RAG-based; external source URLs are kept). Eventually to be moved into a real, standalone knowledge base project (codename Owl).
- **`kb/sources/`** — planned but not yet created: local archived copies (HTML, PDF, etc.) of sources used in `kb/` entries, fetched e.g. via `wget` (TODO: what are knowledge base best practices regarding sources?)
- **`tmp/`** — scratch files (pasted source texts, PDFs) used while researching.

## Current task

Moving content from `knowledge.md` to separate files in `kb/`.

> The information in `kb/` is eventually to be moved to an general external knowledge base (possibly project Owl).

### Conventions for `kb/` entries

- One file per concept; group closely related concepts in one file where they form a natural unit
- No internal cross-links between `kb/` files; keep external source URLs
- For standards-related entries (JIS, Unicode, ISO, ANSI): `## What it is` → `## History` (include founding year) → `## Character Sets and Encodings` (with `### Relation with Unicode and ISO` subsection where applicable)
- Always delete content from `knowledge.md` once it has been moved to a `kb/` file
