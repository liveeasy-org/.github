# liveeasy GitHub Defaults

This repository contains the organization-level collaboration defaults for
`liveeasy-org`.

GitHub applies these files to repositories in the organization when a target
repository does not define its own template:

- Issue forms: `.github/ISSUE_TEMPLATE/`
- Pull request template: `.github/pull_request_template.md`
- Contribution rules: `CONTRIBUTING.md`

The operating model is simple:

1. Every code change starts from a GitHub Issue.
2. Before coding, the owner or AI agent checks the repository Project or active
   task list, linked portfolio item, open Issues, open PRs, and latest remote
   branch state.
3. One Issue maps to one short-lived branch and one PR.
4. Important decisions are captured as Issues so both collaborators and agents
   can read the same source of truth.
5. Release work must include test evidence, known risks, rollback path, and
   final approver.

Portfolio Project:

- https://github.com/orgs/liveeasy-org/projects/1

The Portfolio Project tracks product-level initiatives and major decisions. App
repositories should track their detailed implementation work locally and link
back to the relevant portfolio item.

Official GitHub references used for this setup:

- https://docs.github.com/en/communities/setting-up-your-project-for-healthy-contributions/creating-a-default-community-health-file
- https://docs.github.com/en/communities/using-templates-to-encourage-useful-issues-and-pull-requests/syntax-for-issue-forms
- https://docs.github.com/en/communities/using-templates-to-encourage-useful-issues-and-pull-requests/creating-a-pull-request-template-for-your-repository
