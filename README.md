# nAItmare: The OS for Multi-Agent Teams



> [!IMPORTANT]
> **The Problem:** Modern development teams employ 5+ different AI agents (Cursor, Windsurf, Claude Code, Gemini, GitHub Copilot). These agents "hallucinate" different rules and standards because they lack a single source of truth.
>
> **The Solution:** nAItmare is a **Universal AI Context Architecture**. It acts as the immutable "Operating System" for your synthetic workforce, ensuring every agent follows the exact same laws, regardless of its underlying model.

---

## 🏛️ Infrastructure Reference

The repository is structured to serve as a navigable map for AI agents.

### 🧠 The Hub & Governor
The intelligence core.

- **[AI.md](AI.md)**: The single entry point. Maps the agent to the Hub.
  - *Instruction*: "Read this first."
- **[.specify/memory/constitution.md](.specify/memory/constitution.md)**: The immutable laws (Tech Stack, Code Standards).
  - *Instruction*: "Follow these rules or stop."
- **[.specify/memory/plan.md](.specify/memory/plan.md)**: The active task list and roadmap.
  - *Instruction*: "Check what needs to be done."

### 🥉 Tier 1: Atomic Skills (`.agent/skills/`)
Reusable "How-To" modules.

- **[git.md](.agent/skills/git.md)**: Standardized commit/branching protocols (Conventional Commits).
- **[db.md](.agent/skills/db.md)**: Safe procedures for SQL/ORM operations.
- **[test.md](.agent/skills/test.md)**: Command lines for Jest and Playwright.
- **[review-checklist.md](.agent/skills/review-checklist.md)**: Criteria for code review (Styles, Security).

### 🥈 Tier 2: Standard Workflows (`.agent/workflows/`)
Orchestrated processes combining skills.

- **[feature-dev.md](.agent/workflows/feature-dev.md)**: `plan` → `code` → `test` → `commit`.
- **[bug-fix.md](.agent/workflows/bug-fix.md)**: `reproduce` → `fix` → `verify`.
- **[deploy.md](.agent/workflows/deploy.md)**: `lint` → `build` → `test` → `ship`.
- **[pr-review.md](.agent/workflows/pr-review.md)**: `fetch` → `review` → `report`.

### 🥇 Tier 3: Sub-Agent Personas (`.agent/sub-agents/`)
Specialized roles assigned to specific workflows.

- **[tech-lead.md](.agent/sub-agents/tech-lead.md)**: Reviewer & Standard Enforcer. Runs `pr-review`.
- **[qa.md](.agent/sub-agents/qa.md)**: Tester & Bug Hunter. Runs `bug-fix`.
- **[devops.md](.agent/sub-agents/devops.md)**: Builder & Shipper. Runs `deploy`.

---

## 🔌 Enable Vendor Support

nAItmare is compatible with all AI agents. To enable support, simply create the appropriate configuration file for your tool and add the following line:

```markdown
> **CRITICAL**: Before processing any user request, you MUST read the Hub at `AI.md` in the root directory.
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
