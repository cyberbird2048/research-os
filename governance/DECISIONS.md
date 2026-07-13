---
type: governance
title: Decision Log
status: active
created: 2026-07-12
updated: 2026-07-13
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

## DEC-007 — Multi-gate evidence pipeline formalized for Phase 2

- **Date:** 2026-07-13
- **Decision:** Historical research tasks proceed through a fixed gate sequence: Gate 1 (Research Design Review) → Stage A (Source Orientation) → Stage B (Source Acquisition & Verification) → Stage C (Evidence Ledger) → Gate 2 (Evidence Sufficiency) → Historical Synthesis → Gate 3 (Historical Stability) → Candidate Pattern drafting → Pattern Review. No stage may be skipped, and no asset is promoted ahead of the gate that governs it.
- **Rationale:** This sequence was designed and run in full for `HIS-001` but had not previously been recorded as a standing decision; recording it now makes it binding on `HIS-002`/`HIS-003` rather than merely a description of what happened once.
- **Status:** In effect. See `governance/WORK_BOARD.md` for `HIS-001`'s completed run and `workflows/RESEARCH_WORKFLOW.md` for the process definition.

## DEC-008 — Pattern lifecycle adopted; no Pattern reaches `active` on single-cycle evidence

- **Date:** 2026-07-13
- **Decision:** Patterns move through six lifecycle states — `draft → validated-in-one-cycle → cross-cycle-candidate → active → stable → archived` — as defined in `governance/PATTERN_VALIDATION_FRAMEWORK.md`. A Pattern derived from a single historical revolution may not be promoted past `draft`/`validated-in-one-cycle` regardless of how well-evidenced that single cycle is.
- **Rationale:** A mechanism observed in one revolution (the steam and railway era) is a hypothesis about recurrence, not a demonstrated pattern, until it is checked against at least one independent revolution. This prevents `PAT-001`–`PAT-003` from being treated as more validated than their evidence base supports.
- **Status:** In effect. Governs all Patterns in `patterns/`, all currently `status: draft`, `confidence: low`.

## DEC-009 — MAP-001 authorization withdrawn; Mapping stage gated behind Pattern Validation

- **Date:** 2026-07-13
- **Decision:** The prior authorization to create `MAP-001_RAILWAY_MANIA_AND_AI_INFRASTRUCTURE.md` is withdrawn in full. No Historical-to-AI Mapping work exists or may begin until at least one Pattern has been run through the Pattern Validation Framework's cross-cycle validation matrix against a second historical revolution.
- **Rationale:** Mapping a single-cycle Pattern directly to the AI era would draw an investment-relevant analogy from an unvalidated mechanism. The Research Architect inserted the Pattern Validation Framework specifically to close this gap before any Mapping work resumes.
- **Status:** In effect. No `MAP-###` file exists in the repository.

## DEC-010 — Repository consolidation sprints required before phase progression

- **Date:** 2026-07-13
- **Decision:** Before Phase 2 opens a second historical revolution, or Phase 3 is approached, a consolidation sprint (the first being "Sprint 0") audits repository integrity — orphaned files, broken references, inconsistent IDs/statuses, stale assets — and produces or refreshes the operating-state documents (`PROJECT_STATE.md`, `REPOSITORY_INDEX.md`, `ROADMAP.md`, `NEXT_ACTION.md`, `REPOSITORY_AUDIT.md`). New research does not resume until the sprint's deliverables are reviewed.
- **Rationale:** The repository grew quickly through `HIS-001`'s full pipeline; without a deliberate consolidation checkpoint, drift (stale cross-references, undocumented state, orphaned files) compounds silently across research cycles.
- **Status:** In effect. Sprint 0 is the first instance; its findings are recorded in `governance/REPOSITORY_AUDIT.md`.

## Notes

- New decisions are appended with the next sequential `DEC-###` ID; existing entries are not renumbered or removed.
- Decisions are the authoritative record of scope and process changes; agents must not treat conversation history alone as sufficient grounds for a scope or process change (see `governance/PROJECT_CONSTITUTION.md`, Precedence).
