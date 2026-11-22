[🇫🇷 Français](README.md) · 🇬🇧 English

# P2 — Kubernetes in depth & advanced GitOps

## Goals
- Understand the controller model: reconcile loop, informers, finalizers, status.
- Write an operator with kubebuilder.
- Structure Flux for several tenants: multiple sources, dependencies, promotion.

## Key concepts
API machinery, CRDs and versions, admission webhooks, Server-Side Apply, idempotent reconciliation, Flux Kustomization / HelmRelease / dependsOn, image automation, multi-tenancy (impersonation, one ServiceAccount per tenant).

## Sources
- 🟢 [Kubebuilder Book](https://book.kubebuilder.io/)
- 🟢 [Flux — Ways of structuring your repositories](https://fluxcd.io/flux/guides/repository-structure/)
- 🟢 [fluxcd/flux2-multi-tenancy](https://github.com/fluxcd/flux2-multi-tenancy), the reference example cited by the Flux docs
- 🔵 [Flux — Multi-tenancy lockdown](https://fluxcd.io/flux/installation/configuration/multitenancy/)
- 🟢 [Kubernetes docs — Controllers](https://kubernetes.io/docs/concepts/architecture/controller/)
- 🔵 [Kubernetes The Hard Way](https://github.com/kelseyhightower/kubernetes-the-hard-way)
- 🔵 [OpenGitOps principles](https://opengitops.dev/)
- 📕 *Programming Kubernetes*, Hausenblas & Schimanski (O'Reilly, 2019)
- 🎓 CKA then CKS (certifications, optional)
- 🔵 [Large-scale cluster management at Google with Borg](https://research.google/pubs/large-scale-cluster-management-at-google-with-borg/) (Verma et al., EuroSys 2015): Kubernetes' direct ancestor
- 📕 *Kubernetes Patterns*, Bilgin Ibryam & Roland Huß ([k8spatterns.com](https://k8spatterns.com/))

## Practice
→ [L-P2 — `App` operator for the homelab](../../homelab/labs/L-P2-operateur-app.en.md)

## Validation
- [ ] I can explain what happens between `kubectl apply` and the pod starting.
- [ ] My operator handles create, update and delete (finalizer), and fills in `status.conditions`.
- [ ] Homelab Flux: a tenant cannot write outside its namespace.
