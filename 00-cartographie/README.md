🇫🇷 Français · [🇬🇧 English](README.en.md)

# 00 — Cartographie des rôles

## Platform Engineer

Construit et opère une **plateforme interne gérée comme un produit**. Elle réduit la charge cognitive des équipes applicatives grâce à des chemins pavés (golden paths) en self-service.

Les responsabilités types :
- l'API de la plateforme (CRD, templates, modules IaC) et son contrat avec les utilisateurs ;
- le provisioning (clusters, réseau, bases, secrets) par control planes déclaratifs ;
- la delivery (CI, GitOps, promotion entre environnements) ;
- des garde-fous par défaut (policy as code, supply chain signée, secrets) ;
- l'observabilité, les SLO, l'astreinte et les post-mortems ;
- la mesure de l'adoption et de la DevEx (DORA, SPACE, enquêtes).

## Harness Engineer

Conçoit **l'environnement autour d'un modèle** pour qu'un agent accomplisse un travail multi-étapes de façon fiable. La documentation est rédigée en français, mais le vocabulaire reste celui des sources, souvent anglais.

Les responsabilités types :
- la **boucle d'agent** : appels modèle, exécution d'outils, gestion des erreurs et des arrêts ;
- les **outils** : interface agent-machine (ACI), MCP, schémas, messages d'erreur utiles ;
- le **contexte** : prompt système, fichiers d'instructions, récupération, compaction, mémoire ;
- les **feedback loops** : tests, linters et vérificateurs que l'agent peut lancer lui-même ;
- les **évals** : jeux de tâches, graders, mesure de régression entre deux versions du harness ;
- le **sandboxing** : permissions, isolation du système de fichiers et du réseau, gestion des secrets ;
- le **long-running** : handoff entre sessions, artefacts de progression, orchestration multi-agent ;
- les **coûts et l'observabilité** : tokens, latence, traces des appels d'outils.

## Recouvrement

| Préoccupation | Côté plateforme | Côté harness |
|---|---|---|
| Interface | API de plateforme, CRD | Schémas d'outils, MCP |
| Garde-fous | Kyverno, RBAC, NetworkPolicy | Permissions d'outils, sandbox |
| Feedback | CI, preview envs | Tests et vérificateurs dans la boucle |
| Mesure | DORA, SLO | Évals, taux de réussite des tâches |
| Charge cognitive | Golden paths | Context engineering |
| Isolation | Namespaces, VM | gVisor, microVM, egress allowlist |

## Sources transverses

- 🟢 [CNCF — Platforms white paper](https://tag-app-delivery.cncf.io/whitepapers/platforms/)
- 🟢 [Thoughtworks — AI agent harness](https://www.thoughtworks.com/en-au/insights/blog/machine-learning-and-ai/ai-agent-harness)
- 🟢 [DigitalOcean — What is harness engineering?](https://www.digitalocean.com/resources/articles/what-is-harness-engineering)
- 🔵 [TechTarget — Agent harnesses as critical infrastructure](https://www.techtarget.com/it-infrastructure/tip/Harness-engineering-Agent-harnesses-as-critical-infrastructure)

## Exercice

Remplir la colonne « Départ » de l'auto-évaluation dans [PROGRESSION.md](../PROGRESSION.md). Ensuite, pour chaque ligne notée 2 ou moins, écrire en une phrase ce qui manque.
