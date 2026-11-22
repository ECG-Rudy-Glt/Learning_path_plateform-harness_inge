[🇫🇷 Français](L-P4-golden-path-backstage.md) · 🇬🇧 English

# L-P4 — Golden path & Backstage

**Goal**: "new app → HTTPS URL in prod" in under 15 minutes, without editing the `HOMELAB` repo by hand.

## Steps
1. Deploy [Backstage](https://github.com/backstage/backstage) into `lab-backstage`, with Authentik OIDC auth and a Postgres database.
2. Write a `catalog-info.yaml` for each app (patrimoine, sport-coach, freelance, media, speedtest) and for the infra (OpenBao, Flux, Prometheus).
3. Create a Software Template that creates the Forgejo repo from a skeleton (Dockerfile, CI, `App` from lab L-P2), then opens the Flux PR in `HOMELAB`.
4. Publish TechDocs from `HOMELAB/Documentation`.
5. Time the journey, and compare it with the measurement taken in L-P1.

## Deliverable
Backstage online, complete catalog, working template, before/after measurement.
