# KANJIDIC2

## What it is

- A machine-readable database of information on Japanese kanji, maintained by the Electronic Dictionary Research and Development Group (EDRDG)
- Covers 13,108 characters across three JIS standards: JIS X 0208-1998 (6,355 kanji), JIS X 0212-1990 (5,801 additional kanji), and JIS X 0213-2012 (952 further extra characters)
- Distributed as three files:
  - **KANJIDIC2** — XML format, UTF-8, covers all 13,108 characters (successor to KANJIDIC and KANJD212)
  - **KANJIDIC** — original flat-file format, EUC-JP, covers the JIS X 0208 characters
  - **KANJD212** — same flat-file format as KANJIDIC, EUC-JP, covers the JIS X 0212 characters
- For each character, the data includes (depending on availability): on/kun/pinyin/Korean/nanori readings, English (and some Spanish/French) meanings, radical numbers (classic/Nelson and Kangxi), stroke counts, grade level, frequency ranking, JLPT level, variant ("itaiji") cross-references, and a large set of dictionary index codes (SKIP, Four Corner, De Roo, Spahn & Hadamitzky, Heisig, Gakken, O'Neill, Henshall, Morohashi, New Nelson, and others)

## History and Data Provenance

KANJIDIC began in 1991 as two flat EUC-JP files compiled by Jim Breen from Stephen Chung's `kinfo.dat`, with initial English meanings keyed in from James Heisig's *Remembering The Kanji*. Over the following years, an internationally distributed group of volunteers incrementally added new reading sets, dictionary index codes, and made systematic corrections to radicals, stroke counts, and variant cross-references. The data has continued to be maintained and extended since, eventually converging on the current XML-based KANJIDIC2 format.

As a result, KANJIDIC2's data fields were assembled over time from a wide range of individually contributed sources — published dictionaries, personal compilations, and volunteer keying/correction work — rather than from a single authoritative database. The following breaks this down by data category.

### Japanese readings (on, kun)

- Initial data (1991) came from Stephen Chung's `kinfo.dat` (derived from a file by Mike Erickson) and from Rik Smoody's files (compiled while working for Sony in Japan, apparently themselves based on Nelson's dictionary)
- Theresa Martin contributed extensive early corrections, particularly tracking down and fixing systematically mistranscribed readings (recurring issues like zu/dzu, oo/ou, ji/dji)
- April 1996: all readings were checked against the JIS X 0208 draft, with corrections and additions made
- May 1996: the readings in KANJIDIC and KANJD212 were "unified"
- August 1996: Wolfgang Cronrath flagged the kokuji among the kanji, which were then marked in the readings field with the notation `{(kokuji)}`

### Dictionary index codes

- **SKIP codes**: added 1992 by Jeffrey Friedl; withdrawn mid-1993 over copyright, reinstated 1994 after Jack Halpern secured publisher permission; extended in May 1995 with codes for kanji not covered in the *New Japanese-English Character Dictionary*
- **Halpern (NJECD) numbers**: added 1992 by Jeffrey Friedl, corrected by Magnus Halldorsson, verified against Halpern's own files in 1995
- **Spahn & Hadamitzky (S&H) descriptors**: missing descriptors supplied by Mark Spahn (May 1995); full "Kanji & Kana" indices keyed by Olivier Galibert (April 1997); 2nd-edition numbering extension done by Enrique Sanchez Rosa
- **Heisig numbers**: initial ~1900 numbers keyed by Kevin Moore (1991); expanded set obtained from James Heisig directly (1995) via a list originally compiled by Magnus Halldorsson
- **Gakken numbers**: compiled by Antti Karttunen, added early 1990s
- **O'Neill numbers**: added August 1995, compiled by Jenny Nazak, David Rosenfeld, and Jim Breen
- **Henshall numbers**: supplied by Alfredo Pinochet (date unspecified)
- **Morohashi (Daikanwajiten) numbers and Four Corner codes**: originally extracted from a large file prepared by Dr Urs App (Hanazono College), passed on via Christian Wittern; Morohashi numbers proof-read by Christian Wittern (March 1994) and thoroughly checked against further sources in Jan–Feb 1996
- **New Nelson numbers**: added February 1998, keyed by Jean-Luc Leger
- **Classic Nelson numbers**: included from the 1991 origin; corrected in August 1996 using a comprehensive Nelson list prepared by Wolfgang Cronrath
- **De Roo codes**: added Dec 1998–Jan 1999, keyed by Jasmin Blanchette, with permission obtained directly from Fr De Roo
- **Other dictionary codes**: Tuttle flashcard numbers by Jim Breen; Crowley, Sakade, and Henshall 3rd-edition numbers by James Rose; Kodansha Compact Kanji Guide codes by Richard Fremmerlid; Kanji in Context codes by Randy Foreman; Maniette numbers by Alain Thierion; additional Japanese Flashcards numbers by Andrew Slater

### Radicals

- **Radical numbers**: KANJIDIC2 carries two radical fields per character — a classic Nelson radical number (`rad_type="nelson_c"`) and a classical (Kangxi) radical number (`rad_type="classical"`). The classical radical follows the Kangxi 214-radical system as codified in 「JIS漢字字典」(JIS Kanji Jiten, published by the Japanese Standards Association, 日本規格協会) — used "for the sake of consistency" wherever it differs from the Nelson radical. Nelson radical numbers were included from 1991 and corrected during Jeffrey Friedl's 1992 overhaul
- **Bushu codes**: large-scale corrections in April 1997, based on errors identified by Jean-Luc Leger, with missing codes added and ongoing regularization assistance from Ingar Holst

### Stroke counts

- Included from 1991; corrected in 1992 to match modern usage; Level 2 kanji (第二水準, the less common of JIS X 0208's two character tiers) stroke counts further corrected Dec 1997–Feb 1998 and again Dec 1998–Jan 1999, based on analysis by Wolfgang Cronrath, generally aligning with the New Nelson and S&H counts

### Meanings/glosses

- **English meanings**: initial ~1900 meanings from James Heisig's *Remembering The Kanji* (keyed by Kevin Moore, 1991), supplemented with meanings from Rik Smoody's files (compiled while working for Sony in Japan, apparently based on Nelson)
- **Spanish meanings**: compiled by Francisco Gutierrez, provided by Gabriel Sanroman
- **French meanings**: translated by Alain Thierion

### Grade, frequency, JLPT, and variants

- **Grade levels**: included from 1991; updated in 1992 to reflect the modern Jōyō kanji lists
- **Frequency rankings**: added 1992 by Jeffrey Friedl, based on an analysis of word frequencies in the Mainichi Shimbun over four years by Alexandre Girardi
- **JLPT levels**: updates provided by Andrew Slater
- **Variants (itaiji)**: a comprehensive "unification" of itaiji cross-references was carried out in May/August 1996, based on a list of itaiji identified by Taichi Kawabata and posted to the `fj.kanji` newsgroup

### Sources

- [KANJIDIC Project - History](https://www.edrdg.org/wiki/KANJIDIC_Project.html#History)

## Relation to Unihan

KANJIDIC2 and Unihan data overlap in several areas, including:

- **Radicals**: KANJIDIC2's classical/Nelson radical fields vs. Unihan's `kRSUnicode` (both based on the Kangxi radicals)
- **Stroke counts**: KANJIDIC2's stroke count field vs. Unihan's `kTotalStrokes`
- **Readings**: KANJIDIC2's on/kun readings vs. Unihan's `kJapaneseOn`/`kJapaneseKun` (and later `kJapanese`)
- **Dictionary indices**: KANJIDIC2's dictionary indices vs. Unihan's [dictionary indices](https://www.unicode.org/reports/tr38/#N1013C) (Morohashi, Nelson, etc.)

However, both data sets are independent of each other. They're neither identical (they actually often differ), nor is one based on the other. Looking at the timeline of how the two projects developed clarifies this:

- **1978**: 🗾 Publication of JIS X 0208, Japan's foundational character set standard, covering 6,355 kanji plus kana, Latin, and other characters
- **1987**: 🌐 Start of the Unicode project
- **1990**: 🌐 Start of work on Han unification by the CJK Joint Research Group (CJK-JRG) in the context of the Unicode project, leading to the development of Unihan
- **1991**: 👥 Start of the KANJIDIC project by Jim Breen — initial radical, stroke count, reading, and dictionary index data all included from the outset (for example, radical data based on the [JIS Kanji Jiten](https://ja.wikipedia.org/wiki/JIS%E6%BC%A2%E5%AD%97%E5%AD%97%E5%85%B8))
- **1991**: 🌐 Release of Unicode 1.0
- **1992**: 👥 Jeffrey Friedl's KANJIDIC overhaul — adding frequency rankings, correcting stroke counts, readings, and radicals
- **1994**: 👥 Morohashi dictionary indices added to KANJIDIC
- **1996**: 🌐 First release of Unihan as a component of Unicode 2.0, including readings (`kJapaneseOn`/`kJapaneseKun`), radicals (`kRSUnicode`), and some dictionary indices (`kMorohashi`, `kNelson`, etc.)
- **1997–1999**: 👥 Correction of stroke counts of many characters in KANJIDIC based on the counts in the New Nelson and Spahn & Hadamitzky dictionaries
- **2001**: 🌐 Unihan adds stroke counts (`kTotalStrokes` in Unicode 3.1)
- **2023**: 🌐 Unihan adds a new set of on and kun readings sourced from the [Character Information Technology Promotion Council's (CITPC)](https://moji.or.jp/) Moji Jōhō Kiban database (`kJapanese` in Unicode 15.1)

As can be seen from the timeline, the two projects started around the same time and developed in parallel to each other. They used different, but possibly overlapping, sources and presumably there was no inter-relation.

KANJIDIC relied heavily on JIS standards (especially JIS X 0208) and other Japanese reference works (Nelson's dictionary, Morohashi's Daikanwajiten, NJECD, etc.) contributed by its volunteers. Unihan on the other hand is not limited to Japan but spans across the entire CJK sphere, so it drew on official standards and reference works from China, Japan, Taiwan, Hong Kong, Singapore, Korea, and Vietnam.

### Sources

- [Unicode UAX #38: Unicode Han Database (Unihan)](https://www.unicode.org/reports/tr38/)

## Sources

- [KANJIDIC Project (EDRDG Wiki)](https://www.edrdg.org/wiki/KANJIDIC_Project.html)
