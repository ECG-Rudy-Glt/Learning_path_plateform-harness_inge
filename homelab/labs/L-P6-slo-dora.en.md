[🇫🇷 Français](L-P6-slo-dora.md) · 🇬🇧 English

# L-P6 — Homelab SLOs & DORA

## Steps
1. Define the SLIs for patrimoine and sport-coach: availability (Blackbox) and latency (Traefik metrics).
2. Generate the rules with Sloth: multi-window, multi-burn-rate alerts in Alertmanager.
3. Add an out-of-band alerting channel (ntfy, already self-hosted) to remove the "alerting depends on SMTP" limitation.
4. DORA: collect deployments (`deploy: images` commits + Flux events), lead time (commit → rollout) and failures (rollbacks, post-mortems). Build a Grafana dashboard.
5. Review the actions of the 3 existing post-mortems: which ones are closed?

## Deliverable
SLOs in prod, DORA dashboard, post-mortem action review.
