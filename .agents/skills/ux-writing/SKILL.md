# UX Writing

## Use when

Writing or revising interface copy, labels, validation, errors, empty states, onboarding, confirmations, or destructive-action messaging.

## Procedure

1. Identify the user's task, context, and consequence of misunderstanding.
2. Match established product voice and terminology.
3. Prefer concrete action language over vague system language.
4. For errors, state what happened, what the user can do, and what data/state is preserved when relevant.
5. For empty states, distinguish true zero-data states from loading, permission, filtering, and failure states.
6. Make destructive actions explicit about scope and reversibility.
7. Keep labels stable across UI, documentation, and validation.
8. Check that text expansion/localization will not break the component contract where relevant.

## Failure conditions

Do not use copy to hide missing product behavior. A message saying an action succeeded is a defect if the underlying state did not change.
