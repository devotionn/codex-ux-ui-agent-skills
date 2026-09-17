# Motion Spec

## Use when

Defining or implementing UI motion, transitions, enter/exit behavior, progress feedback, or interaction animation.

## Procedure

1. Identify the functional purpose of each motion: orientation, causality, feedback, continuity, or emphasis.
2. Reuse motion tokens for duration/easing instead of arbitrary per-component values.
3. Keep motion proportional to distance and interaction importance.
4. Ensure interaction remains understandable with motion reduced or removed.
5. Respect `prefers-reduced-motion` or the native platform equivalent.
6. Avoid animations that delay critical actions or conceal content until animation completion.
7. Verify actual runtime behavior where possible.

## Failure conditions

Decorative motion is not a substitute for state communication. Reduced-motion mode must not remove information or make controls unusable.
