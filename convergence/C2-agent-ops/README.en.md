[🇫🇷 Français](README.md) · 🇬🇧 English

# C2 — Homelab operations agent

An incident triage agent, **read-only at first**. It is the capstone project: platform, harness, evals and security all come together.

## Goals
- The agent receives an alert, reads metrics, logs and Flux state, then proposes a diagnosis and a runbook.
- The existing post-mortems (`HOMELAB/Documentation/postmortems/`) become the **eval set**: does the agent find the root cause?
- Escalation happens in stages: read-only, then proposing a PR, then acting with human approval.

## Sources
- 🟢 Google SRE book: *Effective Troubleshooting* and *Postmortem Culture* chapters
- 🟢 H4 (evals) and H5 (permissions)
- 🔵 [Anthropic — Building effective agents](https://www.anthropic.com/engineering/building-effective-agents), to know when a workflow is enough

## Practice
→ [L-C2 — Ops agent](../../homelab/labs/L-C2-agent-ops.en.md)
