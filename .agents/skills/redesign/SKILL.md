# Redesign

## Use when

Improving an existing UI without intentionally replacing its product behavior.

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

## Failure conditions

A redesign is not successful merely because it looks different. Missing functionality, inaccessible interactions, fabricated data, or removed states are regressions unless explicitly required by the brief.
