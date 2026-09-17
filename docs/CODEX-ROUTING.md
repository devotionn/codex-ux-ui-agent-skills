# Codex routing model

Codex receives a user request and starts from `AGENTS.md`. It classifies the work by intent, then loads only the corresponding skill/rules/references.

```text
user request
   |
   v
AGENTS.md router
   |
   +-- component --------> design-component
   +-- screen -----------> design-screen
   +-- redesign ---------> redesign
   +-- accessibility ----> accessibility-audit
   +-- release ----------> ship
   |
   v
relevant rules + project conventions + framework adapter
   |
   v
implement
   |
   v
available deterministic verification
   |
   v
render / interaction verification when possible
   |
   v
adversarial critique
```

## Routing rule

Skills are reusable operating procedures, not personas. A skill should never override repository/product constraints discovered during inspection.

## Verification rule

The router must not send every request directly to `ship`. Build/design skills produce the implementation; `ship` is the final evidence and release workflow.
