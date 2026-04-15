# Claude Power Tools

A curated collection of essential Claude Code skills and agents for professional developers.

> **"The right tool for the right job, at the right time."**

---

## Quick Reference

**Skills** (`/skill-name`) are guided workflows you interact with.  
**Agents** (`claude agent name`) are autonomous helpers that work independently.

**Can't decide?** Start with a Skill for dialogue, escalate to an Agent for speed.

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

### Plan

**`/brainstorming`** — Design features through dialogue
- *Best for:* Starting features where you tend to "figure it out as you code"
- *Why:* Encourages writing a design spec first (skip with `--quick` for spikes)

**`planner`** — Decompose complex features
- *Best for:* Multi-file refactors, architecture changes
- *Why:* Tailors plans to match your existing codebase patterns

---

### Build

**`/test-driven-development`** — TDD enforcement
- *Best for:* Features needing tests and edge case coverage
- *Why:* Encourages writing failing tests before implementation

**`/coding-standards`** — Enforce conventions
- *Best for:* Keeping code consistent across projects
- *Why:* Catches conceptual issues like "is this function doing too many things?"

**`code-reviewer`** — Automatic code review
- *Best for:* Pre-screening PRs before human review
- *Why:* Confidence-based filtering — only reports what truly matters

---

### Debug

**`/systematic-debugging`** — Root cause analysis
- *Best for:* Intermittent production bugs
- *Why:* Based on defense-in-depth — assumes multiple things could be wrong

**`build-error-resolver`** — Fix build/type errors
- *Best for:* Post-upgrade TypeScript error floods
- *Why:* Specialized per language (TS, Python, Go, Rust, etc.)

---

### Review

**`security-reviewer`** — Vulnerability scanning
- *Best for:* Auth, payment, or user data changes
- *Why:* OWASP Top 10, injection checks, dependency audit

**`/requesting-code-review`** — Pre-human review
- *Best for:* Catching formatting, unused vars, obvious bugs
- *Why:* Includes "silent-failure-hunter" for swallowed errors

---

### Polish

**`/humanizer`** — Remove AI writing patterns
- *Best for:* Blog posts, emails, user-facing content
- *Why:* Strips phrases like "In the ever-evolving landscape of..."

---

## Extended Toolkit (Power Users)

Useful, but learn Core first.

| Tool | What it does | Best for |
|------|--------------|----------|
| `/writing-plans` | Detailed implementation plans | Complex multi-phase features |
| `/receiving-code-review` | Process PR feedback with rigor | Evaluating reviewer suggestions |
| `code-simplifier` | Simplify while preserving behavior | Inherited nested-ternary nightmares |
| `architect` | System design and tradeoffs | Choosing between REST/GraphQL, SQL/NoSQL |
| `e2e-runner` | Playwright E2E testing | Critical user flows (checkout, signup) |
| `/verification-before-completion` | Pre-completion checklist | Before shipping — edge cases, debug code |
| `/the-humanizer` | Add personality to text | Emails that need warmth |
| `/frontend-design` | UX/UI guidance | Landing pages that shouldn't look generic |
| `/subagent-driven-development` | Multi-agent parallel workflows | 2000-line refactors |
| `/dispatching-parallel-agents` | Run agents simultaneously | Security + performance review in parallel |

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

| Workflow | Estimated Cost |
|----------|---------------|
| Single agent (code-reviewer) | ~$0.10-0.50 |
| Sequential skills (brainstorm → plan → review) | ~$0.50-2.00 |
| Parallel agents (security + e2e) | ~$1.00-3.00 |
| Subagent-driven (multi-agent refactor) | ~$2.00-5.00 |

**Money-saving tip:** Start with skills, escalate to agents only when needed.

---

## Installation

### Prerequisites

- Claude Code CLI installed
- Git for cloning

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
