🇫🇷 Français · [🇬🇧 English](README.en.md)

# C2 — Agent d'exploitation du homelab

Un agent de triage d'incident, en **lecture seule d'abord**. Il sert de projet final : on y retrouve plateforme, harness, évals et sécurité.

## Objectifs
- L'agent reçoit une alerte, lit métriques, logs et état Flux, puis propose un diagnostic et un runbook.
- Les post-mortems existants (`HOMELAB/Documentation/postmortems/`) deviennent le **jeu d'évals** : l'agent retrouve-t-il la cause racine ?
- L'escalade se fait par paliers : lecture seule, puis proposition de PR, puis action avec approbation humaine.

## Sources
- 🟢 Google SRE book : chapitres *Effective Troubleshooting* et *Postmortem Culture*
- 🟢 H4 (évals) et H5 (permissions)
- 🔵 [Anthropic — Building effective agents](https://www.anthropic.com/engineering/building-effective-agents), pour savoir quand un workflow suffit

## Pratique
→ [L-C2 — Agent ops](../../homelab/labs/L-C2-agent-ops.md)
