# Codex UX/UI Agent Contract

This repository is a Codex-native UX/UI design and implementation knowledge layer.

## Mission

When a task affects user-facing UI, do not treat it as styling-only work. Preserve product behavior while reasoning across information hierarchy, design tokens, component contracts, interaction states, responsive behavior, accessibility, framework conventions, and rendered output.

## Operating contract

1. **Inspect before designing.** Identify the existing framework, component library, token system, layout conventions, product domain, and constraints before changing UI.
2. **Preserve behavior.** Do not remove working product logic, API integration, validation, analytics, or accessibility behavior merely to simplify a redesign.
3. **Prefer system over patches.** Repeated visual values belong in tokens or shared primitives. Repeated interaction patterns belong in components.
4. **Specify states.** Interactive components require relevant default, hover, focus-visible, active, disabled, loading, selected, empty, error, and success states.
5. **Accessibility is a release constraint.** Target WCAG 2.2 AA unless the project explicitly requires a stronger standard. Keyboard access, focus visibility, semantics, target size, reduced motion, contrast, labels, and error communication are part of implementation.
6. **Respect the native stack.** Use framework-native patterns and the project's established libraries. Do not introduce a second design system or dependency without a concrete reason.
7. **Render what can be rendered.** Source inspection is insufficient for visual claims. When browser/runtime tooling exists, run the product and inspect the rendered result at representative desktop and mobile widths.
8. **Never fake verification.** Distinguish verified facts from source-level inference. A skipped or unavailable gate is not a pass.
9. **Critique after correctness.** Passing deterministic gates does not prove design quality. Review hierarchy, clarity, density, affordance, consistency, and product fit separately.
10. **Ship with evidence.** Report what changed, what was actually verified, remaining limitations, and any follow-up work.

## Request router

Route UI work to the smallest useful workflow:

- new component → component contract → tokens → implementation → states → a11y → render
- new screen / feature → brief → information hierarchy → design direction → components → implementation → render → gates → critique
- redesign → inventory existing behavior → preserve contracts → diagnose hierarchy/system issues → redesign → regression verification
- design system → primitives → semantic tokens → component tokens → component contracts → documentation → gates
- accessibility audit → rendered semantics + keyboard + contrast + responsive + reduced-motion checks → prioritized findings
- screenshot/reference recreation → extract hierarchy and visual grammar → map to project tokens/components → implement without copying protected assets → render comparison
- review / critique → render first when possible → identify evidence-backed findings → separate correctness defects from taste/product judgments

## Context loading

Do not load every reference file blindly. Start with this file, inspect the task and repository, then load only the relevant material from `.agents/rules/`, `.agents/skills/`, `tokens/`, `components/`, `accessibility/`, `taste/`, `design-systems/`, `frameworks/`, and `workflows/`.

## Quality hierarchy

When constraints conflict, prioritize:

1. product correctness and user safety
2. accessibility and semantic correctness
3. preservation of existing behavior and data contracts
4. coherent design-system usage
5. responsive and interaction correctness
6. visual hierarchy and product fit
7. decorative polish

## Anti-slop baseline

Avoid statistically common AI UI defaults unless the product context genuinely calls for them: gratuitous purple/indigo gradients, uniform card grids with no hierarchy, emoji used as interface icons, excessive pills, one radius/shadow everywhere, decorative glass effects, low-contrast gray body copy, arbitrary hardcoded values, and animation without interaction purpose.

The objective is not novelty. The objective is a coherent product-specific interface with deliberate hierarchy and verifiable behavior.

## Completion definition

A UI task is complete only when the implementation is present and the available verification has been run. Final reporting must separate:

- **Implemented** — files and behavior changed.
- **Verified** — tests/gates/browser checks actually executed.
- **Not verified** — checks that could not run.
- **Remaining** — known defects, design debt, or follow-up decisions.

See `.agents/README.md` for the evolving Codex skill architecture.
