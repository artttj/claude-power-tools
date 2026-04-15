# Claude Power Tools

A curated collection of essential Claude Code skills and agents for professional developers.

> **"The right tool for the right job, at the right time."**

---

## What Are These?

**Skills** (`/skill-name`) are guided conversation workflows defined in YAML files that customize Claude's behavior. You interact with them — they ask questions, you respond.

**Agents** (`claude agent name`) are pre-configured task-specific assistants. You delegate to them — they work autonomously and return results.

**Can't decide?** Start with a Skill for dialogue when learning, escalate to an Agent for speed once familiar.

---

## Quick Start

```bash
# Use a skill (interactive)
/brainstorming

# Use an agent (autonomous)
claude agent code-reviewer
```

---

## Start Here

**New to these tools?** Pick 2-3 from Core, ignore Extended for now.

**Most useful first:**
1. `/brainstorming` — Before starting any feature
2. `code-reviewer` — After writing code
3. `/systematic-debugging` — When stuck on bugs

---

## Core Toolkit (10 tools)

These solve daily problems. Learn these first.

| Tool | Type | Best For | Skip If... |
|------|------|----------|------------|
| `/brainstorming` | Skill | Starting features | Just adding a field to existing form |
| `planner` | Agent | Multi-file refactors | Single-file change |
| `/test-driven-development` | Skill | Features needing tests | Spikes/experiments |
| `/coding-standards` | Skill | Keeping code consistent | Reviewing someone else's code |
| `code-reviewer` | Agent | Pre-screening PRs | PR is <10 lines, only tests |
| `/systematic-debugging` | Skill | Intermittent production bugs | Obvious typo/quick fix |
| `build-error-resolver` | Agent | Post-upgrade error floods | Single build error |
| `security-reviewer` | Agent | Auth/payment/user data changes | Pure UI changes |
| `/requesting-code-review` | Skill | Catching obvious bugs | Emergency hotfix |
| `/humanizer` | Skill | Blog posts, emails | Internal docs, code comments |

---

## Extended Toolkit (Power Users)

Useful, but learn Core first. These tools are **optional**.

**Polish:**
- `/the-humanizer` (Skill) — Add personality to text
- `/frontend-design` (Skill) — UX/UI guidance

**Review:**
- `/receiving-code-review` (Skill) — Process PR feedback
- `code-simplifier` (Agent) — Simplify complex code

**Planning:**
- `/writing-plans` (Skill) — Detailed implementation plans
- `architect` (Agent) — System design decisions

**Testing:**
- `e2e-runner` (Agent) — Playwright E2E tests
- `/verification-before-completion` (Skill) — Pre-ship checklist

**Scale:**
- `/subagent-driven-development` (Skill) — Multi-agent workflows
- `/dispatching-parallel-agents` (Skill) — Parallel execution

---

## Workflow Guidance

```bash
# Quick fix (< 2 hours):
code-reviewer

# Medium feature (1-2 days):
/brainstorming → code-reviewer → /verification-before-completion

# Large feature (1+ weeks):
/brainstorming → planner → /test-driven-development → 
code-reviewer → security-reviewer → e2e-runner
```

---

## Cost Transparency

| Workflow | Estimated Cost | When to Use |
|----------|---------------|-------------|
| Single agent | ~$0.10-0.50 | Quick reviews, small fixes |
| Sequential skills | ~$0.50-2.00 | Medium features |
| Parallel agents | ~$1.00-3.00 | Security + review together |
| Subagent-driven | ~$2.00-5.00 | Large refactors only |

**Money-saving tip:** Start with skills, escalate to agents only when needed. Costs are per-run, not subscription.

---

## Installation

### Prerequisites

- Claude Code CLI installed (`claude --version` ≥ 0.1.0)
- Git for cloning
- API key configured (if using agents extensively)

### Personal Setup

```bash
git clone https://github.com/artttj/claude-power-tools.git
cd claude-power-tools
cp -r skills/* ~/.claude/skills/
cp -r agents/* ~/.claude/agents/
```

### Team Setup

**Option 1: Git Submodule (Recommended)**
```bash
# In your team repo
git submodule add https://github.com/artttj/claude-power-tools.git .claude-tools
# Team updates via: git submodule update
```

**Option 2: Fork + Customize**
1. Fork this repo
2. Customize `/coding-standards` for your stack
3. Team clones the fork

### Verify

```bash
ls ~/.claude/skills/  # Should show core tools
ls ~/.claude/agents/  # Should show agents
```

**Success:** You can now run `/brainstorming` and `claude agent code-reviewer`.

---

## License

MIT
