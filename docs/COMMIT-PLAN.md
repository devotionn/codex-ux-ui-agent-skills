# Commit plan

Keep future port commits capability-oriented rather than dumping the entire upstream repository in one opaque commit.

Suggested sequence:

1. `feat: port token foundation from upstream v2.8.0`
2. `feat: port accessibility knowledge from upstream v2.8.0`
3. `feat: port component contracts from upstream v2.8.0`
4. `feat: port taste and design-system references`
5. `feat: port framework adapters and workflows`
6. `feat: adapt remaining runnable skills for Codex`
7. `test: port deterministic non-browser gates`
8. `test: port browser-backed gates and fixtures`
9. `eval: add Codex cold-start briefs`

Each phase should leave the repository usable and explain what is still unverified.
