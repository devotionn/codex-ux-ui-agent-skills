---
name: design-tokens
description: Create, extend, normalize, audit, or migrate a product's design tokens. Use when work involves colors, typography, spacing, sizing, radius, borders, elevation, motion, breakpoints, themes, DTCG token files, semantic aliases, or replacing repeated hardcoded design values with a maintainable token system.
---

# Design Tokens

## Procedure

1. Inventory existing variables, theme files, utility configuration, component constants, and hardcoded values.
2. Preserve existing public token names when changing them would create unnecessary migration risk.
3. Prefer a three-tier model when the project can support it: primitive values → semantic intent → component tokens.
4. Use DTCG-compatible structure for portable token artifacts unless the existing system has a stronger native contract.
5. Define light/dark or other theme mappings at the semantic layer rather than duplicating component logic.
6. Include color, typography, spacing, sizing, radius, border, elevation/shadow, motion, and breakpoint concepts only where the product actually needs them.
7. Validate aliases/references and detect unresolved tokens.
8. Render representative components before asserting that token changes are visually safe.

## Deliverables

- token changes or migration plan
- alias/semantic mapping
- impacted component inventory
- validation and render evidence

## Failure conditions

Do not create token aliases that resolve cyclically or to missing values. Do not claim a theme migration is complete while material hardcoded design values remain unexplained.
