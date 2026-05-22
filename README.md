# Zysk Technologies — Organization GitHub Templates

> Default community health files and workflow automation for all repositories in the [Zysk Technologies](https://zysk.tech) organization.

---

## What Is This Repository?

GitHub automatically applies templates and configuration files from this repository to any repository in the `zysk` organization that does not define its own. This keeps our engineering standards consistent across every project — without requiring each repository to maintain its own copies.

## Repository Contents

| File / Folder | Purpose |
|---|---|
| `ISSUE_TEMPLATE/` | Standardized templates for bug reports, feature requests, and internal task tracking |
| `profile/README.md` | Organization profile page shown on [github.com/zysk](https://github.com/zysk) |
| `workflows/` | Reusable GitHub Actions workflows (AI code review, stale cleanup, PR labeling) |
| `pull_request_template.md` | PR checklist with label taxonomy, linked issues, and review criteria |
| `CONTRIBUTING.md` | Branch strategy, commit conventions, and the full contribution process |
| `CODE_OF_CONDUCT.md` | Standards for respectful collaboration across all Zysk projects |
| `SECURITY.md` | Responsible disclosure policy using GitHub Private Advisories |
| `SUPPORT.md` | Help channels for team members and external contributors |
| `labeler.yml` | Auto-labeling rules for PRs (docs, test, chore, dependencies) |

## How It Works

GitHub's [default community health files](https://docs.github.com/en/communities/setting-up-your-project-for-healthy-contributions/creating-a-default-community-health-file) feature automatically surfaces these files across the organization. When a contributor opens an issue or pull request in any `zysk` repository that lacks its own template, GitHub uses the one defined here.

### For Repository Maintainers

To override any of these defaults at the repository level:

1. Create a `.github/` folder inside the target repository.
2. Place your custom file there (e.g., `.github/CONTRIBUTING.md`).
3. That file takes precedence over this organization-wide version.

### For Contributors

When contributing to any Zysk repository:

- Opening an **issue** — you will be prompted to choose from the available issue templates.
- Opening a **pull request** — the PR description will be pre-filled with the checklist from `pull_request_template.md`.
- All interactions are expected to follow the [Code of Conduct](./CODE_OF_CONDUCT.md).

For detailed guidance on branching, commit format, and the review process, read the [Contributing Guidelines](./CONTRIBUTING.md).

## Automated Workflows

This repository includes reusable GitHub Actions workflows applied organization-wide:

- **AI Code Review** — Triggered on every PR; uses Claude to surface potential issues before human review.
- **Stale Issue Cleanup** — Automatically labels and closes inactive issues and PRs.
- **PR Auto-Labeler** — Applies labels based on changed file paths using `labeler.yml`.

## Questions?

Reach out to [shilpa@zysk.tech](mailto:shilpa@zysk.tech) for any questions.

---

*Maintained by the [Zysk Technologies](https://zysk.tech) Engineering Team.*
