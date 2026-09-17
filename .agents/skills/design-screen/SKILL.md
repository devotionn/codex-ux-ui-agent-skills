---
name: design-screen
description: Design or materially restructure a product screen, route, dashboard, form, detail view, or workflow surface. Use when a task needs information hierarchy, layout, responsive composition, interaction states, product-fit visual direction, and implementation that preserves existing behavior and data contracts.
---

# Design Screen

## Inputs

- route or screen purpose
- primary user task
- existing navigation and neighboring screens
- framework, component library, and tokens
- data/API contracts and important product states
- visual or brand constraints, if present

## Load

Inspect the product domain, route implementation, existing navigation, data contracts, framework, theme, component library, and the smallest relevant design/accessibility rules.

## Procedure

1. Identify the primary user task and the information hierarchy required to complete it.
2. Inventory existing behavior and states before changing layout or interaction.
3. Choose a visual direction consistent with the product rather than defaulting to generic AI-dashboard aesthetics.
4. Reuse existing primitives first; define missing component contracts before scattering one-off markup.
5. Implement semantic structure and responsive layout.
6. Cover loading, empty, error, partial-data, permission-restricted, and success states where applicable.
7. Verify keyboard navigation, focus, semantics, contrast, target size, reduced motion, and responsive behavior.
8. Render at representative desktop and mobile widths when tooling permits.
9. Run deterministic gates, then perform a separate design critique.

## Deliverables

- screen implementation or implementation-ready specification
- hierarchy and layout decisions
- required state coverage
- reused/new component inventory
- verification evidence

## Failure conditions

Do not sacrifice existing product behavior for visual simplification. Do not claim responsive or visual correctness from source inspection alone when a runnable surface is available.
