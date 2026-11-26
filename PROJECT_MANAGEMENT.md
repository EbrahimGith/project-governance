# Project Management

[Back to overview](README.md)

## 1. Propose a project
Open an issue in `project-governance` using this template:

```markdown
Title: [Proposal] Project name
Purpose / problem:
Expected users:
Initial scope:
Project maintainer and backup:
Public or private:
License / existing open-source dependencies:
Branching strategy: main-only / develop / release-managed
Hosting (if needed):
Key concerns or dependencies:
Definition of done:
```

The team reviews the proposal, agrees on scope and ownership, and records approval in the issue before creating a repository. A shared GitHub Projects board is optional for tracking proposals and active projects.

## 2. Create the repository
An authorized admin creates the repository in Norouz Club.

- Use a short lowercase name, e.g. `meeting-banners` or `open-calendar`.
- Choose public or private visibility deliberately; confirm that forking is permitted before inviting contributors.
- Add a README with purpose, setup instructions, maintainer and contribution rules.
- Choose a license before publishing open-source code; check third-party licenses.
- Document the project branching strategy in its README or `docs/BRANCHING_STRATEGY.md`.
- Enable Issues, assign reviewers and configure branch protection as described in [Governance](GOVERNANCE.md).
- Link the repository to the approved proposal.

## 3. Define issues
Use one issue per feature, bug or meaningful task. Assign an owner when work starts.

```markdown
Title: [Feature / Bug / Task] Short description
Description / expected behavior:
Steps to reproduce (bugs only):
Acceptance criteria:
- [ ] ...
Assignee (if known):
Related issues / dependencies:
```

Suggested labels: `feature`, `bug`, `documentation`, `good-first-issue`.

Suggested workflow: Backlog → In Progress → In Review → Done.

## 4. Choose a branching strategy
| Strategy | Suitable for | Feature PR target | Release flow |
|---|---|---|---|
| Main-only (default) | Small HTML sites and tools | `main` | Tag or publish from `main` |
| Develop | Projects needing integration testing | `develop` | Reviewed PR to `main` |
| Release-managed | Projects needing staged QA | `develop` | `release/*` from `develop`, QA, reviewed PR to `main`, sync release fixes back to `develop` |

Record the chosen strategy, protected branches, PR targets and release process in each repository. All contributors use forks regardless of strategy. Maintainers create official integration/release branches as administrative work, not as a shortcut for unreviewed changes.

Deployment is optional: GitHub Pages, Coolify or another platform may be used as appropriate. For hosted services, document deployment, rollback and backup steps.

## 5. Project onboarding and templates
Use the [template folder](templates/README.md) when creating a project. Copy `ONBOARDING.md` and `BRANCHING_STRATEGY.md` into the new repository and complete the placeholders before inviting contributors. The maintainer keeps onboarding instructions current. Copy issue and PR templates into `.github/` as needed. Link onboarding from the project README. Never include actual secrets.
