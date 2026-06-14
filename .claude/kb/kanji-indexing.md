# Non-Radical Kanji Indexing and Lookup Systems

## Four Corner Method (1926)

- **Method:**
  - Maps characters to 4-digits codes by assigning a digit of 0–9 to each of the four corners of the character (in the order top-left, top-right, bottom-left, bottom-right) based on the type of stroke found there (for example, 1 for a horizontal stroke, 4 for two strokes crossing, etc.)
  - A fifth digit can optionally be added to disambiguate characters sharing the same four-corner code, in which case the fifth digit describe the type of stroke just above the lower-right corner
- **Introductory work:**
  - Four-Corner Method (pamphlet)
  - Published in 1926
- **Creator:**
  - Wang Yunwu (1888–1979)
- **Background:**
  - Initially created for Chinese telegraphers to look up the transmission codes for characters quickly without needing to know the pronunciation or meaning of the characters
  - Gained some adoption in China in the 1920s–30s but did not replace radicals as the dominant character indexing and lookup method
- **Relevance:**
  - Now largely obsolete but still contained in KANJIDIC2 under `query_code/q_code[@qc_type="four_corner"]` and the Unicode Unihan database as the `kFourCornerCode` property
- **Sources:**
  - <https://en.wikipedia.org/wiki/Four-corner_method>
  - <https://www.edrdg.org/~jwb/mondir/FOURCORNER.html>

## De Roo System (1980)

- **Method:**
  - Maps characters to a numeric code consisting of two parts: a 1 or 2-digit code for the top or top-left of the character, and a 2-digit code for the bottom or bottom-right of the character
  - The assigned code depends on the stroke pattern found at the relevant position: 37 patterns (codes 3-39) for the top/top-left and 40 patterns (codes 40-79) for the bottom/bottom-right
  - Similar idea as the Four Corner Method but with only two positions and a larger set of stroke patterns for each position
- **Introductory work:**
  - [2001 Kanji: Structure Analysis, Association Method, Fully Cross Referenced, Fast Visual Index](https://www.amazon.com/Structure-Analysis-Association-Method-Referenced/dp/B000LBB480/)
  - Published in 1980
- **Creator:**
  - Joseph R. De Roo (1932-2001)
- **Background:**
  - Joseph R. De Roo was a Belgian missionary who taught Japanese to foreigners at the Institute of Japanese Studies of the St. Joseph Friary in Roppongi
  - The De Roo codes define the order of the kanji in the _2001 Kanji_ book, which provides component analysis and mnemonics for all kanji (similar to the works by Heisig and Henshall)
- **Relevance:**
  - Included in KANJIDIC2 under `query_code/q_code[@qc_type="deroo"]`
- **Sources:**
  - <https://www.edrdg.org/~jwb/mondir/deroo.html>

## System of Kanji Indexing by Patterns (SKIP) (1990)

- **Method:**
  - Maps each character to a numeric code consisting of three parts separated by dashes (for example, *1-3-10*):
    1. Part 1: category of how the kanji can be divided into sections which may be one of 1 (left-right), 2 (up-down), 3 (enclosure), or 4 (solid)
    2. Part 2: number of strokes in the first section of the kanji (in particular, the left, top, or enclosing part)
    3. Part 3: number of strokes in the second section of the kanji (in particular, the right, bottom, or enclosed part)
  - Special rules for category 4 (solid): the second part of the code is the total number of strokes of the kanji and the third part denotes a sub-pattern of the kanji which may be one of 1 (prominent horizontal stroke at the top), 2 (prominent horizontal stroke at the bottom), 3 (prominent vertical through stroke), or 4 (others)
  - For categories 1 and 2: if the kanji can be divided into more than two sections, then either the leftmost or topmost section is taken as the first section and the entire rest to the right or bottom is taken as the second section
- **Introductory work:**
  - [New Japanese-English Character Dictionary](https://www.amazon.com/Japanese-English-character-dictionary-Jack-Halpern/dp/4767490405)
  - Published in 1990
- **Creator:**
  - Jack Halpern (born 1946)
- **Background:**
  - One of several radical-independent kanji lookup systems developed in the 20th century, alongside the Four Corner Method and the De Roo System
  - Arguably simpler in practice than the Four Corner Method and De Roo System: only 4 patterns to identify, then stroke counting — no large number of patterns to memorise
- **Relevance:**
  - Included in KANJIDIC2 under `query_code/q_code[@qc_type="skip"]`
  - Used as the primary lookup method in [The Kodansha Kanji Learner's Dictionary](https://www.amazon.com/Kodansha-Kanji-Learners-Dictionary-Expanded/dp/1568364075/) (1999, 2013, 2022) and [The Kodansha Kanji Dictionary](https://www.amazon.com/Kodansha-Kanji-Dictionary-Jack-Halpern/dp/1568364083) (2013)
- **Sources:**
  - <https://en.wikipedia.org/wiki/The_Kodansha_Kanji_Learner%27s_Dictionary#SKIP>
  - <https://www.edrdg.org/~jwb/mondir/SKIP.html>
