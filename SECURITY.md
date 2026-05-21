# Security Policy

## Supported Versions

We actively address security vulnerabilities in the current production branch. Older versions are not guaranteed to receive security patches unless explicitly stated in the specific repository.

## Reporting a Vulnerability

**Please do not report security vulnerabilities through public GitHub issues.**

### For Zysk Team Members

If you discover a security vulnerability in any Zysk project, use the private reporting channel appropriate to the project type:

**Client Projects**
- Notify the project lead immediately via Slack DM
- Do NOT commit any fix, workaround, or reference to the issue until discussed with the project lead
- Client security issues are handled on a case-by-case basis with the client

**Internal Tools & Infrastructure**
- Use GitHub's built-in private security advisory feature (see below)
- Or contact the engineering lead directly via Slack

### For External Contributors

Please use **GitHub Private Security Advisories** to report vulnerabilities:

1. Go to the **Security** tab of the affected repository
2. Click **"Report a vulnerability"**
3. Fill in the advisory form with as much detail as possible

This ensures the report is private, tracked, and can be coordinated for responsible disclosure.

## What to Report

Please report immediately:

- Exposed API keys, credentials, or secrets committed to code
- Authentication or authorization bypasses
- SQL injection, XSS, CSRF, or other injection vulnerabilities
- Sensitive data exposure (client data, user data, internal data)
- Vulnerable dependencies flagged as **Critical** severity
- Production database access issues
- Any vulnerability that could affect client systems or data

## Response Timeline

| Step | Target Timeframe |
|------|-----------------|
| Acknowledgement | Within 48 hours |
| Initial assessment | Within 5 business days |
| Fix or mitigation | Depends on severity — Critical within 24h, High within 7 days |
| Disclosure | Coordinated with reporter |

## Security Best Practices for Zysk Repositories

- Never commit secrets, API keys, or credentials — use environment variables
- Add `.env` and credential files to `.gitignore`
- Use `dependabot` for automated dependency updates
- Review Dependabot alerts weekly — address Critical and High within SLA
- Enable branch protection on `main` and `dev` branches
- Require PR reviews before merging to protected branches

---

_This policy applies to all repositories under the Zysk Technologies organization._
_Last reviewed: May 2026_
