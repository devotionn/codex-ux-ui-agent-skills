# Contributing

This project is a Codex-native adaptation of `plugin87/ux-ui-agent-skills`.

## Principles

- Preserve upstream attribution for derived material.
- Keep `AGENTS.md` concise; deeper knowledge belongs in selective references.
- New skills must define use criteria, procedure/deliverables, verification, and failure conditions.
- A deterministic gate must demonstrate that it rejects a broken case.
- Do not weaken checks to make examples pass.
- Do not report browser-dependent behavior as verified without a render.
- Keep upstream evidence and Codex evidence clearly separated.

## Commit style

Prefer small, reviewable commits grouped by capability: `feat:`, `fix:`, `docs:`, `test:`, `chore:`.

## Before proposing a capability as complete

Verify its routing path, local references, implementation contract, and available tests/gates. Record unavailable verification explicitly.
