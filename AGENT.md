# AGENT.md

> READ THIS FILE FIRST. All actions must comply with this architecture.

## Boot Sequence

Execute in order:

1. Load [constitution.md](.specify/memory/constitution.md) — immutable rules.
2. Load [plan.md](.specify/memory/plan.md) — current priorities.
3. Select persona (if applicable):
   - Code Review → [tech-lead.md](.agent/sub-agents/tech-lead.md)
   - Testing/Debugging → [qa.md](.agent/sub-agents/qa.md)
   - Deployment → [devops.md](.agent/sub-agents/devops.md)

## Resource Index

| Category | Path | Contents |
|----------|------|----------|
| Skills | `.agent/skills/` | git, test, db, review-checklist |
| Workflows | `.agent/workflows/` | feature-dev, bug-fix, deploy, pr-review |
| Personas | `.agent/sub-agents/` | tech-lead, qa, devops |
| Governance | `.specify/memory/` | constitution, plan |
