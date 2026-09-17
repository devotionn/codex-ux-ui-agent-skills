# Phase 2 import plan

Phase 2 ports the upstream agent-agnostic knowledge layer before copying the full executable gate surface.

## Slice A — foundations

- token schema/examples and token rules
- accessibility references
- component anatomy/state contracts

Acceptance: Codex skills can point to real local references rather than only high-level contracts.

## Slice B — visual direction

- taste doctrine
- named design-system library
- design-system interoperability/crosswalk material

Acceptance: screen/redesign skills can select and justify a product-specific direction without loading the entire library.

## Slice C — implementation adapters

- framework adapters
- workflows
- starter/reference material needed by skills

Acceptance: a task can route from design intent into framework-native implementation guidance.

## Slice D — executable verification

Handled in Phase 4 after knowledge/skills stabilize: scripts, fixtures, tests, browser harnesses, and aggregate accuracy reporting.

## Port rule

Prefer coherent directory-level imports from the upstream baseline. Any adapted file that changes semantics should document why the Codex version differs.
