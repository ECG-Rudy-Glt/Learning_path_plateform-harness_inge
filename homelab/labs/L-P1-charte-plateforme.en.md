[🇫🇷 Français](L-P1-charte-plateforme.md) · 🇬🇧 English

# L-P1 — Homelab platform charter

**Goal**: treat the homelab as a product whose users are: me as a developer, the family members who use the apps every day, freelance clients, and soon agents.

## Steps
1. List the personas and, for each one, the current journey: how does an app reach prod today? Time how long it took to add the last app (sport-coach or freelance).
2. Assess each aspect of the [CNCF maturity model](https://tag-app-delivery.cncf.io/whitepapers/platform-eng-maturity-model/) (Investment, Adoption, Interfaces, Operations, Measurement) with evidence.
3. Write `HOMELAB/Documentation/plateforme/charte.md`: mission, scope, contract (what the platform guarantees), out of scope, metrics.
4. Choose 3 metrics and their source (e.g. time to onboard an app, Flux deploy frequency, number of manual steps in `DID.md`).

## Deliverable
Charter + maturity table, as a PR in `HOMELAB`.
