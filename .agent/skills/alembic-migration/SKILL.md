---
name: alembic-migration
description: >-
  For authoring, testing, and reviewing Alembic migration scripts.
---

# alembic-migration

## Scope
Use this skill for generating, modifying, or reviewing Alembic (Python/SQLAlchemy) migrations.

## Guidelines
1. **Autogenerate**: Use `alembic revision --autogenerate` as a starting point, but always manually review the generated script to ensure accuracy.
2. **Down Revisions**: Ensure the `upgrade()` and `downgrade()` functions are perfectly symmetrical.
3. **Data Migrations**: Separate schema migrations from data migrations where possible, or clearly document data transformations within the script.
4. **Naming**: Use descriptive messages for the migration (e.g., `alembic revision -m "add user status column"`).

## Verification
- Test the migration using `alembic upgrade head` and `alembic downgrade -1` to ensure reversibility and correctness.
