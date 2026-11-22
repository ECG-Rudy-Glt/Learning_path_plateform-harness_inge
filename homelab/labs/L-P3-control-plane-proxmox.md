🇫🇷 Français · [🇬🇧 English](L-P3-control-plane-proxmox.en.md)

# L-P3 — De Terraform manuel à un control plane

**But** : lever la limite « state Terraform local sans verrou », puis tester la réconciliation continue.

## Étapes
1. Appliquer l'ADR 0006 (`HOMELAB/Documentation/adr/0006-backend-terraform.md`) : backend S3 avec verrou, migration du state, sauvegarde testée.
2. Mettre en place un plan Terraform planifié en CI Forgejo : un plan non vide déclenche une alerte de **dérive**.
3. Expérimenter dans `lab-crossplane` : Crossplane + provider Terraform (`provider-terraform`) ou provider Proxmox communautaire, avec une XRD `LabVM` (taille, VLAN, image).
4. Rédiger un ADR Terraform+CI ou Crossplane, avec coûts et risques ; le post-mortem `terraform destroy` PBS est un argument à intégrer.

## Livrable
Backend migré, job de détection de dérive, ADR de décision.
