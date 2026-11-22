[🇫🇷 Français](README.md) · 🇬🇧 English

# P3 — IaC & control planes

## Goals
- Move from "Terraform run by hand" to a **declarative API reconciled continuously**.
- Design abstractions: modules, compositions, XRDs.
- Handle state, drift and secrets properly.

## Key concepts
State and locking, drift detection, versioned modules, Crossplane v2 (CNCF *graduated* project; composition: XRD, Composition, composition Functions in YAML/KCL/Python/Go), the Kratix model (Promises), Terraform vs control plane, OpenTofu.

## Sources
- 🟢 [Crossplane — What's Crossplane](https://docs.crossplane.io/latest/whats-crossplane/) then [Composition](https://docs.crossplane.io/latest/composition/)
- 🔵 [Crossplane — Upgrade to v2](https://docs.crossplane.io/latest/guides/upgrade-to-crossplane-v2/): what changed compared with v1 tutorials (claims)
- 🟢 [OpenTofu docs](https://opentofu.org/docs/)
- 🔵 [Kratix — Promises](https://docs.kratix.io/)
- 🔵 [Terraform — Module best practices](https://developer.hashicorp.com/terraform/language/modules/develop)
- 📕 *Terraform: Up & Running*, Yevgeniy Brikman (O'Reilly, 3rd ed. 2022)

## Practice
→ [L-P3 — Control plane for Proxmox VMs](../../homelab/labs/L-P3-control-plane-proxmox.en.md)

## Validation
- [ ] I can argue Terraform vs Crossplane for a given case (written as an ADR).
- [ ] A homelab resource is requested through a manifest and reconciled without a manual `terraform apply`.
- [ ] Drift is detected and reported.
