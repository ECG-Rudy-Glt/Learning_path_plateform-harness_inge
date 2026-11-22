🇫🇷 Français · [🇬🇧 English](README.en.md)

# P5 — Sécurité, policy as code & supply chain

## Objectifs
- Signer les images et vérifier les signatures à l'admission.
- Générer des SBOM et scanner les vulnérabilités dans la CI.
- Appliquer des policies par défaut : pas de root, limites de ressources, registries autorisées.
- Remplacer les secrets statiques par des secrets dynamiques à courte durée de vie.

## Concepts clés
SLSA levels, provenance, Sigstore (cosign, keyless, Rekor), SBOM (SPDX/CycloneDX), Kyverno / Gatekeeper, Pod Security Standards, External Secrets / Vault Agent, secrets dynamiques OpenBao.

## Sources
- 🟢 [SLSA](https://slsa.dev/)
- 🟢 [Sigstore — cosign](https://docs.sigstore.dev/)
- 🟢 [Kyverno docs](https://kyverno.io/docs/)
- 🔵 [Kubernetes — Pod Security Standards](https://kubernetes.io/docs/concepts/security/pod-security-standards/)
- 🔵 [OpenBao docs](https://openbao.org/docs/)
- 🔵 [CNCF — Software Supply Chain Best Practices](https://github.com/cncf/tag-security/tree/main/community/working-groups/supply-chain-security/supply-chain-security-paper)
- 🎧 🇫🇷 [IFTTD #358 — DevSecOps : pourquoi l'automatisation ne sauvera pas (toute seule) la sécu, avec Tugdual Grall (27 mai 2026)](https://www.ifttd.io/episodes/devsecops)

## Pratique
→ [L-P5 — Supply chain signée](../../homelab/labs/L-P5-supply-chain-signee.md)

## Validation
- [ ] Une image non signée est refusée par le cluster (preuve avec un test).
- [ ] La CI publie un SBOM et échoue sur une CVE critique.
- [ ] Au moins une app lit un secret dynamique depuis OpenBao.
