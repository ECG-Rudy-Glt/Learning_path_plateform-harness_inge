🇫🇷 Français · [🇬🇧 English](README.en.md)

# P4 — Internal Developer Portal & golden paths

## Objectifs
- Mettre en place un catalogue logiciel : owners, dépendances, documentation.
- Offrir un golden path « nouvelle app → en prod » en moins de 15 min, sans ticket.
- Distinguer le portail (UI) de l'orchestrateur (backend de la plateforme).

## Concepts clés
Backstage (catalog, software templates, TechDocs, plugins), scorecards, modèle d'entités (Component, System, API, Resource), templates vs abstractions, Score.dev.

## Sources
- 🟢 [Backstage — le projet (GitHub, projet CNCF *incubating*)](https://github.com/backstage/backstage) : lire `ADOPTERS.md`, `plugins/` et `docs/`
- 🟢 [Backstage docs](https://backstage.io/docs/overview/what-is-backstage)
- 🟢 [Backstage — Software Templates](https://backstage.io/docs/features/software-templates/)
- 🔵 [Score specification](https://score.dev/)
- 🔵 [Spotify — How we use golden paths](https://engineering.atspotify.com/2020/08/how-we-use-golden-paths-to-solve-fragmentation-in-our-software-ecosystem)
- 📕 *Software Engineering at Google*, Winters, Manshreck & Wright ([gratuit en ligne](https://abseil.io/resources/swe-book)) : outillage partagé, build, CI à grande échelle

## Pratique
→ [L-P4 — Golden path & Backstage](../../homelab/labs/L-P4-golden-path-backstage.md)

## Validation
- [ ] Toutes les apps du homelab sont dans le catalogue, avec owner et lien vers le repo.
- [ ] Le template crée le repo, la CI, les manifestes et la Kustomization Flux, et l'app répond en HTTPS.
- [ ] J'ai chronométré le parcours et noté les frictions.
