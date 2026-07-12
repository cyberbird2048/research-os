---
type: governance
title: Decision Log
status: active
created: 2026-07-12
updated: 2026-07-12
---

# Decision Log

Append-only record of governance decisions. Each entry has a unique `DEC-###` ID (see `governance/NAMING_AND_IDS.md`). Decisions are never edited retroactively; a decision that reverses or narrows an earlier one references that earlier `DEC-###` explicitly.

## DEC-001 — GitHub is the single source of truth

- **Date:** 2026-07-12
- **Decision:** GitHub is the canonical, single source of truth for CyberBird Research OS. Obsidian is an optional read view only.
- **Rationale:** A repository that persists on GitHub avoids dependence on any single local tool or device and gives every agent (Claude Code, ChatGPT, Codex) and the User the same authoritative view of state.
- **Status:** In effect.

## DEC-002 — Scope locked to one research task at a time

- **Date:** 2026-07-12
- **Decision:** Phase 2 (Historical Research) runs exactly one task at a time. `HIS-001` (Steam, Railways, and Wealth Creation) is the first and, until further decision, the only authorized task.
- **Rationale:** Prevents research gaps caused by premature breadth. Depth on one complete historical chain is required before a second revolution is opened.
- **Status:** In effect. See `governance/WORK_BOARD.md` — `HIS-002` and `HIS-003` remain in Backlog, not started.

## DEC-003 — Phase 3 locked behind explicit entry gates

- **Date:** 2026-07-12
- **Decision:** Phase 3 (Investment Thesis Engine) may not start until all of the following are satisfied: at least 3 historical revolution research assets, at least 5 cross-cycle validated patterns, at least 3 historical mappings, at least 1 completed monthly review, and a demonstrably stable, repeatable Phase 2 workflow.
- **Rationale:** Prevents the repository from producing investment theses before the underlying historical mechanism has been evidenced and cross-validated.
- **Status:** In effect. See `governance/RESEARCH_SCOPE.md`.

## DEC-004 — "Railway builders were the main winners" is a hypothesis, not a conclusion

- **Date:** 2026-07-12
- **Decision:** The claim that railway builders captured most of the value of the railway era is treated strictly as a hypothesis to test (Challenge A in `governance/HIS-001_RESEARCH_BRIEF.md`), not as an accepted historical conclusion.
- **Rationale:** Corrects an earlier over-simplification identified during research design. Value creation, operating profit, bondholder return, shareholder return, and long-term excess return must be analyzed separately across promoters, railway companies, shareholders, bondholders, suppliers, workers, landowners, and downstream businesses before any winner is named.
- **Status:** In effect. Governs all analysis under `HIS-001`.

## DEC-005 — Claude Code's first deliverable is a plan, not a report

- **Date:** 2026-07-12
- **Decision:** For `HIS-001`, Claude Code's first output is a Research Execution Plan only — question tree, evidence needs, source strategy, file plan, risks and biases, and stopping conditions. No historical narrative or conclusion is drafted at this stage. A mandatory Research Design Review (Gate 1, led by ChatGPT as Research Architect) must pass before evidence collection begins.
- **Rationale:** Enforces the collaboration sequence in `governance/AGENTS.md` (Research Design precedes execution) and prevents Claude Code from producing a polished but unreviewed final report.
- **Status:** In effect. Current work-board state: plan submitted, awaiting Gate 1 review.

## DEC-006 — Governance layer reconstructed from handoff package v1.0

- **Date:** 2026-07-12
- **Decision:** The repository's foundation (governance layer) was reconstructed from handoff package v1.0, because the original foundation files were not present in the GitHub repository — only `README.md` and `CHANGELOG.md` had been committed.
- **Rationale:** `CHANGELOG.md` and `README.md` referenced a completed Phase 1 foundation (constitution, scope, operating principles, naming/frontmatter standards, agent instructions, work board, decision log) that did not exist as files. Governance content was rebuilt from `00_START_HERE/PROJECT_STATUS.md` and `01_CONVERSATION/ORIGINAL_CONVERSATION.md` in the handoff package, and made consistent with the already-present `governance/HIS-001_RESEARCH_BRIEF.md`.
- **Status:** In effect. This reconstruction is itself the action recorded by this decision.

## Notes

- New decisions are appended with the next sequential `DEC-###` ID; existing entries are not renumbered or removed.
- Decisions are the authoritative record of scope and process changes; agents must not treat conversation history alone as sufficient grounds for a scope or process change (see `governance/PROJECT_CONSTITUTION.md`, Precedence).
