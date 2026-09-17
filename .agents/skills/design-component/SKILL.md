# Design Component

## Use when

Creating or materially redesigning a reusable UI component.

## Inputs

- component purpose and user task
- existing framework and component library
- existing tokens/theme
- required variants and states
- accessibility constraints

## Procedure

1. Inspect neighboring components and existing primitives.
2. Define anatomy and semantic role before visual styling.
3. Enumerate variants and interaction states.
4. Map visual decisions to existing semantic/component tokens; introduce tokens only when the concept is reusable.
5. Implement using native project conventions.
6. Verify keyboard behavior, focus-visible behavior, accessible name/description, disabled/loading semantics, target size, contrast, reduced motion where relevant, and responsive behavior.
7. Render representative states when runtime tooling exists.
8. Report implementation and verification separately.

## Deliverables

- component implementation
- state/variant contract
- token mapping
- accessibility behavior
- tests or harness updates when appropriate

## Failure conditions

Do not claim completion when required states are absent, when accessibility behavior is knowingly broken, or when a render-dependent claim was not rendered.
