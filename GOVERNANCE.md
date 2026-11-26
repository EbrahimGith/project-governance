# Governance and Access

[Back to overview](README.md)

## 1. Roles
| Role | Responsibility | Upstream access |
|---|---|---|
| Organization Owner | Organization settings, membership and recovery | Owner; preferably two trusted members |
| Repository Admin | Repository setup, permissions and branch rules | Admin on assigned repositories |
| Project Maintainer | Issues, project decisions, approved merges and releases | Appropriate Write or Maintain access |
| Reviewer | Review and approve PRs independently | Write or higher where required for approval enforcement |
| Contributor (core or external) | Submit issues and changes through forks | Public/read access, or private access as authorized |

One person may hold several roles. Assign roles per project. Any team member may be nominated as a reviewer; only authorized reviewers count toward required approval. Maintainers and admins also use forks for their own contributions.

## 2. Repository protection
Configure GitHub rulesets or branch protection for `main` and any project-defined protected branches:
- Require PRs and at least one independent approval.
- Require applicable CI checks and resolved review conversations.
- Block force pushes and branch deletion; restrict bypass permissions.
- Limit merge authority to designated maintainers where supported.

GitHub permissions and enforcement vary by plan and repository visibility. Write access can permit upstream branch creation or merging; fork-only development is a team policy, not automatically enforced by requiring PRs. Verify settings and document any manual controls. Private forks require appropriate access and enabled forking.

## 3. Basic security and continuity
- Use individual accounts and enable two-factor authentication; do not share passwords.
- Keep access limited to what each role needs.
- Keep secrets out of Git and public issues. Report security issues privately.
- Do not run untrusted fork PR code with privileged credentials or deployment access.
- Assign a backup maintainer and document how to run and restore hosted projects.
- Record significant concerns and mitigation in the project proposal or a tracking issue; a separate risk register is not required for v1.

## 4. Decisions and policy changes
The core team agrees on new projects, maintainers and policy changes. Record decisions in GitHub issues or PRs. Review access when members join or leave.

## 5. To finalize before adoption
- Organization owners, repository admins and reviewer groups.
- Repository visibility and license choices.
- Approval of this draft by the team.
- Verification of GitHub plan, forking permissions and branch protection.
