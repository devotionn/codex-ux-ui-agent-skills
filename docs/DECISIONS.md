# Architecture decisions

## ADR-001 — `AGENTS.md` is the Codex root contract

**Decision:** use a concise root contract and selective deeper references rather than copying the full upstream always-on brief into one file.

**Reason:** the design corpus is large; task-specific context should remain available without consuming every session's working context.

## ADR-002 — Keep objective gates deterministic

**Decision:** scripts/tests remain the authority for measurable checks. Agent prose cannot mark a gate passed.

**Reason:** reproducible checks are stronger than self-assessment.

## ADR-003 — Separate correctness from critique

**Decision:** accessibility/state/responsive/token gates and subjective design critique are separate stages.

**Reason:** a page can be mechanically correct and still be poor product design; subjective taste should not be disguised as deterministic scoring.

## ADR-004 — Preserve upstream provenance

**Decision:** record upstream baseline and attribution, and do not relabel upstream Claude eval output as Codex evidence.

**Reason:** evaluation provenance is part of the evidence.
