---
name: product-design
description: Orchestrate end-to-end product UI/UX work in Codex and serve as the default team entry point. Use for requests such as design a page, improve or redesign UI, implement from a brief or screenshot, review an interface, refine a component, apply a design system, or prepare UI work for handoff. Routes to the narrow design skills while preserving product behavior, accessibility, responsiveness, design-system consistency, rendered verification, and evidence-based reporting.
---

# Product Design Orchestrator

Use this as the default entry point for designers and product teams. The user should not need to know which narrow skill applies.

## Operating modes

Infer the mode from the request. Do not ask the user to choose a mode unless the distinction materially changes the requested outcome.

- **Design only** — analyze and produce an implementation-ready UI/UX specification; do not edit code when the user explicitly asks for concepts, review, or design guidance only.
- **Design + implementation** — inspect the product, implement the requested UI change, render it, verify behavior, and report evidence.
- **Review only** — inspect/render the current UI and return prioritized findings without changing code unless the user asks for fixes.

## Start here

1. Read the nearest applicable `AGENTS.md` files and inspect the target repository before proposing visual changes.
2. Identify the product/domain, primary user task, target surface, framework, component library, token/theme system, data contracts, and existing behavior.
3. Prefer evidence in the repository over assumptions. If brand/design-system guidance exists, treat it as a constraint.
4. If information is missing, infer low-risk reversible choices from neighboring product surfaces. Ask only when a missing decision would materially change product behavior, brand direction, or irreversible architecture.

## Route to the smallest useful skill set

Load only the relevant sibling skills when they are available:

- reusable component → `design-component`
- new screen or major screen structure → `design-screen`
- existing UI modernization → `redesign`
- token work → `design-tokens`
- cross-product system work → `design-system`
- accessibility-focused audit → `accessibility-audit`
- critique / design QA → `design-review`
- interface copy → `ux-writing`
- motion → `motion-spec`
- final implementation handoff → `ship`

For broad feature work, the default chain is usually:

`design-screen` or `redesign` → relevant component/token work → `accessibility-audit` where material → `design-review` → `ship`.

Do not load every skill by default. Keep context narrow.

## Design workflow

1. **Inspect** — map existing behavior, data, states, navigation, components, tokens, and constraints.
2. **Frame** — state the primary user task and the main hierarchy/interaction problem in a few lines.
3. **Direction** — choose a product-specific visual and interaction direction; avoid generic AI-dashboard defaults.
4. **Systemize** — reuse existing tokens/components first. Introduce reusable primitives only when the need is repeated or structurally important.
5. **Implement or specify** — preserve routes, data contracts, validation, permissions, analytics, and accessibility behavior unless the brief explicitly changes them.
6. **Cover states** — include loading, empty, partial, error, disabled, permission-restricted, success, and destructive states when relevant.
7. **Verify** — render representative widths/states, exercise important controls, run relevant tests/gates, and distinguish verified facts from inference.
8. **Critique** — separately review hierarchy, density, affordance, consistency, content clarity, responsive composition, and product/domain fit.
9. **Close** — fix material issues, rerun affected checks, and provide a concise handoff.

## Team design rules

- Preserve working business logic unless the user explicitly requests a behavior change.
- Never fabricate production data, successful actions, permissions, or system states for the sake of a prettier demo.
- Prefer the product's existing component library and stack. Do not introduce a second design system without a concrete reason.
- Accessibility is part of design quality, not a final cosmetic audit. Target the repository's stated standard; otherwise use WCAG 2.2 AA as the baseline.
- Treat responsive behavior and interaction states as first-class deliverables.
- Avoid gratuitous gradients, uniform card grids with no hierarchy, excessive pills, fake glassmorphism, emoji-as-icons, arbitrary hardcoded values, and motion without interaction purpose unless the product context specifically calls for them.
- Do not claim visual correctness from source inspection alone when the product can be rendered.

## Handoff format

For implemented work, end with:

- **Implemented** — what changed and where.
- **Verified** — tests, rendered states, widths, interactions, and gates actually checked.
- **Not verified** — checks that were unavailable or intentionally skipped.
- **Remaining** — known defects, design debt, or decisions requiring owner input.

For design-only work, end with:

- **Direction** — the design decision and rationale.
- **Structure** — hierarchy/layout/component plan.
- **States & accessibility** — important state and a11y requirements.
- **Handoff** — implementation notes and any unresolved owner decisions.

## Failure conditions

Do not treat visual novelty as success. A result is not complete if it removes required behavior, hides missing states, breaks accessibility, ignores the existing product system without reason, or reports unverified claims as passed.
