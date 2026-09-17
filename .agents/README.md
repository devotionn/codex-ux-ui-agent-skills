# `.agents` architecture

This directory contains the Codex-facing instruction layer.

## `skills/`

Each skill should be narrowly scoped, composable, and explicit about inputs, outputs, required context, verification, and failure conditions.

Planned initial skills:

- `design-component`
- `design-screen`
- `design-system`
- `design-tokens`
- `accessibility-audit`
- `design-review`
- `redesign`
- `image-to-code`
- `data-dashboard`
- `brandkit`
- `ux-writing`
- `motion-spec`
- `ship`

## `rules/`

Deeper always-reusable rules loaded on demand: tokens/color, typography/spacing, components/states, accessibility, responsive behavior, framework conventions, taste, review, and verification.

## Skill contract

Every skill should define:

1. **Use when** — routing criteria.
2. **Inputs** — required and optional context.
3. **Load** — repository references to inspect.
4. **Procedure** — deterministic sequence where possible.
5. **Deliverables** — concrete files/artifacts expected.
6. **Verification** — gates/tests/browser checks.
7. **Failure conditions** — what must not be represented as success.

The port should preserve useful upstream semantics while removing assumptions that depend specifically on Claude Code plugin loading.
