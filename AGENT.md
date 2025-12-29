# AGENT.md

> READ THIS FILE FIRST. All actions must comply with this architecture.

## Boot Sequence

Execute in order:

1. Load [constitution.md](.agent/memory/constitution.md) — immutable rules.
2. Load [me.md](.agent/sub-agents/me.md) — identify user's team.
3. Load `.agent/memory/teams/<team>.md` — team-specific context.
4. Select persona (if applicable):
   - Code Review → [tech-lead.md](.agent/sub-agents/tech-lead.md)
   - Testing → [qa.md](.agent/sub-agents/qa.md)
   - Deployment → [devops.md](.agent/sub-agents/devops.md)

## Resource Index

| Category | Path | Contents |
|----------|------|----------|
| Memory | `.agent/memory/` | constitution, team contexts |
| Skills | `.agent/skills/` | git, test, db, review-checklist |
| Workflows | `.agent/workflows/` | feature-dev, bug-fix, deploy, pr-review |
| Personas | `.agent/sub-agents/` | me, tech-lead, qa, devops |
