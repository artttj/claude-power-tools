# rapid-stack for OpenCode

Same commands, ported to OpenCode.

## Install

Symlink or copy this directory into your project, or merge into `~/.config/opencode/`:

```bash
# project-local
git clone https://github.com/artttj/rapid-stack.git /tmp/rapid-stack
cp -R /tmp/rapid-stack/.opencode/* .opencode/

# or global
cp -R /tmp/rapid-stack/.opencode/* ~/.config/opencode/
```

## What works out of the box

These commands run with bundled skills and agents and need nothing else:

`/ask` `/10x` `/trim` `/cr` `/hum` `/polish` `/std` `/prm` `/sec`

## What needs external skills

Three commands wrap upstream skills that aren't bundled here, same as in Claude Code. The SKILL.md format is portable, so dropping the upstream skill into `.opencode/skills/<name>/SKILL.md` makes the command work in OpenCode.

| Command | Upstream | Source |
|---|---|---|
| `/brn` | `brainstorming` | [obra/superpowers](https://github.com/obra/superpowers) — MIT |
| `/ui` | `design` (a.k.a. ui-ux-pro-max) | [nextlevelbuilder/ui-ux-pro-max-skill](https://github.com/nextlevelbuilder/ui-ux-pro-max-skill) — MIT |
| `/jobs` | `steve-jobs-perspective` | [alchaincyf/steve-jobs-skill](https://github.com/alchaincyf/steve-jobs-skill) |

Quick install: `cp -R /path/to/superpowers/skills/brainstorming .opencode/skills/`. Same pattern for the others.

One caveat: Claude Code skills auto-trigger via a session bootstrap. OpenCode loads skills explicitly via the `skill` tool. The content runs in both, but skills that assume auto-trigger behavior (like `superpowers:brainstorming`) may behave differently in OpenCode.

## Format differences from the Claude Code plugin

- Agents use `mode: subagent` and a `permission` block declaring `edit`, `write`, and `bash`. Values vary per agent. For example, `code-reviewer` denies writes, while `code-simplifier` and `security-reviewer` allow them.
- Skills are read directly from `.opencode/skills/<name>/SKILL.md`. OpenCode also reads `.claude/skills/` natively, so the existing Claude Code skill layout would work too.
- Commands are unchanged. `description` frontmatter and `$ARGUMENTS` placeholder work in both ecosystems.
