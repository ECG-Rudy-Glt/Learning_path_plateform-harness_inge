🇫🇷 Français · [🇬🇧 English](L-H4-banc-evals.en.md)

# L-H4 — Banc d'évals sur tâches homelab

## Étapes
1. Écrire 20 tâches réalistes avec un état final vérifiable, par exemple :
   - « le pod X crashloop, trouve pourquoi » (incident injecté dans `lab-evals`) ;
   - « ajoute une règle Alertmanager pour Y » (validé par `promtool test rules`) ;
   - « corrige ce rôle Ansible pour que `ansible-lint` passe ».
2. Graders automatiques (tests, `kubectl`, lint), plus un LLM-judge calibré seulement là où c'est indispensable.
3. Lancer avec [Inspect AI](https://inspect.aisi.org.uk/) ou un runner maison, 3 répétitions par tâche, et calculer pass@1 et pass^3.
4. Comparer : mini-agent L-H1 contre Claude Code, puis MCP avant contre après L-H2.
5. Faire l'analyse d'erreurs : catégoriser les échecs en lisant les traces.

## Livrable
Repo `homelab-evals`, rapport comparatif, taxonomie d'échecs.
