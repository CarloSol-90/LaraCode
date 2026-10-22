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
| 002 | Standardize branch names and task language | Completed | [View plan](tasks/002-standardize-branch-names.md) |
| 003 | Guided walkthrough of a VILT request | Completed | [View plan](tasks/003-trace-vilt-request.md) |
| 004 | Create the learning path data model | In progress — planning only; resume after 005 | [View plan](tasks/004-create-learning-path-model.md) |
| 005 | Audit code and align the master plan | In progress — documentation, PR review pending | [View plan](tasks/005-align-master-plan.md) |

## Focus rule

Do not combine several features in one task. If new work appears during an active task, register it as a later task instead of silently expanding the current scope.

Valid examples: `002-standardize-branch-names`, `003-trace-vilt-request`. Invalid examples: `task/003-trace-vilt-request`, `feature/003-trace-vilt-request`.

## Current coordination

Task 005 is a documentation prerequisite, not a second functional implementation. Preserve the existing Task 004 plan and its learning goals; no LearningPath model exists yet. Resume 004 after reviewing this planning update. Do not mark 005 completed before integration or merge main without approval.

## Ordered backlog after 004

Assign numbered plans only when ready to start; these entries are not active tickets:

1. Learning path HTTP/Inertia page, then small course/module/lesson tasks.
2. Confirm seven exercise formats; implement attempt persistence and one format at a time.
3. Skills and reviewed evidence; define the assessment policy with worked examples before implementation.
4. Per-skill mastery 0–100, difficulty 1–5 and explainable recommendations.
5. Public free LaraCodepedia with versioned official references and basic search.
6. Professional case, technical interview practice and practical test with rubrics, within MVP.
7. Visible progress, basic gamification, accessibility and end-to-end MVP verification.
8. After MVP: evaluate Free/Pro and a separately budgeted AWS laboratory.

Each task requires an objective, learning goals, scope/exclusions, dependencies, small steps, observable acceptance criteria and available verification commands. See PROJECT_BRIEF for product scope; unconfirmed format names and assessment thresholds must be resolved before their implementation tasks.
