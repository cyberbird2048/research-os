---
type: workflow
title: Git Workflow
status: active
created: 2026-07-12
updated: 2026-07-12
---

# Git Workflow

GitHub is the canonical source of truth for CyberBird Research OS (see `governance/PROJECT_CONSTITUTION.md`). Durable research state lives in this repository, not in chat history or external notes.

## Branching

- One branch per research task.
- Branch naming pattern: `research/<TASK-ID>-<short-slug>`, e.g. `research/HIS-001-steam-railways`, or a session-assigned branch name where a task ID is not yet available.
- Do not mix work for multiple tasks on the same branch unless it belongs to the same review gate.

## Required Bookkeeping

Every substantive change (new asset, status change, gate pass/fail, evidence added) must update, on the same branch:

- `governance/WORK_BOARD.md` — task status, claimed owner, current gate
- `CHANGELOG.md` — one-line entry describing what changed and why

A pull request without these updates is incomplete.

## Pull Requests

- All changes to research assets, templates, and governance files go through a pull request. No direct commits to `main`.
- PRs use `.github/PULL_REQUEST_TEMPLATE.md` in full; sections must not be deleted.
- The PR description must state which review gate (Gate 1–5, or none) the change targets.

## Review Gates Before Merge

- A PR that advances a research asset past a review gate (see `workflows/RESEARCH_WORKFLOW.md`) must not be merged until the corresponding gate review is complete and recorded.
- Merges of unreviewed research conclusions to `main` are prohibited, even temporarily. If a gate has not passed, the PR stays open or draft.
- The User (Investment Committee) holds final merge authority on any PR that changes thesis or prediction status.

## Commit Hygiene

- Commits are scoped to one logical change where practical.
- Commit messages state what changed and, where relevant, which claim ID, pattern ID, or gate is affected.
- No force pushes to `main`. No history rewriting of merged work.
