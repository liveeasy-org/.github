# liveeasy Collaboration Rules

These rules apply to all liveeasy app repositories unless a repository has a
more specific local rule.

## 1. Start From an Issue

Do not start coding from a private chat message or an undocumented idea. Create
or update a GitHub Issue first.

The Issue must include:

- Goal
- App or repository
- Owner
- Likely touched files or modules
- Conflict risk
- Acceptance criteria
- Test plan
- Important decisions

## 2. Check for Partner Overlap Before Editing

Before editing code, check:

- This repository's Project board or active task list
- The linked liveeasy Portfolio item when this task belongs to a larger product
  project
- Open Issues
- Open PRs
- The latest remote branch state
- Local dirty changes in the checkout

If another person is touching the same feature, route, screen, data model,
configuration file, build pipeline, or release surface, coordinate in the Issue
before changing code.

## 3. Branch and PR Rule

Use one branch per Issue.

Recommended branch format:

```text
feature/12-login-flow
fix/34-payment-state
release/56-ios-1-2-0
```

Open a Draft PR early when work starts. Link the Issue in the PR body and use
`Closes #123` only when the PR is ready to close the Issue after merge.

## 4. Status Rule

Use repository-level Project status consistently:

- Todo: agreed task, not started
- In Progress: owner is actively editing
- Review: implementation is ready for partner or AI review
- Done: merged and verified

Blocked work must include the blocker, owner, and next action in an Issue
comment.

The organization-level liveeasy Project is the portfolio board. It tracks
product projects and major decisions, not every implementation task.

## 5. Agent Rule

Any AI coding agent must report the overlap check before implementation:

- `git status --short --branch`
- `git fetch`
- Whether the branch is behind upstream
- Open Issues or PRs that overlap the requested work
- Local dirty files that could be affected

Agents must not silently overwrite local changes, force-push, reset, or rebase
shared branches.

## 6. Release Rule

Release tasks must list:

- Changed apps
- Test evidence
- Known risks
- Rollback path
- Final approver
