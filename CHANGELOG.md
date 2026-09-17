# Changelog

## Unreleased

### Added

- `product-design` as the default designer/product-team orchestration skill.
- Chinese team rollout and usage guide at `docs/TEAM_USAGE.md`.
- Optional Codex UI metadata for the `product-design` skill.

### Changed

- Added current Codex `name` / `description` frontmatter to all initial skills for discovery and implicit triggering.
- Expanded root routing so broad product-design tasks use the orchestration skill while narrow tasks remain composable.
- Updated README and skill index with team installation and usage guidance.

### Existing foundation

- Codex-native root `AGENTS.md`.
- `.agents/` architecture and reusable design skills.
- Evidence-driven verification rules.
- Claude→Codex porting contract.
- Upstream tracking and staged port roadmap.

### Upstream baseline

- `plugin87/ux-ui-agent-skills` v2.8.0.
