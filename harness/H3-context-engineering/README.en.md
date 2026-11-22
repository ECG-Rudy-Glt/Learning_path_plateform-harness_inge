[🇫🇷 Français](README.md) · 🇬🇧 English

# H3 — Context engineering

## Goals
- Treat context as a finite resource: every token has to earn its place.
- Organise information in layers: system prompt, instruction files (`CLAUDE.md` / `AGENTS.md`), skills, just-in-time retrieval, memory.
- Master compaction, structured notes and sub-agents to isolate context.

## Key concepts
Context rot, "right data, right place, right time", progressive disclosure, compaction vs reset, file-based memory, sub-agents as disposable context spaces, reducing noise in tool output.

## Sources
- 🟢 [Anthropic — Effective context engineering for AI agents](https://www.anthropic.com/engineering/effective-context-engineering-for-ai-agents)
- 🟢 🇫🇷 [IFTTD #383 — *Contexte Engineering : Dresser ses agents IA*, with Florian Bruniaux (Nov. 4, 2026)](https://www.ifttd.io/episodes/contexte-engineering) ([video](https://www.youtube.com/watch?v=Le5K1WheyBE)), in French. Context engineering is defined there as the umbrella discipline, and harness engineering as its tooling-and-verification part. The episode also covers moving the harness from the local machine into CI (cost, security, volume), then the question of reviewing code according to risk. Quote: *"Better a very good harness and a cheaper model than a very good model with a bad harness."*
- 🔵 [Claude Code Guide — Florian Bruniaux](https://cc.bruniaux.com), mentioned in the episode
- 🔵 [RTK — a CLI proxy that compresses command output for LLMs](https://github.com/rtk-ai/rtk), already part of my setup; see also [IFTTD #375 — RTK: the cost of tokens, with Patrick Szymkowiak](https://www.ifttd.io/episodes/rtk) (in French)
- 🔵 [Claude Code — Best practices](https://code.claude.com/docs/en/best-practices)
- 🔵 [OpenAI — Harness engineering (Feb. 2026)](https://openai.com/index/harness-engineering/): *"give Codex a map, not a 1,000-page instruction manual"*, an `AGENTS.md` of about 100 lines that acts as a table of contents pointing to `docs/`
- 🔵 [Chroma — Context Rot](https://research.trychroma.com/context-rot)
- 🟢 [Manus — Context Engineering for AI Agents: Lessons from Building Manus](https://manus.im/blog/Context-Engineering-for-AI-Agents-Lessons-from-Building-Manus) (Yichao "Peak" Ji, Jul. 18, 2025): KV-cache hit rate as the number-one metric, no adding or removing tools mid-run, the file system as context
- 🟢 [Lost in the Middle](https://arxiv.org/abs/2307.03172) (Liu et al., 2023): a model uses information at the start or end of the context better than in the middle

## Practice
→ [L-H3 — Context & memory of my agents](../../homelab/labs/L-H3-contexte-memoire.en.md)

## Validation
- [ ] My HOMELAB `CLAUDE.md` has been audited: every line is justified or deleted.
- [ ] I have measured the effect of RTK (tokens before/after) on a typical session.
- [ ] I know when to launch a sub-agent rather than do everything in the main context.
