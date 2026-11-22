[🇫🇷 Français](L-H1-mini-agent.md) · 🇬🇧 English

# L-H1 — A mini-agent in ~200 lines

**Goal**: write your own loop without a framework, to know what Claude Code or Codex do under the hood.

## Steps
1. Python or Go, Anthropic SDK, 3 tools: `read_file`, `run_command` (with an allowlist), `edit_file` (exact replacement).
2. Loop: call → `tool_use` → execution → `tool_result` (with `is_error` when needed) → repeat until `end_turn` or a limit of N turns.
3. On every turn, log input/output tokens, tokens read from and written to the cache, and the cost.
4. Test task: "add a missing unit test in a small toy repo and make it pass".
5. Vary the tool descriptions and observe the effect on the result.

## Deliverable
`mini-agent` repo, experiment log in `notes/`.
