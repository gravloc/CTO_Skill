---
name: incident-response
description: Respond to outages, security incidents, data leaks or broken deployments. Use immediately when something in production is wrong.
---
## Steps
1. Alert the founder at once with: what, impact, when started.
2. Contain first (disable the feature or access path, rotate exposed keys),
   after founder approval for production actions.
3. Investigate using logs; preserve evidence; do not delete anything.
4. Fix on a branch, test, deploy with approval.
5. Write a short post-mortem: timeline, root cause, fix, prevention.
6. Any possible leak of NDA/ITAR/buyer data goes to the founder as
   a compliance matter (see compliance escalation); do not decide
   notification duties yourself.
7. Log in MEMORY.md.