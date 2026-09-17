# Port Roadmap

## Phase 1 — Codex foundation

- [x] Codex-native `AGENTS.md`
- [x] `.agents/` skill architecture
- [x] initial `design-component` skill
- [x] initial `accessibility-audit` skill
- [x] upstream attribution and MIT license preservation
- [ ] inventory all upstream Claude-specific loading/invocation assumptions
- [ ] define compatibility policy for upstream updates

## Phase 2 — Knowledge layer

- [ ] tokens
- [ ] components
- [ ] accessibility
- [ ] taste / anti-slop doctrine
- [ ] design-system library
- [ ] framework adapters
- [ ] workflows

## Phase 3 — Codex skills

Port and adapt the upstream skill set. Preserve semantics where they are agent-agnostic; rewrite Claude-specific invocation and context-loading assumptions.

## Phase 4 — Gates

Port objective checks and prove they reject known-bad fixtures. Browser-backed checks must fail honestly when browser prerequisites are missing.

## Phase 5 — Cold-start evaluation

Run representative briefs from clean Codex sessions and evaluate the produced artifacts independently. Record provenance and distinguish deterministic correctness from subjective critique.
