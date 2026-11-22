[🇫🇷 Français](README.md) · 🇬🇧 English

# H2 — Agent loop & tool design (ACI, MCP, skills)

## Goals
- Write a robust agent loop: tool errors, timeouts, turn limit, interruption.
- Design tools for an agent rather than for a human: naming, granularity, actionable errors, pagination.
- Expose capabilities through MCP, and package know-how as **skills**.

## Key concepts
Agent-Computer Interface (ACI), "poka-yoke" tools, concise rather than exhaustive responses, MCP (tools, resources, prompts, transports), skills (instructions loaded on demand, progressive disclosure), per-tool permissions.

## Sources
- 🟢 [Anthropic — Writing effective tools for agents](https://www.anthropic.com/engineering/writing-tools-for-agents)
- 🟢 [Model Context Protocol — spec & docs](https://modelcontextprotocol.io/)
- 🟢 [SWE-agent: Agent-Computer Interfaces (Yang et al., 2024)](https://arxiv.org/abs/2405.15793): evidence that the interface changes the outcome with the model held constant
- 🟢 [mattpocock/skills — *Skills for Real Engineers*](https://github.com/mattpocock/skills): small, composable skills (`tdd`, `diagnosing-bugs`, `to-spec`, `handoff`, `writing-for-agents`, `git-guardrails-claude-code`…). Read them as **examples of context and tool design**, and compare them with frameworks that "own the process" (GSD, BMAD, Spec-Kit).
- 🔵 [12-Factor Agents (HumanLayer)](https://github.com/humanlayer/12-factor-agents)
- 🔵 [Anthropic — Agent Skills](https://docs.claude.com/en/docs/agents-and-tools/agent-skills/overview)
- 🟢 [Simon Willison — Designing agentic loops](https://simonwillison.net/2025/Sep/30/designing-agentic-loops/) (Sep. 30, 2025): an agent is tools in a loop; it works on problems with clear success criteria, and in a sandbox
- 🟢 [Anthropic — Code execution with MCP](https://www.anthropic.com/engineering/code-execution-with-mcp) (A. Jones, C. Kelly, Nov. 4, 2025): expose MCP servers as code so only the needed tools are loaded; 150,000 → 2,000 tokens in their example
- 🔵 [Anthropic — Equipping agents for the real world with Agent Skills](https://www.anthropic.com/engineering/equipping-agents-for-the-real-world-with-agent-skills) (Oct. 16, 2025): `SKILL.md`, progressive disclosure, install only trusted skills
- 🔵 [CodeAct — Executable Code Actions Elicit Better LLM Agents](https://arxiv.org/abs/2402.01030) (Wang et al., ICML 2024): Python code as the action space, up to +20% success
- 🔵 [Agentless](https://arxiv.org/abs/2407.01489) (Xia et al., 2024): a fixed localisation → repair → validation pipeline, with no autonomous agent, beat the open-source agents of the time on SWE-bench Lite. Reread before making a harness more complex

## Practice
→ [L-H2 — Homelab MCP server](../../homelab/labs/L-H2-mcp-homelab.en.md)

## Validation
- [ ] Every tool has a tested description: the agent uses it correctly without an example.
- [ ] Error messages tell the agent what to do next.
- [ ] I have written at least 2 personal skills, inspired by `mattpocock/skills`, and I actually use them.
