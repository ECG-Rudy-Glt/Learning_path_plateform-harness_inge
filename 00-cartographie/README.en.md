[🇫🇷 Français](README.md) · 🇬🇧 English

# 00 — Mapping the roles

## Platform Engineer

Builds and runs an **internal platform managed as a product**. It reduces the cognitive load on application teams through self-service golden paths.

Typical responsibilities:
- the platform API (CRDs, templates, IaC modules) and its contract with users;
- provisioning (clusters, network, databases, secrets) through declarative control planes;
- delivery (CI, GitOps, promotion between environments);
- default guardrails (policy as code, signed supply chain, secrets);
- observability, SLOs, on-call and post-mortems;
- measuring adoption and DevEx (DORA, SPACE, surveys).

## Harness Engineer

Designs **the environment around a model** so that an agent can carry out multi-step work reliably.

Typical responsibilities:
- the **agent loop**: model calls, tool execution, handling errors and stops;
- **tools**: agent-computer interface (ACI), MCP, schemas, useful error messages;
- **context**: system prompt, instruction files, retrieval, compaction, memory;
- **feedback loops**: tests, linters and checkers the agent can run on its own;
- **evals**: task suites, graders, regression measurement between two harness versions;
- **sandboxing**: permissions, filesystem and network isolation, secrets handling;
- **long-running**: handoff between sessions, progress artifacts, multi-agent orchestration;
- **costs and observability**: tokens, latency, tool-call traces.

## Overlap

| Concern | Platform side | Harness side |
|---|---|---|
| Interface | Platform API, CRDs | Tool schemas, MCP |
| Guardrails | Kyverno, RBAC, NetworkPolicy | Tool permissions, sandbox |
| Feedback | CI, preview envs | Tests and checkers in the loop |
| Measurement | DORA, SLOs | Evals, task success rate |
| Cognitive load | Golden paths | Context engineering |
| Isolation | Namespaces, VMs | gVisor, microVMs, egress allowlist |

## Cross-cutting sources

- 🟢 [CNCF — Platforms white paper](https://tag-app-delivery.cncf.io/whitepapers/platforms/)
- 🟢 [Thoughtworks — AI agent harness](https://www.thoughtworks.com/en-au/insights/blog/machine-learning-and-ai/ai-agent-harness)
- 🟢 [DigitalOcean — What is harness engineering?](https://www.digitalocean.com/resources/articles/what-is-harness-engineering)
- 🔵 [TechTarget — Agent harnesses as critical infrastructure](https://www.techtarget.com/it-infrastructure/tip/Harness-engineering-Agent-harnesses-as-critical-infrastructure)

## Exercise

Fill in the "Start" column of the self-assessment in [PROGRESSION.en.md](../PROGRESSION.en.md). Then, for each row rated 2 or below, write one sentence on what is missing.
