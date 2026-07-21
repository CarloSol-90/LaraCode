# Task 001 — Professional initial publication

**Status:** Completed

**Branch:** `main` (initial publication exception)

**Start date:** 2026-07-21

## Objective

Publish LaraCode on GitHub for the first time with a professional presentation, clear documentation, and a sustainable workflow for future development.

## Learning goals

- Understand the difference between a local and a remote repository.
- Understand the relationship between a branch, a commit, and a push.
- Learn how a README presents a technical project.
- Learn how to scope and verify a task before integration.

## Scope

- Add the LaraCode logo to the Welcome page and README.
- Improve the main README.
- Create the task index and initial task convention.
- Document this first task.
- Verify the current project state.
- Configure the requested remote and publish `main`.

## Out of scope

- Domain features.
- Authentication or dashboard redesign.
- CI/CD configuration.
- Production deployment.

## Steps

- [x] Prepare the base VILT project.
- [x] Customize Welcome with the LaraCode identity.
- [x] Add the logo as a versioned asset.
- [x] Write a portfolio-oriented README.
- [x] Define the task workflow.
- [x] Run tests and quality checks.
- [x] Review files included in the commit.
- [x] Configure the correct `origin` remote.
- [x] Create the task commit.
- [x] Publish `main` and verify its upstream.

## Acceptance criteria

- The README explains the real purpose, stack, architecture, installation, and status.
- The logo renders on GitHub through a relative path.
- The README links to a task index.
- `.env`, dependencies, and local builds are not published.
- Tests, lint, types, and build pass.
- `main` is published to `git@github.com:CarloSol-90/LaraCode.git`.
- No unapproved domain features are included.

## Verification

```bash
php artisan test
vendor/bin/pint --dirty
npm run lint:check
npm run format:check
npm run types:check
npm run build
git status
```

## Result

Task completed. Commit `35d53b8` (`docs: prepare LaraCode initial publication`) was published to `origin/main`, and the local `main` branch was configured to track the remote branch. All planned checks passed.
