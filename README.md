# Claude Power Tools

A curated collection of essential Claude Code skills and agents for professional developers.

> **"The right tool for the right job, at the right time."**

**Skills** (`/skill-name`) are guided workflows you interact with.  
**Agents** (`claude agent name`) are specialized helpers that work autonomously.

---

## Start Here

**New to Claude Code tools?** Try these first:

1. `/brainstorming` — Before starting any new feature
2. `code-reviewer` — After writing or modifying code
3. `/systematic-debugging` — When you're stuck on a bug
4. `planner` — When the task feels too big

---

## The Toolkit

| Stage | Skills | Agents |
|-------|--------|--------|
| **Plan** | `/brainstorming`, `/writing-plans` | `planner`, `architect` |
| **Build** | `/test-driven-development`, `/coding-standards` | `code-reviewer`, `code-simplifier` |
| **Review** | `/receiving-code-review`, `/requesting-code-review` | `security-reviewer` |
| **Debug** | `/systematic-debugging` | `build-error-resolver` |
| **Test** | `/verification-before-completion` | `e2e-runner` |
| **Polish** | `/humanizer`, `/the-humanizer`, `/frontend-design` | — |
| **Scale** | `/subagent-driven-development`, `/dispatching-parallel-agents` | — |

---

## Plan

### `/brainstorming` (Skill)

Design features through structured dialogue.

**Why it matters:** Designed to block implementation until you've written a design spec.

**Best for:** Starting new features where you're tempted to "figure it out as you code."

---

### `/writing-plans` (Skill)

Create detailed implementation plans.

**Why it matters:** Plans critique themselves before finalizing — catches blind spots early.

**Best for:** Complex features that span multiple files or systems.

---

### `planner` (Agent)

Complex feature decomposition.

**Why it matters:** Analyzes existing codebase patterns first, then tailors the plan to match.

**Best for:** Breaking down microservices, migrations, or multi-phase refactors.

---

### `architect` (Agent)

System design and tradeoff evaluation.

**Why it matters:** Forces explicit "We're choosing X over Y because..." documentation.

**Best for:** Deciding between REST vs GraphQL, monolith vs microservices, PostgreSQL vs Mongo.

---

## Build

### `/test-driven-development` (Skill)

TDD enforcement (RED→GREEN→IMPROVE).

**Why it matters:** Designed to block implementation until you have a failing test.

**Best for:** Features where you want guaranteed test coverage and testable code.

---

### `/coding-standards` (Skill)

Enforce conventions (KISS, DRY, YAGNI, immutability).

**Why it matters:** Checks conceptual issues like "is this function doing too many things?"

**Best for:** Keeping code consistent across projects and teams.

---

### `code-reviewer` (Agent)

Automatic code quality review.

**Why it matters:** Uses confidence-based filtering — only reports issues that truly matter.

**Best for:** Pre-screening PRs before human review.

---

### `code-simplifier` (Agent)

Simplify code while preserving behavior.

**Why it matters:** Will undo clever optimizations if they hurt readability.

**Best for:** Inherited code with nested ternaries or unclear logic.

---

## Review

### `/receiving-code-review` (Skill)

Handle PR feedback with rigor.

**Why it matters:** Built-in YAGNI check — flags "implement properly" requests for unused code.

**Best for:** Evaluating reviewer suggestions before implementing.

---

### `/requesting-code-review` (Skill)

Automated pre-human review.

**Why it matters:** Includes "silent-failure-hunter" for swallowed errors and bad fallbacks.

**Best for:** Catching formatting, unused vars, and obvious bugs before team review.

---

### `security-reviewer` (Agent)

Vulnerability scanning (OWASP, injections).

**Why it matters:** Paranoid by design — assumes everything is suspicious.

**Best for:** Auth, payment, or user data changes. Better safe than breached.

---

## Debug

### `/systematic-debugging` (Skill)

Root cause analysis for complex bugs.

**Why it matters:** Based on defense-in-depth — assumes multiple things could be wrong.

**Best for:** Intermittent production issues that resist quick fixes.

---

### `build-error-resolver` (Agent)

Fix build and type errors.

**Why it matters:** Specialized per language — different strategies for TS, Python, Go, Rust, etc.

**Best for:** 47 TypeScript errors after an upgrade — reads patterns, fixes incrementally.

---

## Test

### `/verification-before-completion` (Skill)

Pre-completion checklist.

**Why it matters:** Checks both technical (tests pass) and process (docs updated) items.

**Best for:** Before shipping — edge cases tested? debug code removed? README updated?

---

### `e2e-runner` (Agent)

E2E testing with Playwright.

**Why it matters:** Manages test quarantines — flaky tests don't block CI.

**Best for:** Critical user flows that unit tests miss (checkout, signup, payments).

---

## Polish

### `/humanizer` (Skill)

Remove AI writing patterns.

**Why it matters:** Based on Wikipedia's AI Cleanup project — analyzed thousands of AI-edited articles.

**Best for:** Blog posts and emails before publishing — removes "In the ever-evolving landscape..."

---

### `/the-humanizer` (Skill)

Add voice and personality to text.

**Why it matters:** While `/humanizer` removes AI tells, this adds voice and opinions.

**Best for:** Sterile emails that need warmth: "I genuinely don't know how to feel about this deadline."

---

### `/frontend-design` (Skill)

UX/UI guidance and patterns.

**Why it matters:** "Anti-template policy" — blocks generic Tailwind/shadcn defaults.

**Best for:** Landing pages that shouldn't look like every other SaaS site.

---

## Scale

### `/subagent-driven-development` (Skill)

Multi-agent parallel workflows.

**Why it matters:** Inspired by GANs — generator + evaluator iterate until quality threshold.

**Best for:** 2000-line refactors where one agent codes, one reviews, one tests — simultaneously.

---

### `/dispatching-parallel-agents` (Skill)

Run multiple agents simultaneously.

**Why it matters:** The primitive that subagent-driven-development is built on.

**Best for:** Security + performance + code review in parallel (10 min vs 30 min).

---

## Installation

### Prerequisites

- Claude Code CLI installed (`claude --version` ≥ 0.1.0)
- Git for cloning

### Install

```bash
# Clone the repository
git clone https://github.com/artttj/claude-power-tools.git
cd claude-power-tools

# Copy skills and agents to your Claude directory
cp -r skills/* ~/.claude/skills/
cp -r agents/* ~/.claude/agents/
```

### Verify Installation

```bash
# Should list available skills
ls ~/.claude/skills/

# Should list available agents
ls ~/.claude/agents/
```

**Success:** You can now invoke skills with `/skill-name` and agents with `claude agent agent-name`.

---

## License

MIT
