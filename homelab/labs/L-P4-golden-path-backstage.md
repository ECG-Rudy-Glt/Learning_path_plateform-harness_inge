🇫🇷 Français · [🇬🇧 English](L-P4-golden-path-backstage.en.md)

# L-P4 — Golden path & Backstage

**But** : « nouvelle app → URL HTTPS en prod » en moins de 15 minutes, sans éditer le repo `HOMELAB` à la main.

## Étapes
1. Déployer [Backstage](https://github.com/backstage/backstage) dans `lab-backstage`, avec auth OIDC Authentik et base Postgres.
2. Écrire un `catalog-info.yaml` pour chaque app (patrimoine, sport-coach, freelance, media, speedtest) et l'infra (OpenBao, Flux, Prometheus).
3. Créer un Software Template qui crée le repo Forgejo depuis un squelette (Dockerfile, CI, `App` du lab L-P2), puis ouvre la PR Flux dans `HOMELAB`.
4. Publier TechDocs depuis `HOMELAB/Documentation`.
5. Chronométrer le parcours, et comparer avec la mesure faite en L-P1.

## Livrable
Backstage en ligne, catalogue complet, template fonctionnel, mesure avant/après.
