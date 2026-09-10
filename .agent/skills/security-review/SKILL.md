---
name: security-review
description: >-
  For structured security review of execution boundary, egress, grant, and credential changes.
---

# security-review

## Scope
Reviewing code that affects system boundaries, network egress, IAM/grants, or credential management.

## Guidelines
1. **Execution Boundary**: Ensure inputs from external sources are strictly validated and sanitized. 
2. **Egress**: Verify that the application only connects to authorized external endpoints. Ensure timeouts and retries are configured securely.
3. **Grants/IAM**: Follow the principle of least privilege. Do not use wildcard permissions (`*`).
4. **Credentials**: Never hardcode secrets. Ensure secrets are fetched from a secure vault or injected via environment variables.

## Verification
- Audit any changes to network policies or IAM roles.
- Review token scopes and lifetimes for any new authentication mechanisms.
