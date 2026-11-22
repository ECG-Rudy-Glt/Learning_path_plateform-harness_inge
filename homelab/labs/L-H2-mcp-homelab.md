🇫🇷 Français · [🇬🇧 English](L-H2-mcp-homelab.en.md)

# L-H2 — Serveur MCP du homelab & skills

**But** : revoir le serveur MCP homelab existant avec les principes de [Writing effective tools for agents](https://www.anthropic.com/engineering/writing-tools-for-agents).

## Étapes
1. Inventorier les outils exposés : nom, description, granularité, taille des réponses.
2. Pour chaque outil, vérifier : est-il nommé par intention ? les réponses sont-elles paginées ou tronquées ? les erreurs sont-elles actionnables ? les opérations dangereuses sont-elles séparées ?
3. Ajouter des outils de haut niveau (`app_status(app)`, qui agrège pods, Flux et dernier déploiement) plutôt que d'exposer `kubectl` brut.
4. Mettre le MCP derrière Authentik, avec des scopes read et write séparés.
5. Écrire 2 skills perso (ex. `homelab-deploy-check`, qui suit la mémoire « vérifier le rollout avant d'annoncer », et `postmortem`), en t'inspirant de la structure de [mattpocock/skills](https://github.com/mattpocock/skills).

## Livrable
MCP refactoré, avant/après mesuré sur 5 tâches, 2 skills dans `~/.claude/skills`.
