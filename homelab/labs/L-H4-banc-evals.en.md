[🇫🇷 Français](L-H4-banc-evals.md) · 🇬🇧 English

# L-H4 — Eval bench on homelab tasks

## Steps
1. Write 20 realistic tasks with a verifiable end state, for example:
   - "pod X is crashlooping, find out why" (incident injected into `lab-evals`);
   - "add an Alertmanager rule for Y" (validated with `promtool test rules`);
   - "fix this Ansible role so that `ansible-lint` passes".
2. Automatic graders (tests, `kubectl`, lint), plus a calibrated LLM judge only where it is unavoidable.
3. Run with [Inspect AI](https://inspect.aisi.org.uk/) or a home-made runner, 3 repetitions per task, and compute pass@1 and pass^3.
4. Compare: L-H1 mini-agent vs Claude Code, then MCP before vs after L-H2.
5. Do the error analysis: categorise failures by reading the traces.

## Deliverable
`homelab-evals` repo, comparison report, failure taxonomy.
