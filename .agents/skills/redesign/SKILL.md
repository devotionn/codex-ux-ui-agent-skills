---
name: redesign
description: Redesign or modernize an existing UI while preserving its product behavior. Use for requests such as make this page cleaner, improve the dashboard, modernize the interface, fix hierarchy or density, or perform a visual overhaul without intentionally changing routes, data contracts, actions, validation, or analytics.
---

# Redesign

## Inputs

- target page, route, component, or flow
- current implementation and rendered state when available
- user pain points or design goals
- explicit behavior changes, if any

## Procedure

1. Inventory current behavior, routes, data, forms, actions, states, analytics hooks, and accessibility contracts.
2. Capture the existing rendered surface when possible before modifying it.
3. Diagnose problems by category: hierarchy, density, consistency, tokens, components, interaction, accessibility, responsive behavior, content, and visual direction.
4. Preserve functional contracts unless the brief explicitly changes them.
5. Prefer system-level corrections over isolated cosmetic patches.
6. Implement incrementally so regressions can be attributed.
7. Compare before/after behavior and render representative states.
8. Run available tests and gates.
9. Critique the redesigned result independently of whether gates pass.

## Deliverables

- concise diagnosis of the current UI
- implemented redesign or implementation-ready design specification
- before/after behavior notes
- verification evidence and remaining gaps

## Failure conditions

A redesign is not successful merely because it looks different. Missing functionality, inaccessible interactions, fabricated data, or removed states are regressions unless explicitly required by the brief.
