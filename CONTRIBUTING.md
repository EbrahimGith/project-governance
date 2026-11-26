# Contribution Guide

[Back to overview](README.md)

## 1. Everyone uses forks
In version 1.0, core members, external contributors and maintainers all use the same fork-based contribution workflow. No contributor needs upstream Write access simply to submit code.

## 2. Workflow
1. Find or create an issue and discuss major changes before starting.
2. Fork the Norouz Club repository into your personal GitHub account.
3. Sync your fork with the correct upstream target branch (`main` or `develop`, according to the project).
4. Create a working branch in your fork, e.g. `feature/25-calendar-view`, `fix/26-date-format` or `docs/27-readme`.
5. Make and test changes; push to your personal fork.
6. Open a pull request from your fork to the correct upstream branch.
7. Address feedback and wait for approval and required checks.
8. An authorized maintainer merges the PR. Delete your working branch and sync your fork afterward.

## 3. Pull request template
```markdown
Related issue: #123
What changed:
How it was tested:
Screenshots (if relevant):
```
Use `Closes #123` when merging into the default branch will complete the issue. For other targets, track closure when the change reaches the default branch.

## 4. Review rules
- At least one authorized reviewer other than the author must approve.
- Resolve review comments and pass required checks before merging.
- Request a new review after significant changes.
- Prefer squash merge for feature PRs; follow the project strategy for integration and release PRs.
- AI-generated changes follow the same rules. Never commit credentials, private data or unlicensed third-party code.

## 5. Example
```text
Personal fork: feature/25-calendar-view
                   |
                   | Pull Request + Review
                   v
Norouz Club repository: main (or develop)
```

## 6. AI contribution placeholder
**Status: TBD — future policy.**

Topics to define: AI agents and identities, permitted actions, access to repositories and secrets, disclosure of AI-assisted changes, human review and approval. Until agreed, AI-assisted changes follow the same fork and human-review workflow; no autonomous merge or privileged deployment is authorized by this document.
