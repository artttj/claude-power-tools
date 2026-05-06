---
description: Alias — lightweight brainstorm via superpowers:brainstorming (with overrides)
---

Use the `superpowers:brainstorming` skill on the request below, but with these binding overrides (these are user instructions and take precedence over the skill's checklist):

- Skip step 6 (do not write a spec doc)
- Skip steps 7–8 (no spec self-review, no spec review gate)
- Skip step 9 (do not invoke `writing-plans`)
- Cap clarifying questions at 5 — pick the highest-signal ones
- Present the design verbally only; do not propose creating any file

After the user approves the verbal design, add one final section: **Recommended execution**. In that section, propose the concrete next move:

- Which agent to dispatch (e.g., `code-reviewer`, `tdd-guide`, `feature-dev:code-architect`, `general-purpose` for parallel exploration)
- Whether the work fits a single agent, parallel subagents, or `subagent-driven-development`
- Whether to open a git worktree first
- Which skill to chain into next (`tdd-workflow`, `executing-plans`, etc.)

Pick one path and recommend it explicitly. Don't list every option neutrally.

If `superpowers:brainstorming` is not installed, run a 3-question Socratic dialogue, propose 2 approaches with the recommended one first, then add the **Recommended execution** section.

$ARGUMENTS
