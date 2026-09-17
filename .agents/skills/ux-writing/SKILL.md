---
name: ux-writing
description: Write or revise product interface copy. Use for labels, buttons, validation, errors, empty states, onboarding, confirmations, destructive actions, status messages, helper text, or terminology consistency where copy must support a real user task and existing product behavior.
---

# UX Writing

## Procedure

1. Identify the user's task, context, and consequence of misunderstanding.
2. Match established product voice and terminology.
3. Prefer concrete action language over vague system language.
4. For errors, state what happened, what the user can do, and what data/state is preserved when relevant.
5. For empty states, distinguish true zero-data states from loading, permission, filtering, and failure states.
6. Make destructive actions explicit about scope and reversibility.
7. Keep labels stable across UI, documentation, and validation.
8. Check that text expansion/localization will not break the component contract where relevant.

## Deliverables

Return final copy in context, grouped by screen/component/state when more than a few strings are involved.

## Failure conditions

Do not use copy to hide missing product behavior. A message saying an action succeeded is a defect if the underlying state did not change.
