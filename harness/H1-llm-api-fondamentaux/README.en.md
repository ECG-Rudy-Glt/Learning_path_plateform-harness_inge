[🇫🇷 Français](README.md) · 🇬🇧 English

# H1 — LLM API & fundamentals

## Goals
- Call a model through the API: messages, system prompt, streaming, tool use, prompt caching.
- Understand tokens, context window, cost and latency.
- Know why a model "hallucinates" a tool call, and how the harness catches it.

## Key concepts
Messages API, roles, `tool_use` / `tool_result`, `stop_reason`, structured outputs, prompt caching, extended thinking, batch, rate limits, model choice (cost / capability).

## Sources
- 🟢 [Anthropic — API documentation](https://docs.claude.com/)
- 🟢 [Anthropic — Tool use](https://docs.claude.com/en/docs/agents-and-tools/tool-use/overview)
- 🟢 [Anthropic — Building effective agents](https://www.anthropic.com/engineering/building-effective-agents): workflows vs agents, worth rereading often
- 🔵 [Lilian Weng — LLM Powered Autonomous Agents](https://lilianweng.github.io/posts/2023-06-23-agent/)
- 🔵 [ReAct (Yao et al., 2022)](https://arxiv.org/abs/2210.03629)
- 📕 *AI Engineering: Building Applications with Foundation Models*, Chip Huyen (O'Reilly, Jan. 2025)

## Practice
→ [L-H1 — A mini-agent in ~200 lines](../../homelab/labs/L-H1-mini-agent.en.md)

## Validation
- [ ] I can read a raw response and say why the model stopped.
- [ ] My script measures the tokens and the cost of each turn.
- [ ] Prompt caching is enabled, and I have measured the gain.
