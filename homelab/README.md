🇫🇷 Français · [🇬🇧 English](README.en.md)

# Homelab learning

Les labs s'appuient sur l'infrastructure **existante** du dépôt `HOMELAB` plutôt que sur un environnement jetable : les erreurs ont un vrai coût, et c'est ce qui fait apprendre.

## Point de départ (nov. 2026)

| Brique | En place |
|---|---|
| Hyperviseur | 2× Proxmox VE (EliteDesk 800 G6), OPNsense bare metal, VLANs 802.1Q |
| IaC | Terraform `bpg/proxmox` (16 LXC, 6 VM), Ansible (24 rôles), state local (ADR 0006 `HOMELAB/Documentation/adr/0006-backend-terraform.md` en attente) |
| Cluster | k3s v1.36 (1 master, 1 worker), FluxCD, MetalLB, cert-manager, Traefik |
| Apps | patrimoine, sport-coach, freelance, media, speedtest |
| CI | Forgejo Actions |
| Secrets / PKI | OpenBao KV v2 + PKI 2 niveaux, Authentik OIDC |
| Observabilité | Prometheus, Grafana, Loki + Alloy, Alertmanager (13 règles) |
| Culture | ADR, post-mortems (certificat, `terraform destroy` PBS, OPNsense) |

🎧 🇫🇷 À écouter en parallèle : [IFTTD #354 — Self Hosting : tout refaire pour être indépendant, avec Loic Tosser](https://www.ifttd.io/episodes/self-hosting).

## Règles des labs

1. **Branche + PR** dans `HOMELAB` pour tout changement d'infra. Pas d'`apply` hors Git.
2. Chaque lab livre un **ADR** s'il fait un choix structurant, et un **post-mortem** s'il casse quelque chose.
3. Les labs agents (H, C) démarrent en **lecture seule**. Les permissions d'écriture se gagnent après évals.
4. Les nouveaux composants vont dans un namespace `lab-*`, pour pouvoir les supprimer proprement.

## Index

| Lab | Module | Livrable |
|---|---|---|
| [L-P1](labs/L-P1-charte-plateforme.md) | P1 | Charte + positionnement maturité |
| [L-P2](labs/L-P2-operateur-app.md) | P2 | Opérateur `App` (kubebuilder) |
| [L-P3](labs/L-P3-control-plane-proxmox.md) | P3 | Backend Terraform + ressource réconciliée |
| [L-P4](labs/L-P4-golden-path-backstage.md) | P4 | Backstage + template « nouvelle app » |
| [L-P5](labs/L-P5-supply-chain-signee.md) | P5 | Images signées + Kyverno + SBOM |
| [L-P6](labs/L-P6-slo-dora.md) | P6 | SLO burn-rate + DORA |
| [L-H1](labs/L-H1-mini-agent.md) | H1 | Mini-agent from scratch |
| [L-H2](labs/L-H2-mcp-homelab.md) | H2 | Serveur MCP homelab revu + skills |
| [L-H3](labs/L-H3-contexte-memoire.md) | H3 | Audit du contexte + mesure RTK |
| [L-H4](labs/L-H4-banc-evals.md) | H4 | Banc d'évals 20 tâches |
| [L-H5](labs/L-H5-sandbox-k3s.md) | H5 | Pod agent gVisor + egress allowlist |
| [L-H6](labs/L-H6-agent-longue-duree.md) | H6 | Projet livré en multi-session |
| [L-C1](labs/L-C1-agent-platform.md) | C1 | CRD `AgentTask` + traces OTel |
| [L-C2](labs/L-C2-agent-ops.md) | C2 | Agent de triage évalué sur les post-mortems |
