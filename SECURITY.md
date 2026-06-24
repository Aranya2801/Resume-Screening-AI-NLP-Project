# Security Policy

## Supported Versions

| Version | Supported |
|---|---|
| main (latest) | ✅ |
| older tags | ❌ |

## Reporting a Vulnerability

Please **do not** open a public GitHub issue for security vulnerabilities.

Instead:

1. Use GitHub's [private vulnerability reporting](../../security/advisories/new) feature on this repository, or
2. Email the maintainers (see repository "About" section for current contact) with:
   - A description of the vulnerability and its impact
   - Steps to reproduce
   - Any suggested remediation

We aim to acknowledge reports within 5 business days and to provide a fix or
mitigation timeline within 14 days for confirmed issues.

## Scope

This includes:
- The FastAPI backend (`backend/`)
- The Next.js frontend (`frontend/`)
- The Docker Compose configuration and CI workflows

Out of scope:
- Vulnerabilities in third-party dependencies that already have public CVEs and patches
  (please instead open a PR bumping the dependency, or a normal issue)
- Denial of service via resource exhaustion on self-hosted, unauthenticated demo deployments

## Handling of resume / candidate data

This project processes personal data (names, emails, phone numbers, employment history).
Operators deploying this platform are responsible for their own compliance with
applicable data protection law (e.g. GDPR, CCPA), including:
- Configuring `DATABASE_URL` to a database under their own access control
- Setting a strong, unique `SECRET_KEY` before any non-local deployment
- Not committing real candidate data, `.env` files, or database dumps to version control
