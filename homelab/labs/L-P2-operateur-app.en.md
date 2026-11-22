[🇫🇷 Français](L-P2-operateur-app.md) · 🇬🇧 English

# L-P2 — `App` operator for the homelab

**Goal**: replace the copy-pasted Deployment + Service + IngressRoute + Certificate of every app with **one high-level resource**.

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

## Steps
1. `kubebuilder init` in Go, `App` v1alpha1 CRD.
2. Reconcile: generate child resources with `ownerReferences`, and use Server-Side Apply.
3. Fill in `status.conditions` (Ready, Degraded) and add a finalizer if an external resource is created.
4. envtest tests, then deploy through Flux into `lab-operator`.
5. Migrate **one** low-criticality app (speedtest), without touching patrimoine.

## Deliverable
`platform-operator` repo on Forgejo, speedtest migrated, "App abstraction" ADR.
