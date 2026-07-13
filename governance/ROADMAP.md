---
type: governance
title: Roadmap
status: active
created: 2026-07-13
updated: 2026-07-13
---

# Roadmap

The phase model is defined in `governance/RESEARCH_SCOPE.md`; this document tracks progress against it and adds the operating detail (entry/exit criteria, sprint-level granularity) that the scope document does not.

## Completed Phases

### Phase 1 — Foundation

**Status: complete** (2026-07-12).

- Exit criteria met: governance layer, naming/frontmatter standards, agent roles, work board, and decision log established; canonical templates for every asset type created.
- No research content was produced in this phase, by design.

## Current Phase

### Phase 2 — Historical Research

**Status: active.**

Entry criteria (met to open this phase): Phase 1 complete.

Progress within Phase 2 so far, task `HIS-001` (Steam, Railways, and Wealth Creation):

- Gate 1 (Research Design Review): PASSED WITH CONDITIONS.
- Stage A (Source Orientation): complete.
- Stage B (Source Acquisition & Verification): complete, full-text verified.
- Stage C (Evidence Ledger): complete, 151 claims.
- Gate 2 (Evidence Sufficiency): PASSED WITH CONDITIONS.
- Historical Synthesis (`REV-HIST-001`): drafted.
- Gate 3 (Historical Stability): PASSED — `REV-HIST-001` is a stable historical asset.
- Candidate Patterns (`PAT-001`–`PAT-003`): drafted, `status: draft`.
- Pattern Review: PASS WITH MINOR REVISIONS — one of two revisions applied; the Pattern Validation Framework insertion superseded further Pattern-review activity before the second revision was specified.
- Pattern Validation Framework: drafted (`governance/PATTERN_VALIDATION_FRAMEWORK.md`), inserted as a new required stage before any Pattern can leave `draft`.
- **Sprint 0 — Repository Consolidation** (current): governance and repository-integrity work only, no new research. In progress.

Exit criteria for Phase 2 (not yet fully met):

- `HIS-001` formally closed (stable synthesis, drafted candidate patterns — done; task itself not yet marked closed on the work board).
- At least one additional historical revolution (`HIS-002` and/or `HIS-003`) taken through the same pipeline, producing at least one Pattern that reaches `cross-cycle-candidate` or better under the Pattern Validation Framework.
- A demonstrated, repeatable Phase 2 workflow — i.e. the pipeline run at least twice without redesign (Phase 3 entry gate requirement; see below).

## Remaining Phases

### Phase 2 (continued) — Second Historical Revolution

Not started. Candidates per the Work Board backlog: `HIS-002` (Electricity & Automobiles) or `HIS-003` (Semiconductors → Internet → Cloud). Blocked until the Research Architect authorizes resuming new research (Sprint 0 explicitly pauses this).

Entry criteria: Sprint 0 consolidation deliverables reviewed and accepted; Research Architect authorization to open a specific `HIS-###` task.

Exit criteria: same Gate 1→2→3 pipeline completed for the new revolution; its Patterns run through the Validation Matrix against `REV-HIST-001`'s Patterns.

### Phase 3 — Investment Thesis Engine

**Status: locked.** Must not start early regardless of apparent readiness of any single asset (per `governance/RESEARCH_SCOPE.md`).

Entry criteria (all required, per `RESEARCH_SCOPE.md`):

- At least 3 completed Historical Revolution Research assets (`REV-HIST-###`). Currently: 1 of 3 (`REV-HIST-001`).
- At least 5 cross-cycle validated Patterns (`PAT-###`) at `active` or better. Currently: 0 of 5 (all 3 existing Patterns are `draft`, single-cycle).
- At least 3 Historical Mappings (`MAP-###`). Currently: 0 of 3 (no Mapping work has started; prior `MAP-001` authorization was withdrawn).
- At least 1 completed Monthly Review (`MR-YYYY-MM`). Currently: 0 of 1.
- A stable, repeatable Phase 2 workflow, evidenced by running it more than once without redesign. Currently: run once (`HIS-001`); not yet demonstrated repeatable.

Exit criteria: first investment thesis (`THS-001`) drafted as an explicitly labeled candidate pending its own mapping's review, per `governance/HIS-001_RESEARCH_BRIEF.md` §9F.

### Phase 4 — Review and Iteration (implied by North Star, not yet formally scoped)

Not yet defined in `governance/RESEARCH_SCOPE.md`. The North Star's fourth step ("review and update those theses through evidence") implies a recurring validation phase once Phase 3 has produced at least one thesis and one prediction (`PRD-###`). This phase should be formally scoped by the Research Architect before Phase 3 exits, not invented ad hoc by Claude Code — flagged here as a planning note only.

## Phase-Change Rule

Scope and phase status may only change via an explicit decision recorded in `governance/DECISIONS.md`, per `governance/RESEARCH_SCOPE.md` §Changing Scope. This roadmap is a tracking view of that decision record, not an independent source of authority.
