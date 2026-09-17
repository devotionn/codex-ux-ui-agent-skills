# Design Review

## Use when

Reviewing an implemented UI for design quality after or alongside measurable correctness checks.

## Procedure

1. Render the actual surface when possible; do not review visual quality from source alone if a runnable UI exists.
2. Inspect representative desktop/mobile widths and supported themes.
3. Exercise important controls so feedback reflects real states, not only the initial frame.
4. Evaluate hierarchy, information density, affordance, consistency, content clarity, product/domain fit, responsive composition, and state communication.
5. Cross-check interaction behavior with established usability heuristics where relevant.
6. Cite concrete evidence for each material finding.
7. Separate measurable defects (for example contrast or clipping) from design judgment.
8. Recommend changes in priority order based on user impact and implementation leverage.

## Output

Use a findings table or equivalent structure with: severity/priority, evidence, why it matters, and recommended correction. Avoid fake precision scores for subjective taste.
