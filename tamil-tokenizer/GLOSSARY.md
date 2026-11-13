# Tamil Tokenizer Glossary

Canonical terminology for Tamil orthography and BPE tokenization used across lessons and learning records.

## Terms

**Independent Vowel**:
A standalone vowel character used only at the beginning of a word or syllable.
Examples in Tamil include `அ`, `ஆ`, `இ`, `ஈ`.
_Avoid_: Free vowel, primary vowel

**Consonant**:
A base sound that in Tamil orthography inherently carries an unspoken short 'a' vowel unless modified.
Examples in Tamil include `க` (ka), `ப` (pa), `த` (ta).
_Avoid_: Base letter, alphabet letter

**Pulli (Virama)**:
A diacritic dot placed above a Tamil consonant that suppresses its inherent 'a' vowel, producing a pure silent consonant.
For example, `க` (ka) + pulli `்` becomes `க்` (k).
_Avoid_: Halant, dot mark

**Vowel Sign (Maatra)**:
A dependent combining glyph attached to a consonant to replace its default vowel sound with another vowel.
For example, the sign `ா` changes `க` (ka) to `கா` (kaa).
_Avoid_: Dependent vowel, modifier sign

**Conjunct Stem**:
A two-consonant cluster formed by a consonant, a pulli, and a second consonant (`C1 + ் + C2`).
Common examples include `ண்ட` (`ண + ் + ட`), `த்த` (`த + ் + த`), and `க்க` (`க + ் + க`).
_Avoid_: Ligature compound, consonant cluster token

**Pretokenization**:
The initial step of slicing raw text into bounded chunks like words, numbers, and punctuation using regular expressions before BPE begins.
Pretokenization prevents subword merges from crossing word or punctuation boundaries.
_Avoid_: Word splitting, initial segmentation

**Combining Mark (`\p{M}`)**:
A Unicode character category for diacritic glyphs, viramas/pullis, and vowel signs that attach to preceding base letters.
In Tamil, the pulli and vowel signs are combining marks that modify base consonants.
_Avoid_: Accent mark, floating symbol

**Regular Expression (Regex)**:
A formalized pattern syntax used to search, match, and slice text by structure and character category rather than exact string values.
In tokenizers, regex patterns act as pre-tokenization rules to establish chunk boundaries.
_Avoid_: String pattern, text matcher

**Unicode Property (`\p{Category}`)**:
A standard metadata classification assigned to every character in the Unicode specification describing its linguistic role (such as Letter, Mark, Number, or Punctuation).
Pretokenizers query Unicode properties to write language-agnostic text segmentation rules.
_Avoid_: Unicode tag, character attribute

**Bit-Packed Pair Key (`u64`)**:
A 64-bit unsigned integer encoding two 32-bit token IDs via bit-shift (`(a << 32) | b`) to avoid heap allocations during pair counting.
_Avoid_: Fast tuple, integer pair

**Inverted Index (`pair_positions`)**:
A lookup map linking each token pair key to the set of word indices that contain it, enabling targeted in-place updates during merges.
_Avoid_: Reverse map, position cache

**Priority Queue (BinaryHeap)**:
A max-heap data structure that maintains elements in sorted order so the highest-frequency token pair can be retrieved in $O(1)$ time.
_Avoid_: Sorted list, rank array

**Priority Merging (Rank Order)**:
The greedy inference rule where adjacent token pairs with the lowest rank index (learned earliest in training) are always merged first.
_Avoid_: Greedy substitution, rank precedence

**Byte Fallback**:
A mechanism where any character missing from the subword vocabulary is decomposed into its constituent UTF-8 bytes (0 to 255), guaranteeing 100% lossless tokenization without unknown token replacement.
_Avoid_: Char fallback, raw byte rescue

**Compressed Sparse Row (CSR)**:
A cache-friendly array representation that packs second tokens, ranks, and replacement IDs into a contiguous memory slice to prevent CPU cache misses at large vocabulary sizes.
_Avoid_: Array table, packed matrix

**Zero-Training Base Vocabulary**:
A pre-compiled initial vocabulary containing all script letters, vowel combinations, and conjunct stems, enabling valid subword tokenization without running corpus training first.
_Avoid_: Pre-trained vocabulary, default dictionary

**Token Fertility**:
The average number of subword tokens produced per word or character in a given language.
Lower fertility means higher compression and lower LLM inference cost.
_Avoid_: Token efficiency, split ratio

**Option<T>**:
A Rust enum representing an optional value: either Some(value) containing data, or None representing absence (replacing null).
_Avoid_: Nullable type, maybe value

**Result<T, E>**:
A Rust enum representing an operation outcome: either Ok(T) on success, or Err(E) on failure (replacing exceptions).
_Avoid_: Return status, error container

**The ? Operator**:
A Rust operator that unwraps an Ok value from a Result, or returns the Err early from the enclosing function.
_Avoid_: Try operator, bail macro

**Borrowing (& and &mut)**:
A Rust mechanism passing a temporary reference to existing memory: & for shared read-only access, &mut for exclusive write access.
_Avoid_: Pointer pass, reference copy
