# nAItmare: Consistency Layer for AI Teams

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

**nAItmare** is a template that brings order to the chaos of multi-agent development — ensuring every AI tool in your stack follows the same rules.

> [!TIP]
> **The Problem:** Modern development teams employ 5+ different AI agents (Cursor, Windsurf, Claude Code, Gemini, GitHub Copilot). These agents "hallucinate" different rules and standards because they lack a single source of truth.
>
> **The Solution:** By centralizing your standards, skills, and sub-agents, you ensure that any agent you use behaves as a consistent member of your team.

---

## 🏛️ How It Works

### Conceptual Model

| Layer | Purpose | Contains |
|-------|---------|----------|
| **Sub-Agents** | WHO does it + WHAT steps to follow | `backend-developer`, `frontend-developer`, `tech-lead`, `qa`, `devops` |
| **Skills** | HOW to do atomic tasks | `git`, `test`, `db`, `review-checklist` |
| **Memory** | Context: rules and team knowledge | `constitution`, `teams/*` |

### Directory Structure

```
.
├── AGENTS.md                              # Entry point — agents read this first
│
└── .agent/
    │
    ├── memory/                           # Long-term context and governance
    │   ├── constitution.md               # Immutable rules: tech stack, code standards
    │   ├── general-context.md            # Shared context for ALL teams
    │   └── teams/                        # Team-specific domain knowledge
    │       └── _template.md              # Copy and rename for each team
    │
    ├── skills/                           # Atomic knowledge modules (HOW-TO)
    │   ├── git.md                        # Version control: commits, branches, conventions
    │   ├── test.md                       # Testing: commands, coverage requirements
    │   ├── db.md                         # Database: migrations, queries, safety rules
    │   └── review-checklist.md           # Code review: correctness, style, security
    │
    └── sub-agents/                       # Specialized personas (WHO + WHAT)
        ├── me.md                         # User identity: team membership (gitignored)
        ├── backend-developer.md          # Backend: APIs, services, database logic
        ├── frontend-developer.md         # Frontend: UI components, pages, client logic
        ├── tech-lead.md                  # Reviews code: fetch → review → approve/reject
        ├── qa.md                         # Tests & debugs: reproduce → isolate → fix → verify
        └── devops.md                     # Deploys: lint → build → test → ship
```

---

## 🚀 Getting Started

### 1. Enable Your AI Tool

Create the appropriate config file for your AI tool and add:

```markdown
> CRITICAL: Read AGENTS.md first.
```

See the [Vendor Reference](#-vendor-reference) section below for the correct file name.

### 2. Define Your Rules

Update [`.agent/memory/constitution.md`](.agent/memory/constitution.md) with your project's tech stack and coding standards.

### 3. Create Your Team Context

Copy `.agent/memory/teams/_template.md` to a new file named after your team (e.g., `platform.md`) and fill in your team's ownership and domain knowledge.

### 4. Set Your Identity

Each developer creates a personal (gitignored) file to declare their team:

**`.agent/sub-agents/me.md`**
```markdown
# My Identity

team: [YOUR_TEAM_NAME]
```

---

## 💬 Usage Examples

| Task | Prompt |
|------|--------|
| Backend Feature | "As a **backend-developer**, implement PROJ-123. Design: [URL]" |
| Frontend Feature | "As a **frontend-developer**, implement PROJ-456. Design: [URL]" |
| Write Tests | "As a **qa**, write tests for the login component" |
| Debug Issue | "As a **qa**, debug this error: TypeError..." |
| Code Review | "As a **tech-lead**, review my recent changes" |
| Deploy | "As a **devops**, deploy to staging" |

### Typical Development Flow

```
1. "As a backend-developer, implement PROJ-123. Design: https://confluence.example.com/page/123"
   → Agent reads design, creates plan, writes tests first, then implements APIs/services

2. "As a frontend-developer, implement PROJ-456. Design: https://confluence.example.com/page/456"
   → Agent reads design, creates plan, writes tests first, then implements UI components

3. "As a tech-lead, review my recent changes"
   → Agent reviews code against standards

4. "As a devops, deploy to staging"
   → Agent runs lint, build, test, deploy
```

---

## 🔌 Vendor Reference

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

## 📄 License

MIT License - see [LICENSE](LICENSE).
