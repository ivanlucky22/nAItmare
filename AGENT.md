# AGENT.md

> READ THIS FILE FIRST. All actions must comply with this architecture.

## Boot Sequence

Execute in order:

1. Load [constitution.md](.agent/memory/constitution.md) — immutable rules
2. Load [me.md](.agent/sub-agents/me.md) — identify user's team
   - If missing: prompt user for team or operate without team context
3. Load `.agent/memory/teams/<team>.md` — team-specific context
4. Select sub-agent based on task:
   - Backend Development → [backend-developer](.agent/sub-agents/backend-developer.md)
   - Frontend Development → [frontend-developer](.agent/sub-agents/frontend-developer.md)
   - Code Review → [tech-lead](.agent/sub-agents/tech-lead.md)
   - Testing/Debugging → [qa](.agent/sub-agents/qa.md)
   - Deployment → [devops](.agent/sub-agents/devops.md)

## Conflict Resolution

Priority (highest to lowest):
1. constitution.md
2. Team context
3. Sub-agent instructions
4. User instructions

## Resource Index

| Category | Path | Contents |
|----------|------|----------|
| Memory | `.agent/memory/` | constitution, team contexts |
| Skills | `.agent/skills/` | git, test, db, review-checklist |
| Sub-Agents | `.agent/sub-agents/` | backend-developer, frontend-developer, tech-lead, qa, devops |
