# Security Policy - Zysk Technologies

## Our Security Commitment

At Zysk Technologies, security isn't just about code—it's about protecting our clients' trust and our reputation built over 11 years.

## For Zysk Team Members

### Reporting Security Issues

If you discover a security vulnerability in any Zysk project:

**1. Client Projects:**
- Immediately notify the project lead via Slack DM
- Email: nagendra.kv@zysk.tech with subject: `[SECURITY] [Client Name] - Brief Description`
- Do NOT commit any fixes until discussed with project lead
- Client security issues are handled on a case-by-case basis

**3. Internal Tools/Infrastructure:**
- Email: nagendra.kv@zysk.tech, shilpa@zysk.tech

### What Constitutes a Security Issue?

**Report immediately:**
- Exposed API keys, credentials, or secrets in code
- Authentication/authorization bypasses
- SQL injection, XSS, or other injection vulnerabilities
- Data exposure (client data, user data, internal data)
- Vulnerable dependencies flagged as CRITICAL by Dependabot
- Production database access issues

**Not security issues (but still important):**
- General bugs → Use bug report template
- Code quality issues → Raise in code review
- Performance problems → Discuss with team lead

### Security Response Process

1. **Acknowledgment:** Within 1 hour
2. **Assessment:** Project lead evaluates severity
3. **Action:** 
   - Client projects: Coordinate with client as needed
   - Internal tools: Based on impact
4. **Post-fix:** Team review to prevent similar issues

## Daily Security Practices

### Before You Commit

- [ ] No hardcoded credentials (API keys, passwords, tokens)
- [ ] No client-specific data in code comments
- [ ] `.env` files are in `.gitignore`
- [ ] Sensitive configuration uses environment variables

### Code Review Checklist

When reviewing PRs, watch for:
- Exposed secrets or credentials
- SQL queries without parameterization
- User input not validated/sanitized
- Authentication/authorization logic changes
- New dependencies (check Dependabot alerts)

### Dependabot Alerts

Dependabot is enabled org-wide. When you receive an alert:

**Critical/High severity:**
1. Review the alert within 4 hours
2. Update dependency or discuss alternative fix with team
3. Test thoroughly before merging
4. Deploy fix within 1 day

**Medium/Low severity:**
1. Include in next regular sprint
2. Batch similar updates together
3. No need for immediate action unless part of active development

## Client Data Protection

**Remember:**
- Client code and data are confidential
- Never share client repository access outside the assigned team
- Client credentials should be in password manager (not GitHub)
- Production database access requires two-person approval

## Security Tools We Use

- **Dependabot:** Enabled on all repos (auto-alerts for vulnerabilities)
- **Code Review:** Mandatory for all production changes

## Questions?

**For security process questions:** nagendra.kv@zysk.tech or ask in team standup

---

**Last Updated:** January 2026  
**Maintained by:** Shilpa VP
