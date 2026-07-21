# Task 002 — Standardize branch names and task language

**Status:** In progress

**Branch:** `002-standardize-branch-names`

**Start date:** 2026-07-21

## Objective

Require every work branch to start with its task number and use English for branch names, commit messages, code comments, and task plans.

## Learning goals

- Understand how naming conventions improve traceability.
- Connect each Git branch to its written task plan.
- Learn why conventions must be specific and verifiable.

## Scope

- Adopt the branch format `NNN-short-english-description`.
- Apply the convention to this branch.
- Translate the task index and existing task plans into English.
- Require English task plans, commit messages, and code comments.
- Move the VILT walkthrough to Task 003.
- Update README workflow references and links.

## Out of scope

- Functional code changes.
- Authentication changes.
- Starting the VILT walkthrough.
- Creating future branches in advance.
- Translating educational and product documentation that is intentionally written in Spanish.

## Steps

- [x] Create the numbered branch for Task 002.
- [x] Rename it to `002-standardize-branch-names`.
- [x] Update the branch convention.
- [x] Translate the task index.
- [x] Translate and rename existing task plans.
- [x] Update README links and workflow guidance.
- [x] Verify that branch names, task plans, and references follow the convention.
- [x] Commit the language standardization.
- [x] Replace the old remote branch with the renamed branch.

## Acceptance criteria

- The current branch is named `002-standardize-branch-names`.
- Branch names start with the matching three-digit task number.
- Branch descriptions, commit messages, code comments, and task plans are in English.
- README and the task index document the same convention.
- All task-plan links resolve to English filenames.
- The next planned task is Task 003.
- No functional code is modified.

## Verification

```bash
git branch --show-current
git diff --check
```
