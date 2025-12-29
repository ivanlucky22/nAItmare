# nAItmare: The OS for Multi-Agent Teams

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

nAItmare is a **Universal AI Context Architecture**. It acts as the immutable "Operating System" for your synthetic workforce, ensuring every agent follows the exact same laws, regardless of its underlying model.

> [!TIP]
> **The Problem:** Modern development teams employ 5+ different AI agents (Cursor, Windsurf, Claude Code, Gemini, GitHub Copilot). These agents "hallucinate" different rules and standards because they lack a single source of truth.
>
> **The Solution:** By centralizing your standards, skills, and sub-agents, you ensure that any agent you use behaves as a consistent member of your team.

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

## 💬 Usage Examples

The agent will automatically select the appropriate sub-agent based on your request:

| Task | Example Prompt | Sub-Agent |
|------|----------------|-----------|
| Implement Feature | "Implement the password reset feature" | `developer` |
| Write Tests | "Write tests for the login component" | `qa` |
| Debug Issue | "Debug this error: TypeError..." | `qa` |
| Code Review | "Review my recent changes" | `tech-lead` |
| Deploy | "Deploy to staging" | `devops` |

You can also explicitly invoke a sub-agent:

```
Use the tech-lead sub-agent to review this PR
```

---

## 🏛️ AI Infrastructure

### Conceptual Model

| Layer | Purpose | Contains |
|-------|---------|----------|
| **Sub-Agents** | WHO does it + WHAT steps to follow | `developer`, `tech-lead`, `qa`, `devops` |
| **Skills** | HOW to do atomic tasks | `git`, `test`, `db`, `review-checklist` |
| **Memory** | Context: rules and team knowledge | `constitution`, `teams/*` |

### Directory Structure

```
.
├── AGENT.md                              # Entry point — agents read this first
│
└── .agent/
    │
    ├── memory/                           # Long-term context and governance
    │   ├── constitution.md               # Immutable rules: tech stack, code standards
    │   └── teams/                        # Team-specific domain knowledge
    │       ├── platform.md               # Platform team context
    │       ├── privacy.md                # Privacy team context
    │       └── security.md               # Security team context
    │
    ├── skills/                           # Atomic knowledge modules (HOW-TO)
    │   ├── git.md                        # Version control: commits, branches, conventions
    │   ├── test.md                       # Testing: commands, coverage requirements
    │   ├── db.md                         # Database: migrations, queries, safety rules
    │   └── review-checklist.md           # Code review: correctness, style, security
    │
    └── sub-agents/                       # Specialized personas (WHO + WHAT)
        ├── me.md                         # User identity: team membership (gitignored)
        ├── developer.md                  # Implements features: plan → code → test → commit
        ├── tech-lead.md                  # Reviews code: fetch → review → approve/reject
        ├── qa.md                         # Tests & debugs: reproduce → isolate → fix → verify
        └── devops.md                     # Deploys: lint → build → test → ship
```

---

## 📄 License

MIT License - see [LICENSE](LICENSE).
