---
name: db
description: Use for database operations including SQL queries, ORM interactions, and migrations.
---

# Database Operations

## Safety Rules
- Verify migration files before applying
- Confirm backups exist before destructive operations
- Never run DROP or DELETE without explicit user confirmation

## Procedures
- Create: Use ORM schema definitions (Prisma, TypeORM)
- Query: Use parameterized queries to prevent SQL injection
- Migrate: Run in transaction when possible
