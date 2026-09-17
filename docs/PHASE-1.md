# Phase 1 — Codex foundation

Phase 1 establishes the instruction architecture before bulk-porting upstream content.

## Implemented

- root `AGENTS.md` as the Codex entry contract and request router;
- `.agents/skills/` contract and initial component, screen, redesign, accessibility-audit, and ship skills;
- `.agents/rules/verification.md` defining source/test/render/interaction evidence classes;
- upstream attribution, MIT preservation, sync policy, and Claude→Codex mapping;
- staged roadmap for knowledge, skills, gates, and Codex cold-start evals.

## Why foundation first

The upstream project currently exposes 19 runnable skills and 44 objective gates, with 31 checks requiring a real browser. Its repository also separates tokens, components, accessibility, design systems, frameworks, taste, workflows, scripts, tests, evals, and examples. A faithful Codex adaptation therefore needs selective context loading and honest verification rather than a single giant prompt.

## Phase 1 exit criteria

- [x] Codex has a clear root instruction entry point.
- [x] Skills have a repeatable contract.
- [x] Render-dependent claims cannot silently become source-only claims.
- [x] Upstream authorship and license are explicit.
- [x] Claude-specific concepts have documented Codex mappings.
- [ ] Full upstream inventory is captured during Phase 2 import preparation.

Next: import the agent-agnostic knowledge layer in coherent slices and keep upstream paths/history traceable.
