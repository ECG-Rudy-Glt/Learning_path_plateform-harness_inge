[🇫🇷 Français](L-H6-agent-longue-duree.md) · 🇬🇧 English

# L-H6 — A long-running agent on a real project

**Goal**: first reproduce the initializer + coding agent pattern (Anthropic, Nov. 2025), then add the separate evaluator (Anthropic, Mar. 2026), on a real project from the backlog. A possible candidate: a feature from `patrimoine/TODO.md`, on a branch.

## Steps
1. Init session: spec, `features.json` (all `"passes": false`), `claude-progress.txt`, `init.sh` (start-up + tests), initial commit.
2. Work sessions: one feature at a time, commit, update `claude-progress.txt`, and **reset** the context between two sessions.
3. Then add a separate evaluator agent (scored criteria with a threshold, calibrated with few-shot examples, tests through Playwright), which accepts or rejects each feature (E2E tests, screenshots).
4. Compare with and without the evaluator, then test compaction against reset. Measure the number of sessions, cost, evaluator rejections and human rework.

## Deliverable
Feature delivered, versioned handoff artifacts, write-up in `notes/`.
