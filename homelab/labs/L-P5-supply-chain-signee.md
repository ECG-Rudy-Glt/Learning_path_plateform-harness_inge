🇫🇷 Français · [🇬🇧 English](L-P5-supply-chain-signee.en.md)

# L-P5 — Supply chain signée

## Étapes
1. CI Forgejo : build, SBOM (`syft`), scan (`grype` ou `trivy`) qui échoue sur une CVE critique, puis signature `cosign` (clé stockée dans OpenBao, ou Transit).
2. Installer Kyverno : vérifier les signatures des images du registre interne, interdire `:latest`, imposer `runAsNonRoot` et les limits. Démarrer en `Audit`, puis passer en `Enforce`.
3. Prouver le refus d'une image non signée avec un test.
4. Remplacer un secret statique d'app par un secret dynamique OpenBao, par exemple un identifiant Postgres à durée courte pour patrimoine, via External Secrets ou Vault Agent.

## Livrable
Pipeline signé, policies en Enforce, test de refus, ADR « secrets dynamiques ».
