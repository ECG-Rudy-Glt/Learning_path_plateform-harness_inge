🇫🇷 Français · [🇬🇧 English](README.en.md)

# C1 — Une plateforme pour faire tourner des agents

Le harness devient un **produit de plateforme** : n'importe quel projet du homelab peut lancer un agent dans un environnement isolé, observé et budgété.

## Objectifs
- Proposer un CRD ou une API « AgentTask » : repo, consigne, budget, permissions.
- Lancer chaque tâche dans un sandbox éphémère, avec identifiants dynamiques.
- Tracer les appels LLM et outils avec les conventions OTel GenAI, et suivre le coût par tâche et par projet.
- Passer les évals du harness en CI avant chaque changement de prompt ou d'outil.

## Sources
- 🟢 [OpenTelemetry — GenAI semantic conventions](https://github.com/open-telemetry/semantic-conventions-genai) (déplacées hors du site principal vers ce dépôt)
- 🟢 [kubernetes-sigs/agent-sandbox](https://github.com/kubernetes-sigs/agent-sandbox) : `SandboxWarmPool` pour démarrer les agents sans attente
- 🔵 [IFTTD #383](https://www.ifttd.io/episodes/contexte-engineering) : passage du harness local à la CI
- 🔵 Tous les modules P2, P5, P6, H4 et H5
- 🟢 🎧 🇫🇷 [IFTTD #384 — Usine logicielle 100 % AI : qui réveille-t-on quand l'usine prend feu ?, avec Nikolay Rodionov (11 nov. 2026)](https://www.ifttd.io/episodes/usine-logicielle-100-ai) : agents en sandboxes éphémères, PR en volume, la revue comme goulot, construire un harnais fiable
- 🟢 🎧 🇫🇷 [IFTTD #382 — Rapprocher la CI : l'IA a 20x la cadence, nos CI doivent suivre, avec Yves Brissaud (28 oct. 2026)](https://www.ifttd.io/episodes/rapprocher-la-ci) : cache fin, parallélisme, exécution locale/distante hybride

## Pratique
→ [L-C1 — Agent platform sur k3s](../../homelab/labs/L-C1-agent-platform.md)
