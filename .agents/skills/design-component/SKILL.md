---
name: design-component
description: Design or materially redesign a reusable UI component. Use for buttons, inputs, tables, cards, dialogs, navigation, composite components, or other reusable interactions that need variants, states, token mapping, accessibility behavior, and implementation in an existing product stack.
---

# Design Component

## Inputs

- component purpose and user task
- existing framework and component library
- existing tokens/theme
- required variants and states
- accessibility constraints

## Load

Inspect neighboring components, shared primitives, theme/token files, and relevant accessibility or framework rules before implementation.

## Procedure

1. Inspect neighboring components and existing primitives.
2. Define anatomy and semantic role before visual styling.
3. Enumerate required variants and interaction states.
4. Map visual decisions to existing semantic/component tokens; introduce tokens only when the concept is reusable.
5. Implement using native project conventions.
6. Verify keyboard behavior, focus-visible behavior, accessible name/description, disabled/loading semantics, target size, contrast, reduced motion where relevant, and responsive behavior.
7. Render representative states when runtime tooling exists.
8. Report implementation and verification separately.

## Deliverables

- component implementation or design contract
- state/variant contract
- token mapping
- accessibility behavior
- tests or harness updates when appropriate

## Verification

Run the narrowest relevant tests and render representative default, interactive, disabled/loading, error, and responsive states when the runtime allows it.

## Failure conditions

Do not claim completion when required states are absent, when accessibility behavior is knowingly broken, or when a render-dependent claim was not rendered.
