# nAItmare: The OS for Multi-Agent Teams

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

nAItmare is a **Universal AI Context Architecture**. It acts as the immutable "Operating System" for your synthetic workforce, ensuring every agent follows the exact same laws, regardless of its underlying model.

> [!TIP]
> **The Problem:** Modern development teams employ 5+ different AI agents (Cursor, Windsurf, Claude Code, Gemini, GitHub Copilot). These agents "hallucinate" different rules and standards because they lack a single source of truth.
>
> **The Solution:** By centralizing your standards, skills, and workflows, you ensure that any agent you use behaves as a consistent member of your team.

---

## 🚀 Getting Started

1. **Define Your Laws**: Update [`.agent/memory/constitution.md`](.agent/memory/constitution.md) with your project's tech stack and coding standards.
2. **Set Your Team**: Create `.agent/sub-agents/me.md` with your team name (see [below](#-user-identity)).
3. **Enable Vendor Support**: Create a config file for your AI tool (see [below](#-enable-vendor-support)).

---

## 👤 User Identity

Each developer creates a personal (gitignored) file to declare their team:

**`.agent/sub-agents/me.md`**
```markdown
# My Identity

team: platform
```

---

## 🔌 Enable Vendor Support

Create the appropriate config file for your AI tool and add:

```markdown
> CRITICAL: Read AGENT.md first.
```

### Configuration File Reference

| Vendor | Configuration File |
| :--- | :--- |
| **Cursor** | `.cursorrules` |
| **Windsurf** | `.windsurfrules` |
| **Roo Code** | `.clinerules` |
| **GitHub Copilot** | `.github/copilot-instructions.md` |
| **Claude Code** | `CLAUDE.md` |
| **Gemini CLI** | `GEMINI.md` |
| **Amazon Q Developer** | `AMAZON_Q.md` |
| **Auggie CLI** | `.auggie.md` |
| **CodeBuddy** | `.codebuddy` |
| **Qoder** | `.qoder/context.md` |
| **OpenCode** | `.opencode` |
| **Amp** | `.amp.md` |
| **Kilo Code** | `.kilo` |
| **Qwen Code** | `.qwen` |
| **IBM Bob** | `.bob/config` |
| **Jules** | `.jules` |
| **SHAI** | `.shai` |
| **CODEX CLI** | `CODEX.md` |

---

## 🏛️ AI Infrastructure

```
.
├── AGENT.md                          # AI Entry Point
└── .agent/
    ├── memory/
    │   ├── constitution.md           # Global rules
    │   └── teams/
    │       ├── platform.md
    │       ├── privacy.md
    │       └── security.md
    │
    ├── skills/                       # Atomic how-to modules
    ├── workflows/                    # Orchestrated processes
    └── sub-agents/
        ├── me.md                     # User identity (gitignored)
        ├── tech-lead.md
        ├── qa.md
        └── devops.md
```

---

## 📄 License

MIT License - see [LICENSE](LICENSE).
