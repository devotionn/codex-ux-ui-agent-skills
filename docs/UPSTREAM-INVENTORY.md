# Upstream inventory — v2.8.0

Observed upstream root areas:

- `.claude-plugin/` — Claude Code plugin packaging
- `.claude/` — Claude-specific skills/rules/commands/agent integration
- `accessibility/` — accessibility knowledge
- `bin/` — CLI entry points
- `components/` — component specifications
- `content/` — content/UX writing material
- `design-systems/` — design-system interoperability/reference material
- `docs/` — guides
- `evals/` — cold-start evaluations and recorded results
- `examples/` — rendered examples/harnesses
- `frameworks/` — framework adapters
- `reference/` — reference material
- `scripts/` — deterministic validation and rendering scripts
- `taste/` — design taste/anti-slop material and named design systems
- `templates/product-design/` — starter template
- `tests/` — gate regression tests and fixtures
- `tokens/` — DTCG token architecture
- `workflows/` — design workflows
- `CLAUDE.md` — upstream always-on agent brief
- `CONTEXT.md` — project context
- `package.json` — runnable scripts/dependencies

Upstream README at the baseline describes 19 runnable skills, 138 named design systems, and 44 objective gates; 31 gates open a real browser. Those counts are upstream facts and must not be presented as Codex-port coverage until the corresponding capability is actually imported and validated here.

## Import order

1. tokens + accessibility + component contracts
2. taste + design-system references
3. framework adapters + workflows
4. skill instructions
5. scripts + tests + bad fixtures
6. examples + browser harnesses
7. Codex-specific cold-start evals

Claude plugin packaging is reference-only; it is not copied as the Codex distribution mechanism.
