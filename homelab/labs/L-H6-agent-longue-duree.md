🇫🇷 Français · [🇬🇧 English](L-H6-agent-longue-duree.en.md)

# L-H6 — Agent longue durée sur un vrai projet

**But** : reproduire d'abord le schéma initializer + coding agent (Anthropic, nov. 2025), puis ajouter l'évaluateur séparé (Anthropic, mars 2026), sur un projet réel du backlog. Candidat possible : une feature du `patrimoine/TODO.md`, sur une branche.

## Étapes
1. Session d'init : spec, `features.json` (toutes `"passes": false`), `claude-progress.txt`, `init.sh` (démarrage + tests), commit initial.
2. Sessions de travail : une feature à la fois, commit, mise à jour de `claude-progress.txt`, et **reset** du contexte entre deux sessions.
3. Ajouter ensuite un agent évaluateur séparé (critères notés avec seuil, calibrés par few-shot, tests via Playwright), qui valide ou rejette chaque feature (tests E2E, captures).
4. Comparer avec et sans évaluateur, puis tester compaction contre reset. Mesurer le nombre de sessions, le coût, les rejets de l'évaluateur et les retouches humaines.

## Livrable
Feature livrée, artefacts de handoff versionnés, retour d'expérience dans `notes/`.
