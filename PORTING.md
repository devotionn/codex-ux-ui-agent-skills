# Claude → Codex porting contract

The upstream project is optimized for Claude Code. This fork should preserve design knowledge and measurable behavior while replacing Claude-specific orchestration with Codex-native project instructions.

| Upstream concept | Codex adaptation |
| --- | --- |
| root `CLAUDE.md` always-on brief | root `AGENTS.md` |
| `.claude/rules/*` | `.agents/rules/*` loaded on demand |
| `.claude/skills/*` | `.agents/skills/*` with explicit skill contracts |
| Claude slash-command routing | natural-language router in `AGENTS.md` + skill selection |
| Claude plugin packaging | later Codex distribution/install strategy; do not assume compatibility |
| design-critic subagent | adversarial critique workflow; use subagent capability only when the host supports it |
| objective Node/browser gates | retain as deterministic scripts with regression fixtures |
| Claude cold-start evals | new Codex cold-start eval runs; preserve upstream evals only as upstream evidence |

## Non-goals

- blind search-and-replace of `Claude` with `Codex`;
- claiming upstream Claude evaluation results as Codex evaluation results;
- changing deterministic gate semantics merely to make the port green;
- bundling all design knowledge into `AGENTS.md` and exhausting context on every task.

## Port acceptance

A capability is considered ported only when its instructions have a Codex loading/routing path and its verification story is documented. Runnable gates additionally require a negative fixture or equivalent evidence that the check can fail broken work.
