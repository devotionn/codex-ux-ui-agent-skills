# Verification rules

## Evidence classes

Use explicit evidence labels internally and in final reports:

- **source-inspected** — inferred from code/configuration only;
- **test-verified** — exercised by automated tests;
- **render-verified** — observed in a real browser/runtime;
- **interaction-verified** — behavior exercised through user-like interaction.

Never upgrade one evidence class into another in reporting.

## Browser-dependent claims

Contrast against computed backgrounds, clipping, overflow, focus visibility, responsive reflow, pointer target geometry, interactive state transitions, and visual hierarchy generally require rendered evidence. If the environment cannot render the relevant surface, report the limitation.

## Gate behavior

A gate should be capable of rejecting a deliberately broken fixture. A check that cannot fail its negative fixture is not a trustworthy gate.

Unavailable prerequisites must not produce a false pass. Aggregate verification should distinguish pass, fail, and unavailable/required states.

## Design critique

Deterministic gates establish measurable correctness, not taste. Critique should cite observable evidence and should not convert subjective judgment into a fake numeric precision score.
