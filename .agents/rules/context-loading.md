# Context loading

Codex should not load the entire design corpus for every UI task.

## Minimal loading matrix

- component work → component skill + component rules + relevant tokens + framework adapter
- screen work → screen skill + taste direction + tokens + relevant component specs + framework adapter
- accessibility audit → accessibility skill + accessibility references + verification rules
- redesign → redesign skill + existing project conventions + taste + relevant component/token rules
- ship → ship skill + verification rules + project test/gate commands

Load named design-system references only when selecting, matching, or auditing a visual direction. Load framework adapters only for the stack being changed.

When a task spans multiple skills, compose the smallest set necessary rather than loading the full repository.
