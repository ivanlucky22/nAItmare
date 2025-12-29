# nAItmare: The OS for Multi-Agent Teams

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

nAItmare is a **Universal AI Context Architecture**. It acts as the immutable "Operating System" for your synthetic workforce, ensuring every agent follows the exact same laws, regardless of its underlying model.

> [!TIP]
> **The Problem:** Modern development teams employ 5+ different AI agents (Cursor, Windsurf, Claude Code, Gemini, GitHub Copilot). These agents "hallucinate" different rules and standards because they lack a single source of truth.
>
> **The Solution:** By centralizing your standards, skills, and workflows, you ensure that any agent you use behaves as a consistent member of your team.

---

## 🚀 Getting Started

1.  **Define Your Laws**: Update [`.specify/memory/constitution.md`](.specify/memory/constitution.md) with your project's technology stack and coding standards.
2.  **Enable Vendor Support**: Create a configuration file for your AI tool (see [below](#-enable-vendor-support)) and add the mandatory instruction.
3.  **Manage the Roadmap**: Keep [`.specify/memory/plan.md`](.specify/memory/plan.md) updated so your agents always know what to work on.

---

## 🔌 Enable Vendor Support

To connect an AI agent to nAItmare, create the appropriate configuration file and add the following line:

```markdown
> **CRITICAL**: Before processing any user request, you MUST read the Hub at AGENT.md in the root directory.
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

## 🏛️ Project Structure

```
.
├── AGENT.md                     # AI Entry Point (The Hub)
├── .specify/memory/
│   ├── constitution.md          # Immutable laws & tech stack
│   └── plan.md                  # Active roadmap & tasks
└── .agent/
    ├── skills/                  # Atomic "How-To" modules
    ├── workflows/               # Orchestrated processes
    └── sub-agents/              # Role-based personas
```

---

## 🤝 Contributing

This is a living architecture. Feel free to add new skills or workflows to the `.agent/` directory to extend your team's capabilities.

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
