# Task 005 — Align documentation with the master plan

**Status:** In progress; implementation documentation prepared, integration pending PR review.

**Branch:** `005-align-master-plan`

## Objective

Audit actual code and align product scope, architecture, roadmap and learning workflow without implementing domain features or replacing authentication.

## Learning goals

Distinguish installed tools from delivered features; explain Exercises versus Assessment; connect small tasks to observable acceptance criteria.

## Scope

Update README, project brief, architecture, roadmap, learning plan, decisions, task index and related audit/source documents. Preserve local task 004 planning and existing code. Correct the nonexistent composer analyse command in that plan.

## Steps

1. Inspect code, manifests, lockfiles, routes, models, tests, CI and local changes.
2. Separate current state from MVP and later work; record uncertain details explicitly.
3. Define conceptual module boundaries without creating empty directories.
4. Run available checks, record exact outcomes and inspect the diff.
5. Commit documentation, push the numbered branch and prepare a draft PR.

## Acceptance criteria

- All requested planning documents agree on the MVP, seven formats, five difficulty levels and per-skill mastery 0–100.
- Interviews and practical tests remain within MVP; AWS and Free/Pro remain later.
- No application code, dependencies, authentication or secrets changed.
- Local task 004 work is preserved; no merge to main without approval.
- Unconfirmed taxonomy and assessment formula are identified, not presented as recovered agreements.
- Check results and limitations are recorded in VALIDATION.md.

## Verification commands

```bash
git diff --check
composer ci:check
npm run build
```

Review local Markdown links and changed-file scope. A successful check does not prove educational effectiveness or validate an assessment formula.
