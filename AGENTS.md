# liveeasy Agent Operating Rules

These rules are designed for AI coding agents working in liveeasy repositories.
Copy this file into each app repository root when that repository is created.

## Required Chinese Collaboration Rules

- All requirements, bugs, decisions, and release tasks must be created in Chinese
  in the GitHub Project board or linked Issue, then kept in sync with the code
  work.
- Every repository must keep a root `CHANGELOG.md`. Each change must add one
  Chinese line in this format: `YYYY-MM-DD | 类型 | 一句话说明`.
- Use these change types first: `功能`, `缺陷`, `文档`, `配置`, `重构`, `测试`,
  `发布`.
- Commit messages, PR titles, and PR bodies must be written in Chinese.
- PR bodies must clearly state the change type, what changed, verification, and
  the linked Chinese Project item or Issue.
- Repository-specific rules may add more constraints, but must not weaken these
  Chinese collaboration requirements.

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
- Update `CHANGELOG.md` before committing any code or configuration change.

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
