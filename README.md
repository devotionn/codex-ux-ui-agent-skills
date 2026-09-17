# Codex UX/UI Agent Skills

A Codex-native adaptation of [plugin87/ux-ui-agent-skills](https://github.com/plugin87/ux-ui-agent-skills).

The goal is to turn Codex from a code generator into a design-aware implementation agent: design systems, DTCG tokens, component states, accessibility, framework-specific implementation, rendered verification, and objective quality gates.

## Status

🚧 Early development — the Codex-native instruction architecture is usable now, while the deeper upstream knowledge layer and deterministic gate suite continue to be ported.

## Team entry point

For designers, product managers, and broad UI/UX tasks, start with:

```text
$product-design
```

`product-design` is the orchestration skill. It inspects the current product and routes work to the smallest relevant specialist skills such as `design-screen`, `redesign`, `design-component`, `accessibility-audit`, `design-review`, and `ship`.

Designers should not need to memorize the specialist skill set.

See [`docs/TEAM_USAGE.md`](docs/TEAM_USAGE.md) for team rollout, installation scopes, and Chinese prompt examples.

## Codex skill compatibility

Skills live under `.agents/skills/<skill-name>/SKILL.md` and include YAML `name` and `description` metadata so Codex can discover them and match tasks to skills.

You can invoke a skill explicitly in Codex with `$skill-name` or browse installed skills with `/skills`. Repository-scoped skills can be checked into the product repository; user-scoped skills can be installed under `$HOME/.agents/skills`.

## Design principles

- **Codex-native first** — `AGENTS.md` is the project entry point; Claude-specific routing is not assumed.
- **Evidence over vibes** — accessibility, responsive behavior, states, token usage, and rendered behavior should be verifiable.
- **Preserve upstream strengths** — port the upstream token architecture, component knowledge, accessibility rules, taste doctrine, design-system library, framework adapters, workflows, tests, and objective gates where applicable.
- **Framework-aware** — React, Next.js, Vue, SwiftUI, Flutter and other adapters should preserve native conventions rather than forcing one UI stack everywhere.
- **No fake green** — unavailable browser/runtime checks must be reported as unavailable or failing, never silently treated as passing.
- **Progressive disclosure** — keep broad routing lightweight and load specialist rules/references only when the task needs them.

## Target workflow

```text
brief
  ↓
$product-design
  ↓
inspect existing product + stack
  ↓
route to narrow design skills
  ↓
DTCG tokens + component contracts when needed
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
  skills/                 reusable Codex skill instructions
    product-design/       default team entry point
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
docs/                      team rollout and project documentation
```

## Roadmap

**Phase 1 — Codex foundation**: `AGENTS.md`, routing contract, official skill metadata, team entry point, attribution, architecture.

**Phase 2 — Knowledge port**: tokens, components, accessibility, taste, 138 design-system references, framework adapters.

**Phase 3 — Skill depth**: connect specialist skills to the imported local references and end-to-end workflows.

**Phase 4 — Objective gates**: port and validate the upstream gate suite, including browser-backed checks.

**Phase 5 — Codex evals**: cold-start briefs that measure whether a fresh Codex session can produce compliant UI without hidden context.

## Upstream

This project is derived from `plugin87/ux-ui-agent-skills`, created by Thientan Soparat (@plugin87). Upstream is licensed under the MIT License. This repository preserves the upstream copyright and permission notice.

Upstream project: https://github.com/plugin87/ux-ui-agent-skills

## License

MIT. See [LICENSE](LICENSE).
