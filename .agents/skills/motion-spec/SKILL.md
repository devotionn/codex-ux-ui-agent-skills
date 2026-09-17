---
name: motion-spec
description: Define, review, or implement purposeful UI motion. Use for transitions, enter/exit behavior, progress feedback, micro-interactions, animated state changes, motion tokens, reduced-motion behavior, or when animation needs a clear functional purpose and runtime verification.
---

# Motion Spec

## Procedure

1. Identify the functional purpose of each motion: orientation, causality, feedback, continuity, or emphasis.
2. Reuse motion tokens for duration/easing instead of arbitrary per-component values.
3. Keep motion proportional to distance and interaction importance.
4. Ensure interaction remains understandable with motion reduced or removed.
5. Respect `prefers-reduced-motion` or the native platform equivalent.
6. Avoid animations that delay critical actions or conceal content until animation completion.
7. Verify actual runtime behavior where possible.

## Deliverables

Specify trigger, target, duration/token, easing/token, enter/exit behavior, interruption behavior, and reduced-motion fallback for material motion.

## Failure conditions

Decorative motion is not a substitute for state communication. Reduced-motion mode must not remove information or make controls unusable.
