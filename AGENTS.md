# liveeasy Agent Operating Rules

These rules are designed for AI coding agents working in liveeasy repositories.
Copy this file into each app repository root when that repository is created.

## Required Startup Check

Before code edits in a repository connected to GitHub:

1. Run `git status --short --branch`.
2. Run `git fetch`.
3. If the current branch is behind upstream, report it and use
   `git pull --ff-only` when safe.
4. If local uncommitted changes exist, do not overwrite, reset, stash, merge, or
   rebase silently.
5. Check this repository's Project or active task list, the linked liveeasy
   Portfolio item, open Issues, and open PRs for overlapping work.

## Conflict Review

Before implementation, state whether another collaborator is working on:

- Same feature
- Same screen or route
- Same data model
- Same API contract
- Same build/config file
- Same release surface

If overlap exists, pause code edits and write the coordination point in the
Issue or PR.

## Work Shape

- One Issue per task.
- One short-lived branch per Issue.
- One PR per branch.
- Draft PR early.
- Keep PRs small enough to review.

## Portfolio Boundary

The organization-level liveeasy Project tracks product-level initiatives and
major decisions. Detailed implementation tasks should live in the relevant app
repository and link back to the portfolio item when applicable.

## Forbidden Without Explicit User Direction

- Force push to shared branches
- `git reset --hard`
- Rebase a shared branch
- Delete remote branches
- Overwrite uncommitted local work
- Change secrets, billing, or organization access
