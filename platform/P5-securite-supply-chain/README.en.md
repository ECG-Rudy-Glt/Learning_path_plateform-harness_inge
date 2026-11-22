[🇫🇷 Français](README.md) · 🇬🇧 English

# P5 — Security, policy as code & supply chain

## Goals
- Sign images and verify signatures at admission.
- Generate SBOMs and scan for vulnerabilities in CI.
- Enforce default policies: no root, resource limits, allowed registries.
- Replace static secrets with short-lived dynamic secrets.

## Key concepts
SLSA levels, provenance, Sigstore (cosign, keyless, Rekor), SBOM (SPDX/CycloneDX), Kyverno / Gatekeeper, Pod Security Standards, External Secrets / Vault Agent, OpenBao dynamic secrets.

## Sources
- 🟢 [SLSA](https://slsa.dev/)
- 🟢 [Sigstore — cosign](https://docs.sigstore.dev/)
- 🟢 [Kyverno docs](https://kyverno.io/docs/)
- 🔵 [Kubernetes — Pod Security Standards](https://kubernetes.io/docs/concepts/security/pod-security-standards/)
- 🔵 [OpenBao docs](https://openbao.org/docs/)
- 🔵 [CNCF — Software Supply Chain Best Practices](https://github.com/cncf/tag-security/tree/main/community/working-groups/supply-chain-security/supply-chain-security-paper)
- 🎧 🇫🇷 [IFTTD #358 — DevSecOps, with Tugdual Grall (May 27, 2026)](https://www.ifttd.io/episodes/devsecops) (in French): why automation alone will not save security

## Practice
→ [L-P5 — Signed supply chain](../../homelab/labs/L-P5-supply-chain-signee.en.md)

## Validation
- [ ] An unsigned image is rejected by the cluster (proven with a test).
- [ ] CI publishes an SBOM and fails on a critical CVE.
- [ ] At least one app reads a dynamic secret from OpenBao.
