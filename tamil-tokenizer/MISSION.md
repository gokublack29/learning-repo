# Mission: Tamil BPE Tokenizer Architecture and Systems

## Why
Understand how this Tamil BPE tokenizer works from scratch without prior Rust or BPE experience.
Trace code execution, run training and inference, and navigate every file with confidence.

## Success looks like
- Locate and run each CLI entry point in under one minute.
- Trace text through pretokenization, base vocab seeding, and BPE merges into token IDs.
- Run training and encoding commands on real Tamil text and inspect the outputs.
- Explain the role of all five core modules in the crate.

## Constraints
- Zero prior knowledge of Rust, BPE algorithms, or this codebase.
- ADHD mode: high signal, numbered steps, visual diagrams, five-minute bite-sized lessons.
- Plain dashes only.
- Each full sentence on its own line in Markdown files.

## Out of scope
- Deep Rust memory management internals like raw pointers or manual memory allocators.
- Training multi-billion parameter transformer neural networks.
