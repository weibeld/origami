# Radicals, Radical Systems, and Radical Ambiguity

## Radicals

- "Radical" is the English translation of the Chinese word 部首 *bùshǒu* (*bushu* in Japanese) which literally means "section head"
- Invented around 100 CE by Chinese scholar Xu Shen during the work on the 説文解字 [*Shuowen Jiezi*](https://en.wikipedia.org/wiki/Shuowen_Jiezi) (*Setsumon Kaiji* in Japanese), one of the earliest comprehensive Chinese character dictionaries containing about 10,000 character entries, as a character indexing and ordering system for this dictionary
- The idea by Xu Shen was to select a component of each character as the 部首 *bùshǒu* of this character and then list all characters with the same 部首 *bùshǒu* under the same section in the dictionary
  - The 部首 *bùshǒu* itself became the head of each section, hence the name "section head"
  - Xu Shen defined 540 部首 *bùshǒu*
- From that point on to this day, this idea of 部首 *bùshǒu* became the canonical way of ordering and indexing characters in Chinese and Japanese character dictionaries
- The set of radicals and the decision of which component of a character is its radical is an editorial decision by the dictionary creators and not an intrinsic property of the characters themselves
  - Therefore, different character dictionaries may use different sets of radicals and assign different radicals to each character
  - There is no objective truth of which is the true radical of a character outside of a specific radical system
- The radical of a character is often selected according to the meaning or position of the corresponding component within the character - but this is specific to each radical system
- In many radical systems, radicals may have a standard form and one or more variant forms
  - For example, in the Kangxi radical system, 水 is a radical and is also its standard form, which can be found for example in 泉 - but the radical also has 氵 as a variant form, which can be found for example in 海
  - Both standard form and variant forms belong to the same radical

---

## Radical Systems

A radical system consists of:

1. A set of radicals (including their standard and variant forms)
2. A set of rules for how to determine the radical of each character

Below is a historical outline about the most relevant radical systems.

### Shuowen Jiezi (121 CE)

- **Radical set:**
  - 540 radicals
  - Selected to create a cosmologically and sequentially coherent ordering among the section heads, not optimised for lookup efficiency
- **Determination rules:**
  - Not formalised
  - Radicals were assigned based on Xu Shen's judgment of shared graphic components
- **Introductory work:**
  - 説文解字 [*Shuōwén Jiězì*](https://en.wikipedia.org/wiki/Shuowen_Jiezi) (*Setsumon Kaiji* in Japanese), which means "graph explanations and character analyses", published in 121 CE
  - One of the first comprehensive Chinese character dictionaries containing around 10,000 character entries
- **Creator:**
  - Xu Shen (~58–148 CE)
- **Relevance:**
  - Introduced the concept of 部首 *bùshǒu* (*bushu* in Japanese), literally meaning "section head", which was later translated to English "radical"
  - Predecessor of all later radical systems

### Zihui (1615)

- **Radical set:**
  - 214 radicals
  - Largely a reduction of the 540 Shuowen Jiezi radicals
- **Determination rules:**
  - No deterministic rules that allow unambiguously determining the radical of a character
  - The radicals of characters seem to have been determined as editorial choices presumably based on etymological considerations, then this choice became an authoritative source on its own
- **Introductory work:**
  - 字彙 [*Zìhuì*](https://en.wikipedia.org/wiki/Zihui) (*Jii* in Japanese), which means "character collection"
  - ~33,000 characters
  - Published in 1615
- **Creator:**
  - Mei Yingzuo
- **Relevance:**
  - Introduced the 214 radicals that became later known as the Kangxi radicals
  - Introduced the radical-and-stroke sorting method which sorts characters with the same radical according to the stroke count in the character

### Kangxi (1716)

- **Radical set:**
  - 214 radicals
  - Inherited from the Zihui radical system
- **Determination rules:**
  - No deterministic rules for unambiguously determining the radical of a character (inherited from the Zihui radical system)
- **Introductory work:**
  - 康熙字典 [*Kāngxī Zìdiǎn*](https://en.wikipedia.org/wiki/Kangxi_Dictionary) (*Kōki Jiten* in Japanese), which means "character dictionary"
  - ~47,000 characters
  - Published in 1716
- **Creator:**
  - Zhang Yushu (1642–1711)
  - Chen Tingjing (1639–1712)
  - Hanlin Academy scholars
- **Relevance:**
  - Radical set commonly known as the "Kangxi radicals"
  - Fully encoded in Unicode in the Kangxi Radicals and CJK Radicals Supplement code blocks
  - Derivation source for most modern radical systems

### Nelson (1962)

- **Radical set:**
  - 214 radicals
  - Inherited from the Kangxi radicals
- **Determination rules:**
  - Radical Priority System: set of position-based rules for unambiguously determining the radical of any character
  - Assigns different radicals to some (about 12%) of the characters with respect to the Kangxi radical system
- **Introductory work:**
  - [The Modern Reader's Japanese-English Character Dictionary](https://en.wikipedia.org/wiki/The_Modern_Reader%27s_Japanese%E2%80%93English_Character_Dictionary)
  - ~5500 characters
  - Published in 1962
- **Creator:**
  - Andrew N. Nelson (1893–1975)
- **Relevance:**
  - Now largely obsolete but the Nelson radicals are still contained in the KANJIDIC2 data under `radical/rad_value[@rad_type="nelson_c"]` along with the Kangxi radicals

> **Note:** the Nelson radical system and dictionary from 1962 is often referred to as the "Classic Nelson" to contrast it from the "New Nelson" which refers to [The New Nelson Japanese-English Character Dictionary](https://en.wikipedia.org/wiki/The_New_Nelson_Japanese-English_Character_Dictionary) from 1997 (compiled by John H. Haig after Andrew N. Nelson's death). In the "New Nelson", the Nelson radical system is abandoned in favour of the Kangxi radical system.

### Hadamitzky (1989)

- **Radical set:**
  - 79 radicals
  - Reduced from the 214 Kangxi radicals
- **Determination rules:**
  - Set of deterministic rules for unambiguously determining the radical of any character
- **Introductory work:**
  - [Japanese Character Dictionary With Compound Lookup Via Any Kanji](https://www.amazon.com/Japanese-Character-Dictionary-Compound-English/dp/0887271707/)
  - ~6000 characters
  - Published in 1989
- **Creator:**
  - Wolfgang Hadamitzky (born 1941)
- **Relevance:**
  - One of the most compact radical systems in use today
  - Contained in the KANJIDIC2 data under `query_code/q_code[@qc_type="sh_desc"]`

---

## Radical Ambiguity

Traditional radical systems conflate two distinct purposes that are difficult to serve simultaneously. The first is semantic grouping — organising characters by a shared meaningful component so that related characters appear together. The second is lookup efficiency — enabling a reader to find a character unambiguously even without knowing anything about it in advance.

Lookup efficiency requires unambiguously determining the indexing position, such as the radical, under which the character is listed - this naturally sacrifices semantic meaning. On the other hand, semantic grouping requires building on the historic and semantic evolution of a character which in many cases excludes clear deterministic rules for determining the radical.

Up to the work by Nelson in 1962, character dictionaries just lived with this ambiguity which arguably hampered their usability. Nelson (1962) and then Hadamitzky (1989) attempted to address this issue by defining deterministic position-based rules for unambiguously determining the radical of any character. In doing so, they sacrified parts of the semantic grouping feature of traditional radical systems in favour of improved lookup efficiency.

In general, it might be beneficial to separate the two concerns. For semantic analysis and grouping, it might be best to solely focus on the functional components of characters (such as semantic and phonetic components), as for example done in the Outlier system, without attempting to double-use this as an indexing system. On the other hand, for lookup efficiency, it might be best to focus solely on determining an indexing position for each character in an efficient and unambiguous way, which may be completely position-based or visual, and exclude all semantic concerns.

For the lookup concern, radicals are actually not required at all, but indexing and lookup systems that are not based on radicals can be used as well.
