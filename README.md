# learning-repo

Interactive Engineering Masterclass Hub hosting multi-track architecture and systems lessons.

Live GitHub Pages URL: https://gokublack29.github.io/learning-repo/

## Course Tracks

### 1. TriageMate Track (`/triagemate/`)
Automated SAST noise reduction and hybrid State-Space Model triage.
Focuses on Semgrep taint flows, AST sink extraction, and fine-tuned LiquidAI d1-3B models.

- `triagemate/index.html`: Full interactive web app (54-commit time machine, 6 entry points, interactive 5-stage pipeline & logit calculator, Chart.js leaderboard, 28 Q&As + quiz).
- `triagemate/lesson_01_foundations_zero_to_one.html`: Zero-to-one foundations, SVG architecture diagram, and self-check drill.
- `triagemate/lesson_02_recursive_54_commits.html`: Complete table of all 54 commits in recursive backtracking order (#54 -> #1).
- `triagemate/lesson_03_all_entry_points.html`: All 6 entry points with exact CLI commands and call-graph targets.
- `triagemate/lesson_04_end_to_end_data_flows.html`: Line-by-line annotated code walkthroughs (`sink_finder.py`, `engine.py`, `decision.py`) and numerical stability drill.
- `triagemate/lesson_05_decisions_and_consequences.html`: All 6 architectural pivots and empirical consequences.
- `triagemate/lesson_06_evaluation_gates_and_math.html`: L0/L2/L3 gates, `P@90R`, `ECE`, `Within-Rule AUC`, and full leaderboard.
- `triagemate/lesson_07_interview_prep_guide.html`: Interactive interview defense drills.

### 2. Tamil Tokenizer Track (`/tamil-tokenizer/`)
High-performance Byte Pair Encoding (BPE) tokenizer engineered from scratch in pure Rust.
Focuses on Tamil orthography, conjunct stems, Unicode regex pretokenization, and zero-allocation inference.

- `tamil-tokenizer/index.html`: Complete 13-step learning path dashboard.
- `tamil-tokenizer/reference/architecture-cheat-sheet.html`: One-page architecture cheat sheet.
- `tamil-tokenizer/interview/dossier.html`: Staff-level interview dossier covering all design decisions and benchmark numbers.
- `tamil-tokenizer/lessons/`: 12 comprehensive lessons covering data flow, orthography, regex, BPE engine, and Rust systems programming.
- `tamil-tokenizer/*.rs`: Complete original Rust implementation files hyperlinked directly from the lessons.
