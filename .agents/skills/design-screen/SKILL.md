# Design Screen

## Use when

Creating a new product screen or materially restructuring an existing one.

## Procedure

1. Inspect product domain, route purpose, existing navigation, data contracts, framework, theme, and component library.
2. Identify the primary user task and the information hierarchy required to complete it.
3. Choose a visual direction consistent with the product rather than defaulting to generic AI-dashboard aesthetics.
4. Reuse existing primitives first; define missing component contracts before scattering one-off markup.
5. Implement semantic structure and responsive layout.
6. Cover loading, empty, error, partial-data, permission-restricted, and success states where the screen can encounter them.
7. Verify keyboard navigation, focus, semantics, contrast, target size, reduced motion, and responsive behavior.
8. Render at representative desktop and mobile widths when tooling permits.
9. Run deterministic gates, then perform a separate design critique.

## Failure conditions

Do not sacrifice existing product behavior for visual simplification. Do not claim responsive or visual correctness from source inspection alone when a runnable surface is available.
