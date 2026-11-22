[🇫🇷 Français](README.md) · 🇬🇧 English

# Learning path — Platform Engineer × Harness Engineer

A repository to **line up the sources** and **practice on the homelab**, in order to hold two roles that are converging:

| Role | What you build | For whom |
|---|---|---|
| **Platform Engineer** | A self-service internal platform (golden paths, IaC, GitOps, security, observability) | Developers, treated as customers |
| **Harness Engineer** | The system around a model: agent loop, tools, context, evals, sandbox, recovery across long sessions | AI agents and the humans who steer them |

**Why both together?** An agent harness is a platform whose user is a model. The same reflexes apply to both: stable interfaces, declarative guardrails, fast feedback loops, isolation, observability, measurement. The [convergence/](convergence/) track draws the consequences: running agents *on* the platform.

## Layout

```
00-cartographie/      Role definitions, skills matrix, self-assessment
platform/   P1 → P6   Platform Engineering track
harness/    H1 → H6   Harness Engineering track (AI agents)
convergence/ C1 → C2  Platform for agents, operations agent
homelab/              Hands-on labs on the existing k3s / Proxmox cluster
notes/                Reading notes (template provided)
PROGRESSION.md        Progress checklist
BIBLIOGRAPHY.md       Every source, verified and dated
```

📚 **[Full bibliography](BIBLIOGRAPHY.md)**: books, articles, docs, podcasts and repositories, with author, date and module.

Every module follows the same format:

1. **Goals**: what you can do at the end
2. **Key concepts**
3. **Sources**: 🟢 essential (read first), 🔵 go deeper, 📕 book
4. **Practice**, with a link to the matching homelab lab
5. **Validation**: the checklist that tells you the module is done

## Suggested path

The two tracks run **in parallel** (one week Platform, one week Harness), then converge.

```
Month 1   P1 Platform as product      H1 LLM API & fundamentals
Month 2   P2 K8s & advanced GitOps    H2 Agent loop & tools (MCP)
Month 3   P3 IaC & control planes     H3 Context engineering
Month 4   P4 IDP & golden paths       H4 Evals
Month 5   P5 Security & supply chain  H5 Agent sandboxing & security
Month 6   P6 Observability & SRE      H6 Long-running & multi-agent
Month 7+  C1 Platform for agents → C2 Homelab operations agent
```

The starting point is someone already operational: a homelab in IaC (Terraform, Ansible, Flux), PKI, OpenBao, post-mortems. Linux, networking and Git fundamentals are therefore not covered. The path targets **abstraction** (turning it into a product) and **automation through agents**.

## Repository rules

- A source only goes in once it has been read, or if it is tagged `to read`. No dead link lists.
- Every important read produces a note in `notes/` (see [notes/_template.en.md](notes/_template.en.md)).
- Every finished lab leaves a verifiable trace: a PR in `HOMELAB`, an ADR or a post-mortem.

## Language

Each document exists in French (`README.md`) and English (`README.en.md`). The bibliography is `BIBLIOGRAPHIE.md` / `BIBLIOGRAPHY.md`.
