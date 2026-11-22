[🇫🇷 Français](L-P3-control-plane-proxmox.md) · 🇬🇧 English

# L-P3 — From manual Terraform to a control plane

**Goal**: remove the "local Terraform state without locking" limitation, then try continuous reconciliation.

## Steps
1. Apply ADR 0006 (`HOMELAB/Documentation/adr/0006-backend-terraform.md`): S3 backend with locking, state migration, tested backup.
2. Set up a scheduled Terraform plan in Forgejo CI: a non-empty plan raises a **drift** alert.
3. Experiment in `lab-crossplane`: Crossplane + Terraform provider (`provider-terraform`) or a community Proxmox provider, with a `LabVM` XRD (size, VLAN, image).
4. Write an ADR choosing Terraform+CI or Crossplane, with costs and risks; the PBS `terraform destroy` post-mortem is an argument to include.

## Deliverable
Migrated backend, drift-detection job, decision ADR.
