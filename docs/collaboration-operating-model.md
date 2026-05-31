# liveeasy Webcoding Operating Model

This document turns the collaboration method into a reusable team protocol.

## Source of Truth

Use GitHub Issues and the liveeasy Project as the shared planning surface.

- Issues record intent, ownership, decisions, risk, and acceptance criteria.
- Pull requests record implementation and review.
- The Project board shows live status and reduces duplicate work.

## Normal Flow

1. Create an Issue with the correct template.
2. Check Project, Issues, PRs, and remote branches for overlap.
3. Claim the Issue by commenting and moving it to In Progress.
4. Create a branch that includes the Issue number.
5. Open a Draft PR early.
6. Keep important decisions in the Issue or PR thread.
7. Request review.
8. Merge only after acceptance criteria and tests are satisfied.
9. Move the Issue to Done after verification.

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
