# Ship UI Work

## Use when

The implementation is believed to be ready for handoff, merge, or release.

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

Never report skipped, unavailable, or source-only checks as passed.
