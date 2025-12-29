---
name: review-checklist
description: Use when reviewing code for quality, correctness, and security.
---

# Code Review Checklist

## Correctness
- [ ] Satisfies requirements?
- [ ] Edge cases handled?
- [ ] Obvious bugs?

## Style
- [ ] Follows constitution.md standards?
- [ ] Descriptive variable names?
- [ ] No duplicated code?

## Security
- [ ] Inputs validated?
- [ ] No exposed secrets or API keys?
- [ ] SQL injection prevented?

## Output Format
Organize feedback by priority:
1. **Critical** (must fix)
2. **Warning** (should fix)
3. **Suggestion** (consider improving)
