🇫🇷 Français · [🇬🇧 English](L-H5-sandbox-k3s.en.md)

# L-H5 — Sandbox d'agent sur k3s

## Étapes
1. Installer gVisor (`runsc`) sur le worker k3s, puis créer une `RuntimeClass` gvisor.
2. Créer le namespace `lab-agents` : Pod Security `restricted`, NetworkPolicy par défaut deny, egress autorisé uniquement vers l'API du modèle et Forgejo (via proxy ou FQDN policy).
3. Pour les identifiants, s'authentifier à OpenBao avec la ServiceAccount (auth kubernetes), et obtenir un token Forgejo à périmètre repo avec TTL de 1 h.
4. Red-team : faire lire à l'agent un README piégé (prompt injection) qui tente d'exfiltrer un secret. Documenter ce qui bloque, et ce qui passe.
5. Évaluer [agent-sandbox](https://github.com/kubernetes-sigs/agent-sandbox) comme alternative.

## Livrable
Manifestes Flux `lab-agents`, rapport red-team, ADR « isolation des agents ».
