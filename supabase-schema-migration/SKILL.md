---
name: supabase-schema-migration
description: Design or change the Supabase/Postgres schema safely. Use for new tables, columns, RLS policies, indexes or data migrations.
---
## Steps
1. Read existing schema and MEMORY.md data-model notes first.
2. Write a SQL migration file in the repo with up and rollback.
3. Include RLS policies, indexes, constraints, and audit columns
   (created_at, updated_at, created_by).
4. Test on dev/branch database only. NEVER run against production without
   explicit founder approval.
5. Open a PR with the migration and an impact note (data loss? downtime?).
6. Destructive changes (drop, truncate, type change) always need approval.