# Accessibility Audit

## Use when

Auditing a page, component, flow, or design system for accessibility.

## Procedure

1. Prefer rendered inspection over source-only inference when runtime/browser access exists.
2. Check semantic structure, names/roles/values, heading hierarchy, landmarks, labels and descriptions.
3. Check full keyboard operation, focus order, focus visibility, traps, and escape behavior.
4. Check text/non-text contrast and state-specific contrast against the project's target WCAG level.
5. Check pointer target sizing and alternatives to drag/gesture-only interactions.
6. Check errors, status messages, loading states, validation, and dynamic announcements.
7. Check reduced motion and content that depends on animation.
8. Check responsive/reflow behavior at narrow widths and zoom-sensitive layouts.
9. Separate automated findings from manual/behavioral findings.

## Output

Prioritize findings by user impact and release risk. Every finding should include evidence, affected surface, remediation, and verification method.

## Failure conditions

An automated scanner passing is not equivalent to WCAG conformance. Do not state that a surface is accessible solely because axe or another automated tool reports zero violations.
