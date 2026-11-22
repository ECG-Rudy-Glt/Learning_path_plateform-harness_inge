[🇫🇷 Français](L-C1-agent-platform.md) · 🇬🇧 English

# L-C1 — Agent platform on k3s

**Goal**: merge L-P2, L-H5 and L-H4 into one platform service.

```yaml
apiVersion: platform.homelab/v1alpha1
kind: AgentTask
spec:
  repo: rudy/sport-coach
  prompt: "Fix issue #42"
  budget: { usd: 2, maxTurns: 80 }
  permissions: { write: pr-only }
```

## Steps
1. The controller (an extension of the L-P2 operator) creates a sandbox Pod (L-H5) and injects ephemeral credentials. The result is a PR and a `status`.
2. OTel GenAI traces → Collector → Tempo or Loki. A Grafana dashboard of cost per task and per project, and an alert when the budget is exceeded.
3. Harness CI: any prompt or tool change re-runs the L-H4 bench. A regression blocks the merge.
4. Expose the "launch an agent" template in Backstage (L-P4).

## Deliverable
`AgentTask` CRD in lab prod, cost dashboard, evals gate in CI.
