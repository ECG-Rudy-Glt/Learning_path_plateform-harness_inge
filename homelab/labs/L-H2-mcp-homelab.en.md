[🇫🇷 Français](L-H2-mcp-homelab.md) · 🇬🇧 English

# L-H2 — Homelab MCP server & skills

**Goal**: review the existing homelab MCP server against the principles in [Writing effective tools for agents](https://www.anthropic.com/engineering/writing-tools-for-agents).

## Steps
1. Inventory the exposed tools: name, description, granularity, response size.
2. For each tool, check: is it named after an intent? are responses paginated or truncated? are errors actionable? are dangerous operations kept separate?
3. Add high-level tools (`app_status(app)`, which aggregates pods, Flux and the last deployment) rather than exposing raw `kubectl`.
4. Put the MCP behind Authentik, with separate read and write scopes.
5. Write 2 personal skills (e.g. `homelab-deploy-check`, which follows the "verify the rollout before announcing" memory, and `postmortem`), modelled on the structure of [mattpocock/skills](https://github.com/mattpocock/skills).

## Deliverable
Refactored MCP, before/after measured on 5 tasks, 2 skills in `~/.claude/skills`.
