[🇫🇷 Français](L-P5-supply-chain-signee.md) · 🇬🇧 English

# L-P5 — Signed supply chain

## Steps
1. Forgejo CI: build, SBOM (`syft`), scan (`grype` or `trivy`) that fails on a critical CVE, then `cosign` signature (key stored in OpenBao, or Transit).
2. Install Kyverno: verify signatures of internal-registry images, forbid `:latest`, require `runAsNonRoot` and limits. Start in `Audit`, then switch to `Enforce`.
3. Prove with a test that an unsigned image is rejected.
4. Replace an app's static secret with an OpenBao dynamic secret, for example a short-lived Postgres credential for patrimoine, through External Secrets or Vault Agent.

## Deliverable
Signed pipeline, policies in Enforce, rejection test, "dynamic secrets" ADR.
