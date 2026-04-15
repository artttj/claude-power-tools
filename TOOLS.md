# Tools Reference

Complete reference for all skills and agents in Claude Power Tools.

---

## Skills

### `/brainstorming`

**When to Use:** Designing new features, products, or projects from scratch

**What It Does:** Guides you through a structured design process — starting with context exploration, asking clarifying questions, presenting approaches, and producing a written design spec.

**Key Benefit:** Prevents jumping into implementation before understanding the problem

**Example:**
```bash
/brainstorming I want to add user authentication to my app
```

**Pro Tips:**
- Answer the questions honestly — the skill is designed to surface assumptions
- Review the generated spec before moving to implementation

---

### `/writing-plans`

**When to Use:** Before implementing complex features

**What It Does:** Creates detailed implementation plans with phases, dependencies, file modifications, and verification steps.

**Key Benefit:** Forces thinking through edge cases before coding

**Example:**
```bash
/writing-plans Add real-time notifications using WebSockets
```

---

### `/test-driven-development`

**When to Use:** Writing new features or fixing bugs

**What It Does:** Enforces RED-GREEN-IMPROVE cycle: write failing test first, implement to pass, then refactor.

**Key Benefit:** Guarantees testable code and 80%+ coverage

**Example:**
```bash
/tdd-guide Add user registration endpoint
```

---

### `/systematic-debugging`

**When to Use:** Complex bugs that resist quick fixes

**What It Does:** Structured root cause analysis using pattern matching, hypothesis testing, and defense in depth.

**Key Benefit:** Prevents "fixing" symptoms instead of causes

**Example:**
```bash
/systematic-debugging Memory leak in production server
```

---

### `/subagent-driven-development`

**When to Use:** Large tasks that can be parallelized

**What It Does:** Orchestrates multiple specialized agents working in parallel (e.g., reviewer + tester + documenter).

**Key Benefit:** Faster completion of multi-faceted tasks

**Example:**
```bash
/subagent-driven-development Refactor auth module
```

---

### `/dispatching-parallel-agents`

**When to Use:** Multiple independent subtasks

**What It Does:** Runs agents simultaneously for independent operations.

**Key Benefit:** Linear speedup for parallelizable work

**Example:**
```bash
# Run security review and performance analysis at the same time
```

---

### `/receiving-code-review`

**When to Use:** Processing PR feedback

**What It Does:** Helps evaluate review comments with technical rigor — verifying correctness before implementing.

**Key Benefit:** Prevents performative agreement and blind implementation

---

### `/requesting-code-review`

**When to Use:** Preparing code for review

**What It Does:** Runs automated code review before human review.

**Key Benefit:** Catches issues before humans spend time on them

---

### `/coding-standards`

**When to Use:** Writing or reviewing code

**What It Does:** Enforces naming conventions, immutability, KISS, DRY, YAGNI principles.

**Key Benefit:** Consistent, maintainable code across projects

---

### `/frontend-design`

**When to Use:** Building UI components or pages

**What It Does:** Provides UX/UI guidance, component patterns, and accessibility best practices.

**Key Benefit:** Professional-quality frontend output

---

### `/the-humanizer`

**When to Use:** Polishing AI-generated content

**What It Does:** Adjusts tone and style to sound more natural and human.

**Key Benefit:** Reduces "AI-speak" in user-facing content

---

### `/verification-before-completion`

**When to Use:** Before marking work complete

**What It Does:** Systematic verification checklist ensuring nothing was missed.

**Key Benefit:** Fewer "oops, forgot to..." moments

---

## Agents

### `code-reviewer`

**When to Use:** After writing or modifying code

**What It Does:** Reviews code for quality, patterns, and best practices

**Key Benefit:** Catches issues before human review

**Usage:**
```bash
claude agent code-reviewer
```

---

### `code-simplifier`

**When to Use:** Code feels complex or hard to read

**What It Does:** Simplifies code while preserving behavior — extracts nested logic, removes dead code, improves names.

**Key Benefit:** Maintainable code without losing functionality

**Usage:**
```bash
claude agent code-simplifier
```

---

### `security-reviewer`

**When to Use:** Security-sensitive code (auth, payments, user data)

**What It Does:** Scans for vulnerabilities, OWASP Top 10, injection risks

**Key Benefit:** Prevents security incidents

**Usage:**
```bash
claude agent security-reviewer
```

---

### `build-error-resolver`

**When to Use:** Build or type check failures

**What It Does:** Analyzes error messages, fixes incrementally

**Key Benefit:** Faster recovery from build breaks

**Usage:**
```bash
claude agent build-error-resolver
```

---

### `planner`

**When to Use:** Complex features requiring decomposition

**What It Does:** Creates implementation plans with phases and dependencies

**Key Benefit:** Clear roadmap before coding

**Usage:**
```bash
claude agent planner
```

---

### `architect`

**When to Use:** System design decisions

**What It Does:** Evaluates tradeoffs, scalability, and architectural patterns

**Key Benefit:** Informed decisions with documented rationale

**Usage:**
```bash
claude agent architect
```

---

### `e2e-runner`

**When to Use:** Critical user flows need verification

**What It Does:** Creates and runs E2E tests with Playwright

**Key Benefit:** Confidence that key paths work

**Usage:**
```bash
claude agent e2e-runner
```
