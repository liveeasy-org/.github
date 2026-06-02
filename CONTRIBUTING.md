# liveeasy Collaboration Rules

These rules apply to all liveeasy app repositories unless a repository has a
more specific local rule.

## 1. Use Chinese as the Collaboration Language

All liveeasy product work must be recorded in Chinese:

- Project board items
- GitHub Issues
- Commit messages
- Pull request titles and bodies
- `CHANGELOG.md` entries

This keeps product requirements, review notes, and later verification readable
for the full team. Technical identifiers, commands, file paths, and API names
can remain in their original form.

## 2. Start From an Issue or Project Item

Do not start coding from a private chat message or an undocumented idea. Create
or update a GitHub Issue or Project item first, and write it in Chinese.

The Issue must include:

- 目标
- 应用或仓库
- 负责人
- 可能涉及的文件或模块
- 冲突风险
- 验收标准
- 验证方式
- 重要决策

## 3. Check for Partner Overlap Before Editing

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

## 4. Branch and PR Rule

Use one branch per Issue.

Recommended branch format:

```text
feature/12-login-flow
fix/34-payment-state
release/56-ios-1-2-0
```

Open a Draft PR early when work starts. Link the Issue in the PR body and use
`Closes #123` only when the PR is ready to close the Issue after merge.

PR titles and bodies must be written in Chinese. The PR body must state:

- 修改类型：功能、缺陷、文档、配置、重构、测试或发布
- 改动内容
- 验证方式
- 关联的中文看板条目或 Issue

## 5. Changelog Rule

Every app repository must keep `CHANGELOG.md` in the root directory.

Each code, configuration, document, test, or release change must add one Chinese
line:

```text
YYYY-MM-DD | 类型 | 一句话说明
```

Preferred types: `功能`, `缺陷`, `文档`, `配置`, `重构`, `测试`, `发布`.

## 6. Status Rule

Use repository-level Project status consistently:

- Todo: agreed task, not started
- In Progress: owner is actively editing
- Review: implementation is ready for partner or AI review
- Done: merged and verified

Blocked work must include the blocker, owner, and next action in an Issue
comment.

The organization-level liveeasy Project is the portfolio board. It tracks
product projects and major decisions, not every implementation task.

## 7. Agent Rule

Any AI coding agent must report the overlap check before implementation:

- `git status --short --branch`
- `git fetch`
- Whether the branch is behind upstream
- Open Issues or PRs that overlap the requested work
- Local dirty files that could be affected

Agents must not silently overwrite local changes, force-push, reset, or rebase
shared branches.

## 8. Release Rule

Release tasks must list:

- Changed apps
- Test evidence
- Known risks
- Rollback path
- Final approver
