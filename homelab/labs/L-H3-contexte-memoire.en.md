[🇫🇷 Français](L-H3-contexte-memoire.md) · 🇬🇧 English

# L-H3 — Context & memory of my agents

## Steps
1. Audit `HOMELAB/CLAUDE.md`, `~/.claude/CLAUDE.md` and the auto-memory: for each line, ask whether it is useful in every session, only on demand (move it into a skill), or never (delete it).
2. Measure RTK: the same typical session (Flux diagnosis) with and without the proxy, comparing tokens consumed and outcome.
3. Test compaction against a reset with a progress file, on a long task.
4. Listen again to [IFTTD #383](https://www.ifttd.io/episodes/contexte-engineering) and compare its recommendations with your setup, in writing.

## Deliverable
Slimmed-down CLAUDE.md (diff), RTK measurement, IFTTD reading note in `notes/`.
