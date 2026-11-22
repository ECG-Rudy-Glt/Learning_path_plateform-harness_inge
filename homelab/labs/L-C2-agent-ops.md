🇫🇷 Français · [🇬🇧 English](L-C2-agent-ops.en.md)

# L-C2 — Agent de triage d'incident

## Étapes
1. Webhook Alertmanager → `AgentTask` (L-C1) en lecture seule : Prometheus, Loki, `flux get`, `kubectl describe`.
2. Sortie : diagnostic, preuves (requêtes exécutées) et runbook proposé, publié sur ntfy.
3. **Évals sur l'histoire réelle** : rejouer les 3 post-mortems (certificat non renouvelé, `terraform destroy` PBS, tempête OPNsense) sous forme de scénarios, et mesurer si l'agent trouve la cause racine.
4. Escalade par paliers : PR de correctif proposée, puis action après approbation humaine (bouton ntfy). Les actions destructrices ne sont jamais automatiques.

## Livrable
Agent ops en lecture seule actif, score sur les scénarios post-mortem, ADR « niveaux d'autonomie ».
