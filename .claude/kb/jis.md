# JIS (Japanese Industrial Standards)

## What it is

- Japan's national standards body; international equivalents include ISO (international), ANSI (USA), DIN (Germany)
- Coordinated by the Japanese Industrial Standards Committee (JISC) and published by the Japanese Standards Association (JSA)
- JIS X is the information processing subdivision
- Standards named as "JIS X NNNN:YYYY" (number + revision year)

## History

- Precursor standards body established in 1921
- Current form established after 1946, following Japan's defeat in World War II
- Industrial Standardization Law enacted in 1949, forming the legal foundation for JIS

## Character Sets

- **JIS X 0201** (1969) — Japan's national variant of ISO 646; covers basic Latin and half-width katakana
- **JIS X 0208** (1978, revised 1983/1990/1997) — primary Japanese character set; 6,355 kanji plus kana, Roman letters, and symbols; basis for KANJIDIC
- **JIS X 0212** (1990) — supplementary character set; 5,801 additional kanji not in JIS X 0208; basis for KRADFILE2/RADKFILE2
- **JIS X 0213** (2000, revised 2004) — extension of JIS X 0208; adds further characters, making JIS X 0212 largely redundant; covered by KANJIDIC2
- Code points expressed as row-cell (kuten) codes
- TODO: do the JIS X character sets include radical characters?

### Relation with Unicode and ISO

- JIS character sets predate Unicode; the kanji in JIS X 0208, 0212, and 0213 were incorporated into Unicode's CJK Unified Ideographs block through the Han Unification process
- JIS X 0221 is Japan's formal adoption of ISO 10646 (the Unicode-equivalent international standard), representing JIS's convergence with Unicode
- The old JIS character sets remain relevant as reference systems (e.g. KANJIDIC organises kanji by JIS set membership) but are no longer used for new software development
