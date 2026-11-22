🇫🇷 Français · [🇬🇧 English](README.en.md)

# P3 — IaC & control planes

## Objectifs
- Passer de « Terraform lancé à la main » à une **API déclarative réconciliée en continu**.
- Concevoir des abstractions : modules, compositions, XRD.
- Gérer l'état, la dérive et les secrets proprement.

## Concepts clés
State et locking, drift detection, modules versionnés, Crossplane v2 (projet CNCF *graduated*, composition : XRD, Composition, composition Functions en YAML/KCL/Python/Go), modèle de Kratix (Promises), Terraform contre control plane, OpenTofu.

## Sources
- 🟢 [Crossplane — What's Crossplane](https://docs.crossplane.io/latest/whats-crossplane/) puis [Composition](https://docs.crossplane.io/latest/composition/)
- 🔵 [Crossplane — Upgrade to v2](https://docs.crossplane.io/latest/guides/upgrade-to-crossplane-v2/) : ce qui change par rapport aux tutoriels v1 (claims)
- 🟢 [OpenTofu docs](https://opentofu.org/docs/)
- 🔵 [Kratix — Promises](https://docs.kratix.io/)
- 🔵 [Terraform — Module best practices](https://developer.hashicorp.com/terraform/language/modules/develop)
- 📕 *Terraform: Up & Running*, Yevgeniy Brikman (O'Reilly, 3e éd. 2022)

## Pratique
→ [L-P3 — Control plane pour VM Proxmox](../../homelab/labs/L-P3-control-plane-proxmox.md)

## Validation
- [ ] Je peux argumenter Terraform vs Crossplane pour un cas donné (rédigé sous forme d'ADR).
- [ ] Une ressource du homelab est demandée par un manifeste et réconciliée sans `terraform apply` manuel.
- [ ] La dérive est détectée et signalée.
