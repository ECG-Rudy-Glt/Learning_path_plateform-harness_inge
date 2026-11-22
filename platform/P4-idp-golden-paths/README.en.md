[🇫🇷 Français](README.md) · 🇬🇧 English

# P4 — Internal Developer Portal & golden paths

## Goals
- Set up a software catalog: owners, dependencies, documentation.
- Offer a "new app → in prod" golden path in under 15 minutes, with no ticket.
- Tell the portal (UI) apart from the orchestrator (platform backend).

## Key concepts
Backstage (catalog, software templates, TechDocs, plugins), scorecards, entity model (Component, System, API, Resource), templates vs abstractions, Score.dev.

## Sources
- 🟢 [Backstage — the project (GitHub, CNCF *incubating* project)](https://github.com/backstage/backstage): read `ADOPTERS.md`, `plugins/` and `docs/`
- 🟢 [Backstage docs](https://backstage.io/docs/overview/what-is-backstage)
- 🟢 [Backstage — Software Templates](https://backstage.io/docs/features/software-templates/)
- 🔵 [Score specification](https://score.dev/)
- 🔵 [Spotify — How we use golden paths](https://engineering.atspotify.com/2020/08/how-we-use-golden-paths-to-solve-fragmentation-in-our-software-ecosystem)
- 📕 *Software Engineering at Google*, Winters, Manshreck & Wright ([free online](https://abseil.io/resources/swe-book)): shared tooling, build, CI at scale

## Practice
→ [L-P4 — Golden path & Backstage](../../homelab/labs/L-P4-golden-path-backstage.en.md)

## Validation
- [ ] Every homelab app is in the catalog, with an owner and a link to its repo.
- [ ] The template creates the repo, the CI, the manifests and the Flux Kustomization, and the app answers over HTTPS.
- [ ] I have timed the journey and noted the friction points.
