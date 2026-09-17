# Skills index

These are repository-scoped Codex skills using the current `SKILL.md` format with YAML `name` and `description` metadata for discovery and triggering.

## Default team entry point

- `product-design` — broad product UI/UX orchestration for designers and product teams. Use this when the user should not need to choose a specialist workflow.

## Specialist skills

- `design-component`
- `design-screen`
- `redesign`
- `design-tokens`
- `design-system`
- `accessibility-audit`
- `design-review`
- `ux-writing`
- `motion-spec`
- `ship`

## Routing principle

Prefer the smallest useful skill set. Broad UI work should normally start with `product-design`, which then loads only the specialist instructions needed for the task.

These skills are the orchestration layer, not the complete upstream knowledge port. As the knowledge layer lands, keep large references outside `SKILL.md` and load them progressively.

See `docs/TEAM_USAGE.md` for company/team rollout and designer-facing examples.
