---
name: database-admin
description: >-
  For schema changes, migrations, index reviews, and database integrity work.
---

# database-admin

## Scope
This skill is triggered when performing schema changes, adding or modifying indexes, or ensuring database integrity.

## Guidelines
1. **Schema Changes**: Always ensure backward compatibility. Use additive changes when possible.
2. **Indexes**: Review query execution plans before and after adding indexes. Ensure indexes do not negatively impact write performance excessively.
3. **Integrity**: Enforce data integrity through constraints (foreign keys, unique constraints, NOT NULL).
4. **Transactions**: Ensure that any multi-step database operation is wrapped in a transaction.

## Verification
- Run database migrations in a test environment before applying to production.
- Validate schema changes against existing data to prevent data loss.
