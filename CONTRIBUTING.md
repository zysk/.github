# Contributing to Zysk Projects

Thank you for contributing to a Zysk Technologies project! This guide covers our standards for all repositories under the [zysk](https://github.com/zysk) organization.

## Table of Contents

- [Code of Conduct](#code-of-conduct)
- [Getting Started](#getting-started)
- [How to Contribute](#how-to-contribute)
- [Branch Strategy](#branch-strategy)
- [Commit Messages](#commit-messages)
- [Pull Request Process](#pull-request-process)
- [Code Standards](#code-standards)

---

## Code of Conduct

All contributors are expected to follow our [Code of Conduct](CODE_OF_CONDUCT.md). Please read it before contributing.

---

## Getting Started

1. **Fork or clone** the repository (external contributors fork; team members clone directly)
2. **Create a branch** from `dev` (or `main` if the project has no `dev` branch)
3. **Set up your environment** following the project's `README.md`
4. **Make your changes** — keep them focused and well-scoped
5. **Test your changes** locally before opening a PR
6. **Open a pull request** using our [PR template](.github/pull_request_template.md)

---

## How to Contribute

### Reporting Bugs

Use the [Bug Report](.github/ISSUE_TEMPLATE/bug_report.yml) issue template. Please include reproduction steps, expected vs actual behavior, and your environment details.

### Suggesting Features

Use the [Feature Request](.github/ISSUE_TEMPLATE/feature_request.yml) issue template. Describe the problem you're solving, not just the solution you have in mind.

### Internal Tasks & Tech Debt

Use the [Task / Tech Debt](.github/ISSUE_TEMPLATE/task.yml) issue template for refactors, cleanups, and non-user-facing improvements.

### Security Issues

**Do not open public issues for security vulnerabilities.** See our [Security Policy](SECURITY.md) for the correct reporting channel.

---

## Branch Strategy

| Branch | Purpose |
|--------|---------|
| `main` | Production-ready code |
| `dev` | Active development, base for feature branches |
| `feature/*` | New features or enhancements |
| `fix/*` | Bug fixes |
| `chore/*` | Maintenance, tooling, non-code changes |

Always branch off from `dev` (or `main` in single-branch projects). Never commit directly to `main`.

---

## Commit Messages

We follow the [Conventional Commits](https://www.conventionalcommits.org/) standard:

```
<type>(<scope>): <short description>

[optional body]

[optional footer]
```

**Types:**

| Type | When to use |
|------|------------|
| `feat` | New feature |
| `fix` | Bug fix |
| `docs` | Documentation only |
| `refactor` | Code restructure, no behavior change |
| `test` | Adding or updating tests |
| `chore` | Build, tooling, config, non-code |
| `perf` | Performance improvement |
| `ci` | CI/CD changes |

**Examples:**

```
feat(auth): add SSO login support
fix(api): handle null response from payment gateway
docs: update deployment instructions in README
chore: upgrade Node.js to 20.x
```

---

## Pull Request Process

1. **Open a PR** against the `dev` branch (or `main` for hotfixes)
2. **Fill in the PR template** completely — summary, type of change, testing notes
3. **Link the related issue** using `Closes #<issue number>`
4. **Request a review** from at least one team member
5. **Address review feedback** — push new commits, do not force-push to open PRs
6. **Squash or merge** as agreed with the reviewer

PRs should be focused and small. A PR that does too many things is hard to review and hard to revert.

---

## Code Standards

Each repository has its own linting and formatting configuration. Before submitting a PR, ensure:

- [ ] No lint errors (`npm run lint` or equivalent)
- [ ] No type errors (`npm run type-check` or equivalent)
- [ ] Code is formatted (`npm run format` or equivalent)
- [ ] Tests pass (`npm test` or equivalent)
- [ ] No new `console.log`, commented-out code, or debug artifacts

---

_This guide applies to all repositories under the Zysk Technologies organization._
_For project-specific guidance, check the `CONTRIBUTING.md` in that repository (if present) which overrides this document._
—
