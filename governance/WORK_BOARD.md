---
type: governance
title: Work Board
status: active
created: 2026-07-12
updated: 2026-07-14
---

# Work Board

Single tracker for all research task state. Update this file in the same change set as any substantive repository change.

## Active

### Sprint 1 — HIS-002 Research Design / Pattern Validation

- **Owner:** claude-code (Research Executor)
- **Current step:** Research design only. [`governance/HIS-002_RESEARCH_BRIEF.md`](HIS-002_RESEARCH_BRIEF.md) (`id: HIS-002-BRIEF`) drafted: primary research question, bounded geography (United States, chosen for institutional diversity from HIS-001's British frame) and time period (c. 1900–1935), included/excluded infrastructure layers, evidence/counter-evidence/failure-case requirements, and explicit Supports/Weakens/Rejects/Undecidable validation criteria for `PAT-001`–`PAT-003`. **No evidence collection has begun.** Three open research-design questions are logged in the brief §11 for Research Architect ruling (vocabulary mapping; Pattern lifecycle sequencing relative to `validated-in-one-cycle`; confirmation of the US-only geography choice).
- **Pattern Validation Framework readiness:** [`governance/PATTERN_VALIDATION_FRAMEWORK.md`](PATTERN_VALIDATION_FRAMEWORK.md) reviewed for internal completeness. One minimum necessary gap closed: §3 now defines how an `Undecidable` cross-cycle result is recorded (Notes column, not a new table column) — the lifecycle, Validation Matrix template, and promotion requirements are otherwise unchanged. Assessed as ready for Research Architect methodology review; that formal sign-off has not yet been separately confirmed (see brief §11).
- **Tracking asset:** [`patterns/PATTERN_VALIDATION_MATRIX.md`](../patterns/PATTERN_VALIDATION_MATRIX.md) created — the canonical cross-Pattern tracking table. HIS-001 column populated from the repository's own existing verdicts (`PAT-001`/`PAT-002`: Supports (partial); `PAT-003`: Supports — not simplified to a uniform rating). HIS-002/HIS-003 columns: pending. All three Patterns remain `status: draft`; none promoted.
- **Next review:** Gate 1 — HIS-002 Research Design Review.
- **Scope:** Research design and Pattern-validation tracking only. No evidence collection, no Source Register, no Evidence Ledger, no historical synthesis, no new or promoted Pattern, no `MAP-001`, no `THS-001`, no AI mapping, no investment recommendation.

## Waiting for Review

_None._

## Backlog

Do not begin these tasks. Listed for sequencing only; Phase 2 runs one task at a time (see `governance/RESEARCH_SCOPE.md`).

### HIS-003

- **Title:** Semiconductors → Internet → Cloud
- **Status:** Not started. Do not begin.

## Done

### HIS-001 — Steam, Railways, and Wealth Creation in the First Industrial Revolution

- **Completed:** 2026-07-14 (marked complete in Sprint 0.1; research content finalized 2026-07-12)
- **Owner:** claude-code
- **Brief:** [`governance/HIS-001_RESEARCH_BRIEF.md`](HIS-001_RESEARCH_BRIEF.md) (`id: HIS-001-BRIEF`)
- **Plan:** [`knowledge/industrial-revolutions/HIS-001_RESEARCH_EXECUTION_PLAN.md`](../knowledge/industrial-revolutions/HIS-001_RESEARCH_EXECUTION_PLAN.md) (`id: HIS-001-PLAN`)
- **Gate 1 Review:** [`governance/HIS-001_GATE_1_REVIEW.md`](HIS-001_GATE_1_REVIEW.md) (`id: HIS-001-GATE-1`) — verdict: PASS WITH CONDITIONS, confirmed PASSED.
- **Source Register:** [`knowledge/industrial-revolutions/HIS-001_SOURCE_REGISTER.md`](../knowledge/industrial-revolutions/HIS-001_SOURCE_REGISTER.md) — full-text verified. ~20 Tier 1 sources fetched and read via curl + pypdf/bs4, upgraded to `verified-open`. All 9 Tier 1 requirements Sufficient-for-Stage-C or Partial, none Blocked. Cash-flow candidate: York and North Midland Railway (dated call schedule a genuine, carried gap). Provincial-market question: partially resolved.
- **Evidence Ledger:** [`knowledge/industrial-revolutions/HIS-001_EVIDENCE_LEDGER.md`](../knowledge/industrial-revolutions/HIS-001_EVIDENCE_LEDGER.md) — Stage C deliverable, **151 claims** (C1–C8). 105 supported / 29 partially-supported / 11 contested / 4 gap / 2 undecidable; 0 ai-era analogy. Gate 2: PASS WITH CONDITIONS.
- **Historical Synthesis:** [`knowledge/industrial-revolutions/REV-HIST-001_STEAM_AND_RAILWAYS.md`](../knowledge/industrial-revolutions/REV-HIST-001_STEAM_AND_RAILWAYS.md) — **Gate 3: PASSED (stable historical asset).** H1–H5 verdicts: H5 supported (medium-high), H2/H3 partially supported, H1 partially supported (supplier side undecidable), H4 undecidable.
- **Candidate Patterns (`status: draft`, `confidence: low`; cross-cycle validation from HIS-002/003 required before promotion):**
  - [`patterns/PAT-001_SOCIAL_VALUE_INVESTOR_RETURN_DIVERGENCE.md`](../patterns/PAT-001_SOCIAL_VALUE_INVESTOR_RETURN_DIVERGENCE.md) — infrastructure can create durable social/downstream value while direct investors see weak, uneven, or negative returns.
  - [`patterns/PAT-002_CAPITAL_CYCLE_OVERBUILD.md`](../patterns/PAT-002_CAPITAL_CYCLE_OVERBUILD.md) — abundant speculative capital can accelerate buildout beyond near-term demand, impairing investors while leaving some productive capacity behind.
  - [`patterns/PAT-003_ENTRY_TIMING_AND_FINANCING_STRUCTURE.md`](../patterns/PAT-003_ENTRY_TIMING_AND_FINANCING_STRUCTURE.md) — entry timing, leverage, and installment-call structure can dominate investor outcome within the same sector.
  - **Pattern Review, both authorized revisions confirmed complete:** `PAT-001`'s Pattern Statement wording (commit `d0b7910`); `PAT-002`'s operational definition of overbuild (already present in its Mechanism section — authorization→subscription→called→paid→expenditure→completed→impaired kept strictly distinct — verified and recorded complete in Sprint 0.1, no file change required).
- **Workflow change — MAP-001 superseded:** the prior authorization to create `MAP-001_RAILWAY_MANIA_AND_AI_INFRASTRUCTURE.md` was withdrawn (`DEC-009`). No AI Mapping work exists or was started. Pipeline is now `Candidate Pattern → Pattern Validation Framework → Cross-cycle Historical Validation → Active Pattern → Historical → AI Mapping → Investment Thesis`. All three candidate Patterns remain `draft`; none may reach `active` until a second historical revolution (`HIS-002` or `HIS-003`) is studied and run through the framework's Validation Matrix. No `MAP-001` or `THS-001` exists.
- **Network prerequisite:** [`governance/ENVIRONMENT_NETWORK_REQUIREMENTS.md`](ENVIRONMENT_NETWORK_REQUIREMENTS.md) — resolved at the proxy/allowlist level.

### Sprint 0 — Repository Consolidation

- **Completed:** 2026-07-13
- Six governance documents created (`PROJECT_STATE.md`, `REPOSITORY_INDEX.md`, `ROADMAP.md`, `DECISION_LOG.md`, `NEXT_ACTION.md`, `REPOSITORY_AUDIT.md`); `DEC-007`–`DEC-010` appended to `governance/DECISIONS.md`. Audit: 0 high, 1 medium-high, 4 medium, 4 low, 1 disclosed-informational finding.

### Sprint 0.1 — Repository Integrity Fix

- **Completed:** 2026-07-14
- Applied the fixes reviewed and authorized from the Sprint 0 audit: unique asset IDs (`HIS-001-BRIEF`, `HIS-001-PLAN`, `HIS-001-GATE-1`); removed nonexistent `related` assets (`PAT-004`, `MAP-001`, `THS-001`) from the brief and execution plan, with outcome annotations reconciling planned vs. actually-drafted Patterns; fixed `THESIS_WORKFLOW.md`'s non-standard `status: locked` → `draft`; rewrote `README.md`'s Status and Core Loop; confirmed `PAT-002`'s "operational definition of overbuild" (the second Pattern Review revision) was already implemented. See [`governance/REPOSITORY_AUDIT.md`](REPOSITORY_AUDIT.md) for fix-by-finding disposition.

### Phase 1 — Repository Foundation

- **Completed:** 2026-07-12
- Governance layer, naming/frontmatter standards, agent roles, work board, and decision log established.
