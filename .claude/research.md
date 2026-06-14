# Research

## Glyphs for non-Unicode radical forms

Some radical forms (particularly variants) may not have a Unicode code point. For generating glyph images of these forms, one avenue to explore is non-Unicode CJK character sets that predate or diverge from Unicode's Han unification, such as:

- CNS character set
- CCCII character set
- TRON
- Mojikyō
- ISO/IEC 2022
- Big5 extensions
- GCCS / HKSCS (Hong Kong)

If a form exists in one of these encodings and a corresponding font exists, that font could be used to render and capture the glyph.

However, the forms in question are often component-only — they function as parts of characters but are not used as standalone characters. General-purpose character sets would not normally include these. They would only appear in a character set that was specifically designed with component-level encoding in mind (e.g. for input methods or character decomposition purposes).

The Outlier dataset contains renderings of such component forms as SVG images, which proves it is possible. Two possible explanations for how these SVGs were produced:

1. **Font-based**: the component exists in some encoding and font, and the glyph was rendered and captured as SVG
2. **Hand-drawn**: the SVG was drawn manually, or derived by editing an existing character SVG (e.g. isolating the component from a full character SVG)
