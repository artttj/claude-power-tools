# Claude Power Tools

A curated collection of essential Claude Code skills and agents for professional developers.

> **"The right tool for the right job, at the right time."**

## Quick Start

```bash
# Use a skill
/skill-name

# Use an agent
claude agent agent-name

# Browse examples
ls examples/
```

## The Toolkit

| Category | Tools |
|----------|-------|
| 🎯 **Starting Something New** | `/brainstorming`, `/writing-plans` |
| 📝 **Writing Code** | `/test-driven-development`, `code-reviewer`, `code-simplifier` |
| 🐛 **When Things Break** | `/systematic-debugging`, `build-error-resolver` |
| ☁️ **Cloud & Security** | `security-reviewer` |
| 🏗️ **Big Decisions** | `planner`, `architect`, `/frontend-design` |
| 🔍 **Review** | `/receiving-code-review`, `/requesting-code-review` |
| 🎨 **Polish** | `/the-humanizer` |
| ⚡ **Level Up** | `/subagent-driven-development`, `/dispatching-parallel-agents` |
| 🧪 **Testing** | `e2e-runner`, `/verification-before-completion` |
| 📋 **Standards** | `/coding-standards` |

## Why These Tools?

**Daily utility** — Used multiple times per week  
**Time saved** — At least 10x vs manual approaches  
**Quality impact** — Catches bugs, improves design, enforces consistency

## Installation

```bash
git clone https://github.com/YOUR_USERNAME/claude-power-tools.git
```

No dependencies. Works with your existing Claude Code installation.

## Structure

```
claude-power-tools/
├── skills/          # Skill definitions (invoked via /skill-name)
├── agents/          # Agent definitions (invoked via claude agent)
├── examples/        # Real-world usage examples
└── TOOLS.md         # Detailed tool reference
```

## Contributing

1. Fork the repository
2. Add your skill or agent
3. Update TOOLS.md
4. Submit a PR

## License

MIT — See [LICENSE](LICENSE)
