---
name: code-review-pr
description: Review a GitHub pull request or diff for correctness, security, tests and style. Use when asked to review a PR, branch or code change.
---
## Checklist
1. Does it satisfy the Linear issue's "done means"?
2. Auth: every endpoint has authentication, role check and ownership check.
3. Input validation, file-type/size limits, parameterized queries, no
   secrets, no sensitive data in logs.
4. Audit logging present for document access, RFQ, quote and admin actions.
5. Tests added and meaningful; migrations reversible.
6. Performance: N+1 queries, missing indexes, unbounded lists.
Output: Blockers / Should-fix / Nits / Approve or Request changes.
Post as a PR review comment only after the founder agrees; otherwise
return the review in chat.