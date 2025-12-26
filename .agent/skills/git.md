# Atomic Skill: Git Operations

> **CONTEXT**: Use this skill when required to interact with version control.

## 1. Commit Standards
- **Format**: Conventional Commits (e.g., `feat: add user login`, `fix: resolve crash`).
- **Forbidden**: `wip`, `temp`, or vague messages.

## 2. Branching Strategy
- **Feature**: `feat/description-of-feature`
- **Bugfix**: `fix/issue-description`
- **Hotfix**: `hotfix/urgent-patch`

## 3. Common Commands
```bash
git checkout -b <branch-name>
git add .
git commit -m "<type>: <description>"
git push origin <branch-name>
```
