🇫🇷 Français · [🇬🇧 English](L-P2-operateur-app.en.md)

# L-P2 — Opérateur `App` pour le homelab

**But** : remplacer le copier-coller Deployment + Service + IngressRoute + Certificate de chaque app par **une ressource de haut niveau**.

```yaml
apiVersion: platform.homelab/v1alpha1
kind: App
metadata: { name: speedtest, namespace: speedtest }
spec:
  image: registry.example/speedtest:1.2.0
  port: 8080
  host: speedtest.lan
  auth: authentik        # none | authentik
  resources: small       # small | medium
```

## Étapes
1. `kubebuilder init` en Go, CRD `App` v1alpha1.
2. Reconcile : générer les ressources enfants avec `ownerReferences`, et utiliser Server-Side Apply.
3. Remplir `status.conditions` (Ready, Degraded) et ajouter un finalizer si une ressource externe est créée.
4. Tests envtest, puis déploiement via Flux dans `lab-operator`.
5. Migrer **une** app peu critique (speedtest), sans toucher patrimoine.

## Livrable
Repo `platform-operator` sur Forgejo, migration de speedtest, ADR « abstraction App ».
