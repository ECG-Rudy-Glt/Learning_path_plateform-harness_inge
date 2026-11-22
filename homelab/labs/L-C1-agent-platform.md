🇫🇷 Français · [🇬🇧 English](L-C1-agent-platform.en.md)

# L-C1 — Agent platform sur k3s

**But** : fusionner L-P2, L-H5 et L-H4 en un service de plateforme.

```yaml
apiVersion: platform.homelab/v1alpha1
kind: AgentTask
spec:
  repo: rudy/sport-coach
  prompt: "Corrige l'issue #42"
  budget: { usd: 2, maxTurns: 80 }
  permissions: { write: pr-only }
```

## Étapes
1. Le contrôleur (extension de l'opérateur L-P2) crée un Pod sandbox (L-H5) et injecte des identifiants éphémères. Le résultat est une PR et un `status`.
2. Traces OTel GenAI → Collector → Tempo ou Loki. Dashboard Grafana du coût par tâche et par projet, et alerte en cas de budget dépassé.
3. CI du harness : toute modification de prompt ou d'outil relance le banc L-H4. Une régression bloque le merge.
4. Exposer le template « lancer un agent » dans Backstage (L-P4).

## Livrable
CRD `AgentTask` en prod lab, dashboard de coûts, gate d'évals en CI.
