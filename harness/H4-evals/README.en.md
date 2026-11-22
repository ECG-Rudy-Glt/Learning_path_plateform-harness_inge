[🇫🇷 Français](README.md) · 🇬🇧 English

# H4 — Agent evals

## Goals
- Build a representative task suite, with automatic graders (tests, end state, calibrated LLM-as-judge).
- Compare two versions of a harness with the model held constant, and the other way round.
- Read traces to classify failures (error analysis), instead of looking at a single score.

## Key concepts
Tasks with verifiable state, pass@k vs pass^k, variance and repetitions, LLM-as-judge and its calibration, contamination, regression evals in CI, error analysis by category.

## Sources
- 🟢 [Anthropic — Demystifying evals for AI agents (Jan. 2026)](https://www.anthropic.com/engineering/demystifying-evals-for-ai-agents): pass@k (at least 1 success in k) vs pass^k (k successes out of k); "20-50 simple tasks drawn from real failures" to get started; grade the outcome rather than the path; read the transcripts
- 🟢 [Hamel Husain — Your AI product needs evals](https://hamel.dev/blog/posts/evals/)
- 🟢 [Inspect AI (UK AISI)](https://inspect.aisi.org.uk/), an open-source evals framework
- 🟢 [SWE-bench](https://www.swebench.com/), to understand how a coding-agent benchmark is built
- 🔵 [τ-bench (Sierra, 2024)](https://arxiv.org/abs/2406.12045), which popularised pass^k for measuring reliability
- 🔵 [SWE-bench — the paper](https://arxiv.org/abs/2310.06770) (Jimenez et al., ICLR 2024): 2,294 real GitHub issues; the best model at the time solved 1.96%
- 🔵 [Judging LLM-as-a-Judge with MT-Bench and Chatbot Arena](https://arxiv.org/abs/2306.05685) (Zheng et al., 2023): over 80% agreement with humans, but position, verbosity and self-enhancement biases

## Practice
→ [L-H4 — Eval bench on homelab tasks](../../homelab/labs/L-H4-banc-evals.en.md)

## Validation
- [ ] 20+ tasks, each with an automatic grader.
- [ ] A report compares 2 harness variants, with at least 3 repetitions per task.
- [ ] A taxonomy of my most frequent failures exists.
