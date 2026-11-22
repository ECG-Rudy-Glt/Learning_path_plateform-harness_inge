🇫🇷 Français · [🇬🇧 English](L-P6-slo-dora.en.md)

# L-P6 — SLO & DORA du homelab

## Étapes
1. Définir les SLI de patrimoine et sport-coach : disponibilité (Blackbox) et latence (Traefik metrics).
2. Générer les règles avec Sloth : alertes multi-window multi-burn-rate dans Alertmanager.
3. Ajouter un canal d'alerte hors bande (ntfy, déjà auto-hébergé) pour lever la limite « alerting dépendant du SMTP ».
4. DORA : collecter les déploiements (commits `deploy: images` + événements Flux), le lead time (commit → rollout) et les échecs (rollbacks, post-mortems). Construire un dashboard Grafana.
5. Revoir les actions des 3 post-mortems existants : lesquelles sont fermées ?

## Livrable
SLO en prod, dashboard DORA, revue des actions post-mortem.
