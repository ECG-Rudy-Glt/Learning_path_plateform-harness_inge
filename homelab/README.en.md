[🇫🇷 Français](README.md) · 🇬🇧 English

# Homelab learning

The labs build on the **existing** infrastructure in the `HOMELAB` repository rather than on a throwaway environment: mistakes have a real cost, and that is what makes you learn.

## Starting point (Nov. 2026)

| Building block | In place |
|---|---|
| Hypervisor | 2× Proxmox VE (EliteDesk 800 G6), bare-metal OPNsense, 802.1Q VLANs |
| IaC | Terraform `bpg/proxmox` (16 LXC, 6 VMs), Ansible (24 roles), local state (ADR 0006 `HOMELAB/Documentation/adr/0006-backend-terraform.md` pending) |
| Cluster | k3s v1.36 (1 master, 1 worker), FluxCD, MetalLB, cert-manager, Traefik |
| Apps | patrimoine, sport-coach, freelance, media, speedtest |
| CI | Forgejo Actions |
| Secrets / PKI | OpenBao KV v2 + 2-tier PKI, Authentik OIDC |
| Observability | Prometheus, Grafana, Loki + Alloy, Alertmanager (13 rules) |
| Culture | ADRs, post-mortems (certificate, PBS `terraform destroy`, OPNsense) |

🎧 🇫🇷 Worth a listen alongside: [IFTTD #354 — Self Hosting, with Loic Tosser](https://www.ifttd.io/episodes/self-hosting) (in French): redoing everything to be independent.

## Lab rules

1. **Branch + PR** in `HOMELAB` for every infra change. No `apply` outside Git.
2. Each lab delivers an **ADR** if it makes a structural choice, and a **post-mortem** if it breaks something.
3. Agent labs (H, C) start **read-only**. Write permissions are earned after evals.
4. New components go into a `lab-*` namespace, so they can be removed cleanly.

## Index

| Lab | Module | Deliverable |
|---|---|---|
| [L-P1](labs/L-P1-charte-plateforme.en.md) | P1 | Charter + maturity positioning |
| [L-P2](labs/L-P2-operateur-app.en.md) | P2 | `App` operator (kubebuilder) |
| [L-P3](labs/L-P3-control-plane-proxmox.en.md) | P3 | Terraform backend + reconciled resource |
| [L-P4](labs/L-P4-golden-path-backstage.en.md) | P4 | Backstage + "new app" template |
| [L-P5](labs/L-P5-supply-chain-signee.en.md) | P5 | Signed images + Kyverno + SBOM |
| [L-P6](labs/L-P6-slo-dora.en.md) | P6 | Burn-rate SLOs + DORA |
| [L-H1](labs/L-H1-mini-agent.en.md) | H1 | Mini-agent from scratch |
| [L-H2](labs/L-H2-mcp-homelab.en.md) | H2 | Reviewed homelab MCP server + skills |
| [L-H3](labs/L-H3-contexte-memoire.en.md) | H3 | Context audit + RTK measurement |
| [L-H4](labs/L-H4-banc-evals.en.md) | H4 | 20-task eval bench |
| [L-H5](labs/L-H5-sandbox-k3s.en.md) | H5 | gVisor agent pod + egress allowlist |
| [L-H6](labs/L-H6-agent-longue-duree.en.md) | H6 | Project delivered over multiple sessions |
| [L-C1](labs/L-C1-agent-platform.en.md) | C1 | `AgentTask` CRD + OTel traces |
| [L-C2](labs/L-C2-agent-ops.en.md) | C2 | Triage agent evaluated on the post-mortems |
