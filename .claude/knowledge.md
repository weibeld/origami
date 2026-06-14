# Research

---

## CJK Dictionary Institute (CJKI)

### What it is

A commercial linguistic institute and dictionary compilation company based in Niiza, Saitama, Japan, headed by Jack Halpern. Its principal activity is the compilation and licensing of large-scale lexical databases for CJK (Chinese, Japanese, Korean) and Arabic — currently over 50 million entries covering general vocabulary, proper nouns, technical terms, and NLP lexicons. These are licensed on a bespoke, case-by-case basis to IT companies and software developers, with clients including Google, Amazon, Microsoft, IBM, Fujitsu, Sharp, Sony, Yahoo, and Baidu. CJKI also offers consulting services in CJK and Arabic linguistics and data processing.

An increasingly significant part of their offering targets AI and NLP applications: alongside their core database licensing business, CJKI develops lexical resources and tooling specifically designed for deep learning, neural machine translation, speech technology, and — more recently — large language models.

### History

Founded in 1993 by Jack Halpern, CJKI grew out of his long-running work on Japanese lexicography. Halpern had begun compiling a new kind of kanji dictionary in 1974, motivated by his own frustrating experience with traditional rote-memorisation approaches to learning kanji. The project took 16 years and over 100 person-years of effort, culminating in the New Japanese-English Character Dictionary (Kenkyusha, 1990), which introduced the SKIP system for kanji indexing. The Kanji Dictionary Publishing Society (KDPS), also established in 1993 under Showa Women's University in Tokyo, served as the academic and publishing vehicle for this dictionary work.

From these kanji dictionary origins, CJKI gradually expanded into a broader CJK and Arabic lexical data business targeting the IT industry. As AI and NLP became central to the software industry, CJKI's databases found new applications as training data and infrastructure for machine learning systems — a direction the company has leaned into deliberately.

### Significance

CJKI occupies a niche but genuinely significant position in the CJK language technology industry. Its client list and database scale suggest real authority as a B2B provider of CJK and Arabic lexical data; the company claims to be the world's prime source for CJK lexical resources for the IT industry, and there is little to contradict this for the specific niche of large-scale, commercially licensed CJK data.

Its significance is likely larger than its low public profile suggests, and is growing rather than declining — primarily because of its deliberate move into the LLM space. LLMs fail badly on CJK proper nouns and technical terms: experiments conducted by CJKI in 2024 showed GPT-4 achieving a 54% error rate on Japanese proper nouns and place names in translation, reduced to 0% when their databases were injected into the prompt via RAG. This points to a structural gap that CJKI is uniquely positioned to fill: decades of compiled CJK and Arabic proper noun data is precisely what LLMs lack, and as LLMs expand beyond English this gap becomes more rather than less important.

### Sources

- [CJK Dictionary Institute (CJKI)](https://www.cjk.org)
- [Kanji Dictionary Publishing Society (KDPS)](https://www.kanji.org)

---

## Electronic Dictionary Research and Development Group (EDRDG)

### What it is

An independent, non-commercial research organisation dedicated to compiling electronic dictionaries and conducting computational linguistics research, with a focus on Japanese. Its principal output is a suite of open, freely licensed lexical datasets which collectively form the backbone of the open-source Japanese NLP and language-learning ecosystem. All data is released under a Creative Commons Attribution-ShareAlike 4.0 licence.

The datasets follow two models. Word and name dictionaries (JMdict, JMnedict) are original, community-compiled data — started by Breen and grown over decades through volunteer contributions. The kanji database (KANJIDIC2) is an aggregation: core kanji data (readings, English meanings) compiled by Breen from published references, with additional data points (SKIP codes, De Roo codes, Four Corner codes, Hadamitzky descriptors, etc.) contributed by their respective rights holders under explicit permission.

Current canonical datasets:

- **JMdict** — Japanese–English dictionary in XML format (formerly EDICT)
- **JMnedict** — Japanese proper names dictionary (~740,000 entries) in XML format (formerly ENAMDICT)
- **KANJIDIC2** — comprehensive kanji information database in XML format, covering JIS X 0208, JIS X 0212, and JIS X 0213 (successor to KANJIDIC)
- **KRADFILE2** — maps each kanji to the visual elements it is composed of (e.g. 哀 → 衣 口 亠). The elements are not classical radicals but informally identified visual components; the decomposition is based on visual examination rather than etymological principles and is somewhat subjective and inconsistent in how it handles recursion.
- **RADKFILE2** — the inverse of KRADFILE2: maps each visual element to all kanji containing it. Used to drive component-based kanji lookup (e.g. "show me all kanji containing 口").

### History

The group's origins lie in the personal project of Jim Breen, an Australian computer scientist who was an Associate Professor in the Faculty of Information Technology at Monash University in Melbourne. In 1991 Breen began compiling EDICT, a simple text-format Japanese–English dictionary file, which he made freely available. Over the following decade he expanded the project significantly — adding the WWWJDIC web dictionary server in 1998 and converting EDICT to the richer XML-format JMdict in 1999.

The Electronic Dictionary Research and Development Group was formally established in 2000 at Monash University primarily to serve two practical purposes: to hold the copyright for the dictionary files, and to receive and disburse funds in a tax-effective way. While initially just Breen himself, it gradually developed into an informal, globally distributed team of editors and developers. In 2006, Breen registered the edrdg.org domain and moved the group's activities to a rented cloud server, separating it from Monash University infrastructure.

Until February 2003 the dictionary files were restricted to non-commercial use. At that point the group transitioned to a Creative Commons Attribution-ShareAlike licence, opening the data to commercial use.

Maintenance of the project has gradually broadened beyond Breen. In 2010, Stuart McGraw developed the JMdictDB online database system, which took over maintenance of the JMdict/EDICT and later (2014) the JMnedict/ENAMDICT data.

### Significance

EDRDG's datasets are the de-facto standard data source for Japanese dictionary applications. Virtually every Japanese dictionary app and tool in use today — free or commercial, web or mobile — is built on JMdict, KANJIDIC2, or KRADFILE/RADKFILE. The data is actively queried and distributed daily, making EDRDG not just historically significant but a piece of live, load-bearing infrastructure for the Japanese language technology ecosystem.

### Sources

- [EDRDG homepage](https://www.edrdg.org/)
- [EDRDG Wiki (archived 2025-04-01)](https://web.archive.org/web/20250401012724/https://www.edrdg.org/wiki/index.php/Main_Page)
- [Jim Breen's homepage](https://www.edrdg.org/~jwb/)

---

## JMdict/EDICT

TODO

---

## ENAMDICT/JMnedict

TODO

---

## KRADFILE/RADKFILE

TODO

---

## KanjiVG

TODO

---

## Sources

- https://www.hadamitzky.de/english/lp_char_dict.htm
- https://www.hadamitzky.de/english/lp_radicals.htm
- https://www.hadamitzky.de/english/lp_how_to_determine.htm
- https://www.outlier-linguistics.com/blogs/chinese/getting-radical-about-radicals
- https://www.tofugu.com/japanese/how-to-use-a-kanji-dictionary/
