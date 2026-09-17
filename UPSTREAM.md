# Upstream tracking

Upstream: `plugin87/ux-ui-agent-skills`

Initial adaptation baseline: upstream release `v2.8.0` (observed 2026-09-17).

## Port policy

This repository is an adaptation, not a claim of independent authorship of the upstream design corpus. Preserve upstream attribution and the MIT notice for copied or substantially derived material.

Upstream changes should be classified before porting:

- **agent-agnostic knowledge** — normally port with minimal semantic change;
- **Claude Code loading/invocation** — translate to Codex-native instructions;
- **deterministic scripts/gates** — preserve behavior first, then change interfaces only with regression coverage;
- **examples/evals** — preserve provenance and do not rewrite historical evaluation outputs as if Codex produced them;
- **new upstream capabilities** — add only after identifying their Codex routing and verification contract.

Every future sync should record the upstream tag or commit used as the comparison baseline.
