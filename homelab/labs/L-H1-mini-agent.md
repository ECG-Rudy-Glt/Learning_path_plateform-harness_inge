🇫🇷 Français · [🇬🇧 English](L-H1-mini-agent.en.md)

# L-H1 — Mini-agent en ~200 lignes

**But** : écrire sa propre boucle sans framework, pour savoir ce que font Claude Code ou Codex sous le capot.

## Étapes
1. Python ou Go, SDK Anthropic, 3 outils : `read_file`, `run_command` (avec allowlist), `edit_file` (remplacement exact).
2. Boucle : appel → `tool_use` → exécution → `tool_result` (avec `is_error` si besoin) → répéter jusqu'à `end_turn` ou une limite de N tours.
3. Logger, à chaque tour, les tokens in/out, les tokens lus et écrits en cache, et le coût.
4. Tâche test : « ajoute un test unitaire manquant dans un petit repo jouet et fais-le passer ».
5. Faire varier la description des outils et observer l'effet sur le résultat.

## Livrable
Repo `mini-agent`, journal des expériences dans `notes/`.
