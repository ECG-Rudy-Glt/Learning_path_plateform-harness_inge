[🇫🇷 Français](README.md) · 🇬🇧 English

# C1 — A platform for running agents

The harness becomes a **platform product**: any homelab project can launch an agent in an isolated, observed and budgeted environment.

## Goals
- Offer an "AgentTask" CRD or API: repo, instruction, budget, permissions.
- Run each task in an ephemeral sandbox, with dynamic credentials.
- Trace LLM and tool calls with the OTel GenAI conventions, and track cost per task and per project.
- Run the harness evals in CI before every prompt or tool change.

## Sources
- 🟢 [OpenTelemetry — GenAI semantic conventions](https://github.com/open-telemetry/semantic-conventions-genai) (moved off the main site into this repository)
- 🟢 [kubernetes-sigs/agent-sandbox](https://github.com/kubernetes-sigs/agent-sandbox): `SandboxWarmPool` to start agents without waiting
- 🔵 [IFTTD #383](https://www.ifttd.io/episodes/contexte-engineering) (in French): moving the harness from the local machine into CI
- 🔵 All of modules P2, P5, P6, H4 and H5
- 🟢 🎧 🇫🇷 [IFTTD #384 — Usine logicielle 100% AI, with Nikolay Rodionov (Nov. 11, 2026)](https://www.ifttd.io/episodes/usine-logicielle-100-ai) (in French): agents in ephemeral sandboxes, PRs at volume, review as the bottleneck, building a reliable harness
- 🟢 🎧 🇫🇷 [IFTTD #382 — Rapprocher la CI, with Yves Brissaud (Oct. 28, 2026)](https://www.ifttd.io/episodes/rapprocher-la-ci) (in French): AI multiplies the pace 20x and CI must keep up; fine-grained cache, parallelism, hybrid local/remote runs

## Practice
→ [L-C1 — Agent platform on k3s](../../homelab/labs/L-C1-agent-platform.en.md)
