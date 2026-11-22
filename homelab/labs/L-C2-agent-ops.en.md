[🇫🇷 Français](L-C2-agent-ops.md) · 🇬🇧 English

# L-C2 — Incident triage agent

## Steps
1. Alertmanager webhook → `AgentTask` (L-C1) in read-only mode: Prometheus, Loki, `flux get`, `kubectl describe`.
2. Output: diagnosis, evidence (queries run) and proposed runbook, published to ntfy.
3. **Evals on real history**: replay the 3 post-mortems (certificate not renewed, PBS `terraform destroy`, OPNsense storm) as scenarios, and measure whether the agent finds the root cause.
4. Staged escalation: proposed fix PR, then action after human approval (ntfy button). Destructive actions are never automatic.

## Deliverable
Read-only ops agent live, score on the post-mortem scenarios, "autonomy levels" ADR.
