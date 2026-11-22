[🇫🇷 Français](README.md) · 🇬🇧 English

# P6 — Observability & SRE

## Goals
- Define SLIs/SLOs, error budgets and multi-burn-rate alerts.
- Instrument with OpenTelemetry (traces, metrics, logs).
- Measure DORA on your own delivery.
- Write blameless post-mortems and turn them into actions.

## Key concepts
SLI/SLO/SLA, burn rate, alerting on symptoms rather than causes, OTel Collector, RED/USE, cardinality, DORA (deployment frequency, lead time, change failure rate, time to restore).

## Sources
- 🟢 [Google SRE books (online, free)](https://sre.google/books/), starting with the SLO, Alerting on SLOs and Postmortem Culture chapters
- 🟢 [OpenTelemetry docs](https://opentelemetry.io/docs/)
- 🔵 [Sloth — Prometheus SLO generation](https://sloth.dev/)
- 🔵 [DORA metrics guide](https://dora.dev/guides/dora-metrics-four-keys/)
- 📕 *Observability Engineering*, Majors, Fong-Jones & Miranda (O'Reilly, 2022; 2nd ed. with chapters on LLMs)
- 🎧 🇫🇷 [IFTTD #355 — SRE et DevOps, with Kevin Davin (May 6, 2026)](https://www.ifttd.io/episodes/sre-et-devops) (in French): error budgets, declarative model, shared run responsibility

## Practice
→ [L-P6 — Homelab SLOs & DORA](../../homelab/labs/L-P6-slo-dora.en.md)

## Validation
- [ ] 2 apps have SLOs with burn-rate alerts.
- [ ] A DORA dashboard is fed by Forgejo and Flux.
- [ ] The latest post-mortem has actions tracked through to closure.
