---
name: security-best-practices
description: >-
  For requested security review or secure coding.
---

# security-best-practices

## Scope
General secure coding practices and codebase security reviews.

## Guidelines
1. **OWASP Top 10**: Protect against common vulnerabilities like SQL Injection, XSS, CSRF, and broken authentication.
2. **Dependencies**: Regularly audit and update third-party libraries. Do not introduce dependencies with known vulnerabilities.
3. **Data Protection**: Encrypt sensitive data at rest and in transit.
4. **Error Handling**: Do not leak stack traces or sensitive internal state in API error responses.

## Verification
- Run static application security testing (SAST) tools.
- Ensure all endpoints have proper authorization and authentication checks.
