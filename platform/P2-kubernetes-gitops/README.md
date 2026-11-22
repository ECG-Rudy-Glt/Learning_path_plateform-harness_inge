🇫🇷 Français · [🇬🇧 English](README.en.md)

# P2 — Kubernetes en profondeur & GitOps avancé

## Objectifs
- Comprendre le modèle de contrôleur : reconcile loop, informers, finalizers, status.
- Écrire un opérateur avec kubebuilder.
- Structurer Flux pour plusieurs tenants : multi-sources, dépendances, promotion.

## Concepts clés
API machinery, CRD et versions, admission webhooks, Server-Side Apply, réconciliation idempotente, Flux Kustomization / HelmRelease / dependsOn, image automation, multi-tenancy (impersonation, ServiceAccount par tenant).

## Sources
- 🟢 [Kubebuilder Book](https://book.kubebuilder.io/)
- 🟢 [Flux — Ways of structuring your repositories](https://fluxcd.io/flux/guides/repository-structure/)
- 🟢 [fluxcd/flux2-multi-tenancy](https://github.com/fluxcd/flux2-multi-tenancy), l'exemple de référence cité par la doc Flux
- 🔵 [Flux — Multi-tenancy lockdown](https://fluxcd.io/flux/installation/configuration/multitenancy/)
- 🟢 [Kubernetes docs — Controllers](https://kubernetes.io/docs/concepts/architecture/controller/)
- 🔵 [Kubernetes The Hard Way](https://github.com/kelseyhightower/kubernetes-the-hard-way)
- 🔵 [OpenGitOps principles](https://opengitops.dev/)
- 📕 *Programming Kubernetes*, Hausenblas & Schimanski (O'Reilly, 2019)
- 🎓 CKA puis CKS (certifications, en option)
- 🔵 [Large-scale cluster management at Google with Borg](https://research.google/pubs/large-scale-cluster-management-at-google-with-borg/) (Verma et al., EuroSys 2015) : l'ancêtre direct de Kubernetes
- 📕 *Kubernetes Patterns*, Bilgin Ibryam & Roland Huß ([k8spatterns.com](https://k8spatterns.com/))

## Pratique
→ [L-P2 — Opérateur `App` pour le homelab](../../homelab/labs/L-P2-operateur-app.md)

## Validation
- [ ] Je sais expliquer ce qui se passe entre `kubectl apply` et le démarrage du pod.
- [ ] Mon opérateur gère création, mise à jour et suppression (finalizer), et remplit `status.conditions`.
- [ ] Flux du homelab : un tenant ne peut pas écrire hors de son namespace.
