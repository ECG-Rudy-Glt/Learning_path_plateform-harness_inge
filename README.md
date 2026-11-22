🇫🇷 Français · [🇬🇧 English](README.en.md)

# Learning path — Platform Engineer × Harness Engineer

Un dépôt pour **aligner les sources** et **pratiquer sur le homelab** afin de tenir deux rôles qui convergent :

| Rôle | Ce qu'on construit | Pour qui |
|---|---|---|
| **Platform Engineer** | Une plateforme interne en self-service (golden paths, IaC, GitOps, sécurité, observabilité) | Les développeurs, traités comme des clients |
| **Harness Engineer** | Le système autour d'un modèle : boucle d'agent, outils, contexte, évals, sandbox, reprise sur session longue | Les agents IA et les humains qui les pilotent |

**Pourquoi les deux ensemble ?** Un harness d'agent est une plateforme dont l'utilisateur est un modèle. Les mêmes réflexes s'appliquent aux deux : interfaces stables, garde-fous déclaratifs, feedback loops rapides, isolation, observabilité, mesure. Le module [convergence/](convergence/) en tire les conséquences : faire tourner des agents *sur* la plateforme.

## Organisation

```
00-cartographie/      Définitions des rôles, matrice de compétences, auto-évaluation
platform/   P1 → P6   Track Platform Engineering
harness/    H1 → H6   Track Harness Engineering (agents IA)
convergence/ C1 → C2  Plateforme pour agents, agent d'exploitation
homelab/              Labs pratiques sur le cluster k3s / Proxmox existant
notes/                Fiches de lecture (template fourni)
PROGRESSION.md        Suivi coché de l'avancement
BIBLIOGRAPHIE.md      Toutes les sources, vérifiées et datées
```

📚 **[Bibliographie complète](BIBLIOGRAPHIE.md)** : livres, articles, docs, podcasts et dépôts, avec auteur, date et module.

Chaque module suit le même format :

1. **Objectifs**, ce que tu sais faire à la fin
2. **Concepts clés**
3. **Sources** : 🟢 essentiel (à lire en premier), 🔵 approfondir, 📕 livre
4. **Pratique**, avec un lien vers le lab homelab correspondant
5. **Validation** : la checklist qui dit si le module est acquis

## Parcours conseillé

Les deux tracks avancent **en parallèle** (une semaine Platform, une semaine Harness), puis convergent.

```
Mois 1   P1 Platform as product      H1 API LLM & fondamentaux
Mois 2   P2 K8s & GitOps avancé       H2 Boucle d'agent & outils (MCP)
Mois 3   P3 IaC & control planes      H3 Context engineering
Mois 4   P4 IDP & golden paths        H4 Évals
Mois 5   P5 Sécurité & supply chain   H5 Sandboxing & sécurité agents
Mois 6   P6 Observabilité & SRE       H6 Long-running & multi-agent
Mois 7+  C1 Plateforme pour agents → C2 Agent d'exploitation du homelab
```

Le point de départ est un profil déjà opérationnel : homelab en IaC (Terraform, Ansible, Flux), PKI, OpenBao, post-mortems. Les fondamentaux Linux, réseau et Git ne sont donc pas couverts. Le parcours vise l'**abstraction** (en faire un produit) et l'**automatisation par agents**.

## Règles du dépôt

- Une source n'entre que si elle a été lue, ou si elle est marquée `à lire`. Pas de liste de liens morte.
- Chaque lecture importante donne une fiche dans `notes/` (voir [notes/_template.md](notes/_template.md)).
- Chaque lab terminé laisse une trace vérifiable : PR dans `HOMELAB`, ADR ou post-mortem.

## Langue

Chaque document existe en français (`README.md`) et en anglais (`README.en.md`). La bibliographie est `BIBLIOGRAPHIE.md` / `BIBLIOGRAPHY.md`.
