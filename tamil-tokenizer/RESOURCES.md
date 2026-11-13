# Tamil BPE Tokenizer Resources

## Knowledge

- [Paper: Neural Machine Translation of Rare Words with Subword Units (Sennrich et al., 2016)](https://arxiv.org/abs/1508.07909)
  Foundational subword BPE paper for NLP.
  Use for: original BPE merge algorithm and vocabulary sizing logic.
- [Hugging Face Tokenizers Documentation](https://huggingface.co/docs/tokenizers/index)
  Industry standard tokenization library architecture.
  Use for: understanding normalization, pretokenization, models, and decoders.
- [The Rust Programming Language Book](https://doc.rust-lang.org/book/)
  Official reference for Rust syntax, structs, traits, and modules.
  Use for: decoding Rust syntax (`match`, `Result`, `Option`, `Vec`, `impl`).
- [Codebase Learning Notes: Mental Model](./learning/01_mental_model_and_tokenization_basics.md)
  Repo-specific notes on Tamil byte representations and tokenization basics.
  Use for: understanding Tamil Unicode combining marks and token count trade-offs.
- [Codebase Architecture Deep Dive](./learning/02_codebase_architecture_and_deep_dive.md)
  Repo-specific systems analysis of data structures and optimization choices.
  Use for: reviewing pair key packing and compression benchmarks.

## Wisdom (Communities)

- [r/rust](https://reddit.com/r/rust)
  Active Rust community for systems programming and idiom checks.
- [r/MachineLearning](https://reddit.com/r/MachineLearning)
  Community discussions on LLM architectures, multilingual tokenization, and vocabulary compression.
