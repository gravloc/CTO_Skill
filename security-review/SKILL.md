---
name: security-review
description: Security review of a feature, endpoint, schema or document flow. Use before launch, for auth or document-vault changes, and for anything handling NDA, ITAR or buyer data.
---
## Checklist
1. Auth: JWT signing and expiry, refresh rotation/revocation, single-use
   short-lived reset tokens, rate limiting, lockout, email verification.
2. Authorization: RBAC plus ownership checks; Supabase RLS policies on
   every table; no service-role key on the client.
3. Documents: private storage, signed short-lived URLs, access gating by
   buyer status, NDA and ITAR checks, download audit log, virus scan,
   file validation.
4. Uploads and AI pipeline: treat PDFs as hostile; sandbox parsing; guard
   against prompt injection in extracted text; confidence scoring before
   publishing extracted data.
5. OWASP Top 10, secrets scanning, dependency audit, encryption at rest
   and in transit.
6. Output: findings ranked Critical/High/Medium/Low with fix and owner.
   Escalate Critical issues to the founder immediately.