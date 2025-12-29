---
name: git
description: Use for version control operations including commits, branching, and pushing code.
---

# Git Operations

## Commit Format
Use Conventional Commits:
- `feat:` - new feature
- `fix:` - bug fix
- `docs:` - documentation
- `refactor:` - code restructuring
- `test:` - adding tests
- `chore:` - maintenance

Forbidden: `wip`, `temp`, vague messages

## Branch Naming
- Feature: `feat/<description>`
- Bugfix: `fix/<description>`
- Hotfix: `hotfix/<description>`

## Commands
```bash
git checkout -b <branch>
git add .
git commit -m "<type>: <description>"
git push origin <branch>
```
