🇫🇷 Français · [🇬🇧 English](README.en.md)

# H1 — API LLM & fondamentaux

## Objectifs
- Appeler un modèle par API : messages, système, streaming, tool use, prompt caching.
- Comprendre tokens, fenêtre de contexte, coûts et latence.
- Savoir pourquoi un modèle « hallucine » un appel d'outil, et comment le harness le rattrape.

## Concepts clés
Messages API, rôles, `tool_use` / `tool_result`, `stop_reason`, structured outputs, prompt caching, extended thinking, batch, rate limits, choix du modèle (coût / capacité).

## Sources
- 🟢 [Anthropic — Documentation API](https://docs.claude.com/)
- 🟢 [Anthropic — Tool use](https://docs.claude.com/en/docs/agents-and-tools/tool-use/overview)
- 🟢 [Anthropic — Building effective agents](https://www.anthropic.com/engineering/building-effective-agents) : workflows vs agents, à relire souvent
- 🔵 [Lilian Weng — LLM Powered Autonomous Agents](https://lilianweng.github.io/posts/2023-06-23-agent/)
- 🔵 [ReAct (Yao et al., 2022)](https://arxiv.org/abs/2210.03629)
- 📕 *AI Engineering: Building Applications with Foundation Models*, Chip Huyen (O'Reilly, janv. 2025)

## Pratique
→ [L-H1 — Mini-agent en ~200 lignes](../../homelab/labs/L-H1-mini-agent.md)

## Validation
- [ ] Je sais lire une réponse brute et dire pourquoi le modèle s'est arrêté.
- [ ] Mon script mesure les tokens et le coût de chaque tour.
- [ ] Le prompt caching est activé, et j'en ai mesuré le gain.
