---
name: ship
description: Run the final UI handoff or release-readiness pass for implemented product design work. Use when a UI change is believed ready for merge, handoff, demo, or release and needs diff review, relevant tests, rendered verification, responsive/state/accessibility checks, final critique, and an evidence-based completion report.
---

# Ship UI Work

## Procedure

1. Review the diff and confirm the requested behavior is present.
2. Run project tests relevant to changed code.
3. Run deterministic design/accessibility gates available in the repository.
4. Start the application and render changed surfaces when possible.
5. Exercise critical interactions and representative states.
6. Check narrow and desktop widths, light/dark modes when supported, keyboard operation, focus, loading/error/empty states, and destructive actions.
7. Perform a final adversarial critique after measurable checks pass.
8. Fix material defects and rerun affected verification.

## Report

Return four explicit sections: Implemented, Verified, Not verified, Remaining.

## Failure conditions

Never report skipped, unavailable, source-only, or inferred checks as passed.
