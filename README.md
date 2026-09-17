# Codex UX/UI Agent Skills

A Codex-native adaptation of [plugin87/ux-ui-agent-skills](https://github.com/plugin87/ux-ui-agent-skills).

The goal is to turn Codex from a code generator into a design-aware implementation agent: design systems, DTCG tokens, component states, accessibility, framework-specific implementation, rendered verification, and objective quality gates.

## Status

🚧 Early development — Phase 1 establishes the Codex-native instruction architecture before the full upstream knowledge layer and gates are ported.

## Design principles

- **Codex-native first** — `AGENTS.md` is the project entry point; Claude-specific routing is not assumed.
- **Evidence over vibes** — accessibility, responsive behavior, states, token usage, and rendered behavior should be verifiable.
- **Preserve upstream strengths** — port the upstream token architecture, component knowledge, accessibility rules, taste doctrine, design-system library, framework adapters, workflows, tests, and objective gates where applicable.
- **Framework-aware** — React, Next.js, Vue, SwiftUI, Flutter and other adapters should preserve native conventions rather than forcing one UI stack everywhere.
- **No fake green** — unavailable browser/runtime checks must be reported as unavailable or failing, never silently treated as passing.

## Target workflow

```text
brief
  ↓
inspect existing product + stack
  ↓
select / infer design direction
  ↓
DTCG tokens + component contracts
  ↓
implementation
  ↓
render + interaction verification
  ↓
WCAG + responsive + state gates
  ↓
adversarial design critique
  ↓
fix → verify → ship
```

## Repository architecture

```text
AGENTS.md                 Codex project contract and router
.agents/
  skills/                 reusable Codex-oriented skill instructions
  rules/                  deeper design and implementation rules
tokens/                    DTCG token knowledge and templates
components/                component contracts and states
design-systems/            named design-system references
accessibility/             WCAG guidance and audits
taste/                     visual direction and anti-slop doctrine
frameworks/                framework adapters
workflows/                 end-to-end design workflows
scripts/                   deterministic validation gates
evals/                     cold-start agent evaluations
tests/                     gate regression fixtures
examples/                  rendered examples and harnesses
```

## Roadmap

**Phase 1 — Codex foundation**: `AGENTS.md`, routing contract, skill format, attribution, architecture.

**Phase 2 — Knowledge port**: tokens, components, accessibility, taste, 138 design-system references, framework adapters.

**Phase 3 — Skill port**: convert upstream runnable design skills into Codex-oriented reusable skills and workflows.

**Phase 4 — Objective gates**: port and validate the upstream gate suite, including browser-backed checks.

**Phase 5 — Codex evals**: cold-start briefs that measure whether a fresh Codex session can produce compliant UI without hidden context.

## Upstream

This project is derived from `plugin87/ux-ui-agent-skills`, created by Thientan Soparat (@plugin87). Upstream is licensed under the MIT License. This repository preserves the upstream copyright and permission notice.

Upstream project: https://github.com/plugin87/ux-ui-agent-skills

## License

MIT. See [LICENSE](LICENSE).
