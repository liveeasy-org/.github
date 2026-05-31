# liveeasy Webcoding Operating Model

This document turns the collaboration method into a reusable team protocol.

## Source of Truth

Use two levels of GitHub tracking.

The organization-level liveeasy Project is the portfolio board. It tracks
product-level initiatives and major decisions.

Each app repository tracks detailed implementation work in its own Issues,
Pull Requests, and optional repository-level Project.

- Portfolio Issues record product intent, ownership, decisions, risk, and links
  to detailed tracking.
- App Issues record implementation scope and acceptance criteria.
- Pull Requests record implementation and review.

## Normal Flow

1. Create or update a portfolio Issue for the product-level initiative.
2. Create detailed app Issues in the relevant repository.
3. Link app Issues and PRs back to the portfolio Issue.
4. Check repository work, portfolio item, Issues, PRs, and remote branches for
   overlap.
5. Claim the detailed Issue by commenting and moving it to In Progress.
6. Create a branch that includes the Issue number.
7. Open a Draft PR early.
8. Keep important implementation decisions in the Issue or PR thread.
9. Keep product-level decisions in the portfolio Issue.
10. Request review.
11. Merge only after acceptance criteria and tests are satisfied.
12. Move the detailed Issue to Done after verification.

## Agent Review Requirement

When either collaborator asks an AI agent to code, the agent should first check
whether the partner is already doing related work.

The agent should report:

- Related open Issues
- Related open PRs
- Potentially conflicting files
- Dirty local files
- Whether the branch is behind remote

## Conflict Levels

- Low: isolated UI copy, docs, or tests
- Medium: same feature area but different files
- High: same screen, route, API, model, build config, or release task

High-risk overlap requires coordination before code edits.

## Decision Records

Use the Decision Record template when a decision changes:

- Product behavior
- App architecture
- Data model
- API contract
- Release policy
- Collaboration policy

Do not bury durable decisions only in chat.
