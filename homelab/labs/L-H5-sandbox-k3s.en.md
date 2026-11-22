[🇫🇷 Français](L-H5-sandbox-k3s.md) · 🇬🇧 English

# L-H5 — Agent sandbox on k3s

## Steps
1. Install gVisor (`runsc`) on the k3s worker, then create a gvisor `RuntimeClass`.
2. Create the `lab-agents` namespace: Pod Security `restricted`, default-deny NetworkPolicy, egress allowed only to the model API and Forgejo (through a proxy or an FQDN policy).
3. For credentials, authenticate to OpenBao with the ServiceAccount (kubernetes auth), and get a repo-scoped Forgejo token with a 1 h TTL.
4. Red-team: make the agent read a booby-trapped README (prompt injection) that tries to exfiltrate a secret. Document what blocks it and what gets through.
5. Evaluate [agent-sandbox](https://github.com/kubernetes-sigs/agent-sandbox) as an alternative.

## Deliverable
`lab-agents` Flux manifests, red-team report, "agent isolation" ADR.
