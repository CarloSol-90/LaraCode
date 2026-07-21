# Task Index

This document is the operational source of truth for LaraCode development. Only one functional task should be active at a time.

## Statuses

- **Pending:** work has not started.
- **In progress:** active work exists on its branch.
- **Completed:** acceptance criteria are met, checks have passed, and the task is integrated.
- **Blocked:** a documented decision or external dependency is required.

## Convention

- Identifier: three digits (`NNN`).
- Plan: `docs/tasks/NNN-short-english-description.md`.
- Branch: `NNN-short-english-description`; the plan number must be the first element and the description must be in English.
- Commit: English Conventional Commit style, such as `docs: standardize branch names`.
- Code comments and task documentation must be written in English.
- Each plan must include its objective, learning goals, scope, steps, acceptance criteria, and verification commands.

## Tasks

| ID | Task | Status | Plan |
| --- | --- | --- | --- |
| 001 | Professional initial publication | Completed | [View plan](tasks/001-initial-publication.md) |
| 002 | Standardize branch names and task language | In progress | [View plan](tasks/002-standardize-branch-names.md) |
| 003 | Guided walkthrough of a VILT request | Pending | Create when the task starts |

## Focus rule

Do not combine several features in one task. If new work appears during an active task, register it as a later task instead of silently expanding the current scope.

Valid examples: `002-standardize-branch-names`, `003-trace-vilt-request`. Invalid examples: `task/003-trace-vilt-request`, `feature/003-trace-vilt-request`.
