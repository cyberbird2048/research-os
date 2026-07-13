---
type: governance
title: Work Board
status: active
created: 2026-07-12
updated: 2026-07-13
---

# Work Board

Single tracker for all research task state. Update this file in the same change set as any substantive repository change.

## Active

### Sprint 0 — Repository Consolidation

- **Owner:** claude-code
- **Current step:** Complete. Six governance documents created/updated (`PROJECT_STATE.md`, `REPOSITORY_INDEX.md`, `ROADMAP.md`, `DECISION_LOG.md`, `NEXT_ACTION.md`, `REPOSITORY_AUDIT.md`), plus `DEC-007`–`DEC-010` appended to `governance/DECISIONS.md`. Awaiting Research Architect review of the audit findings and a decision on the next sprint.
- **Scope:** Governance, repository integrity, and operating-system quality only. No research content, no Pattern promotion, no AI mapping, no investment thesis, no new `HIS-###` task.
- **Audit summary:** [`governance/REPOSITORY_AUDIT.md`](REPOSITORY_AUDIT.md) — 0 high, 1 medium-high, 4 medium, 4 low, 1 disclosed-informational finding. No medium/high finding was auto-fixed, per instruction.
- **State snapshot:** [`governance/PROJECT_STATE.md`](PROJECT_STATE.md). **Directory map:** [`governance/REPOSITORY_INDEX.md`](REPOSITORY_INDEX.md). **Phase tracking:** [`governance/ROADMAP.md`](ROADMAP.md). **Handoff:** [`governance/NEXT_ACTION.md`](NEXT_ACTION.md).

### HIS-001

- **Title:** Steam, Railways, and Wealth Creation in the First Industrial Revolution
- **Owner:** claude-code
- **Current step:** Pattern Validation Framework complete; Sprint 0 consolidation complete. Paused — awaiting Research Architect review before `HIS-002`/`HIS-003` or further Pattern/Mapping work.
- **Branch:** `main`
- **Brief:** [`governance/HIS-001_RESEARCH_BRIEF.md`](HIS-001_RESEARCH_BRIEF.md)
- **Plan:** [`knowledge/industrial-revolutions/HIS-001_RESEARCH_EXECUTION_PLAN.md`](../knowledge/industrial-revolutions/HIS-001_RESEARCH_EXECUTION_PLAN.md)
- **Gate 1 Review:** [`governance/HIS-001_GATE_1_REVIEW.md`](HIS-001_GATE_1_REVIEW.md) — verdict: PASS WITH CONDITIONS, confirmed PASSED by Research Architect.
- **Source Register:** [`knowledge/industrial-revolutions/HIS-001_SOURCE_REGISTER.md`](../knowledge/industrial-revolutions/HIS-001_SOURCE_REGISTER.md) — Stage A reviewed PASS WITH CONDITIONS. **Stage B complete, now with full-text verification** (awaiting Research Architect review): after the User opened the environment network allowlist, ~20 Tier 1 sources were fetched and read via curl + pypdf/bs4 and upgraded to `verified-open`. All 9 Tier 1 requirements are Sufficient-for-Stage-C or Partial, none Blocked. Both Gate 2 competing-interpretation pairs confirmed genuine and citation-level from full text. Two full-text corrections applied (Donaldson & Hornbeck result is "moderately larger" 3.22% vs 2.7%, not "more than double"; the Dec-1870 survivorship method belongs to Rule Britannia!, not Before the Cult of Equity); "Brian Mitchell" = B.R. Mitchell resolved. Cash-flow candidate: York and North Midland Railway (partial inputs verified; dated call schedule a genuine gap). Provincial-market question: partially-resolved.
- **Network prerequisite:** [`governance/ENVIRONMENT_NETWORK_REQUIREMENTS.md`](ENVIRONMENT_NETWORK_REQUIREMENTS.md) — **RESOLVED at the proxy/allowlist level** (User widened egress allowlist; curl-over-HTTPS now reaches all Tier 1 hosts). Note: the WebFetch tool itself is still 403 (separate path); verification uses curl + local extraction. SSRN and HathiTrust remain Cloudflare-blocked but have working open substitutes.
- **Evidence Ledger:** [`knowledge/industrial-revolutions/HIS-001_EVIDENCE_LEDGER.md`](../knowledge/industrial-revolutions/HIS-001_EVIDENCE_LEDGER.md) — Stage C deliverable, **151 claims** (C1–C8), each tied to a source read at an exact location. 105 supported / 29 partially-supported / 11 contested / 4 gap / 2 undecidable; 0 ai-era analogy. Gate 2: PASS WITH CONDITIONS.
- **Historical Synthesis:** [`knowledge/industrial-revolutions/REV-HIST-001_STEAM_AND_RAILWAYS.md`](../knowledge/industrial-revolutions/REV-HIST-001_STEAM_AND_RAILWAYS.md) — **Gate 3: PASSED (stable historical asset).** Mechanism-first, structured around the research question (§A–L), ~4,070 words, 75 distinct C-### claim IDs cited, 0 AI-era content. H1–H5 verdicts: H5 supported (medium-high), H2/H3 partially supported, H1 partially supported (supplier side undecidable), H4 undecidable.
- **Candidate Patterns (draft, confidence: low; cross-cycle validation from HIS-002/003 required before promotion):**
  - [`patterns/PAT-001_SOCIAL_VALUE_INVESTOR_RETURN_DIVERGENCE.md`](../patterns/PAT-001_SOCIAL_VALUE_INVESTOR_RETURN_DIVERGENCE.md) — infrastructure can create durable social/downstream value while direct investors see weak, uneven, or negative returns.
  - [`patterns/PAT-002_CAPITAL_CYCLE_OVERBUILD.md`](../patterns/PAT-002_CAPITAL_CYCLE_OVERBUILD.md) — abundant speculative capital can accelerate buildout beyond near-term demand, impairing investors while leaving some productive capacity behind.
  - [`patterns/PAT-003_ENTRY_TIMING_AND_FINANCING_STRUCTURE.md`](../patterns/PAT-003_ENTRY_TIMING_AND_FINANCING_STRUCTURE.md) — entry timing, leverage, and installment-call structure can dominate investor outcome within the same sector.
  - One PAT-001 revision applied per Pattern Review; a second revision (file/wording unspecified) remains an open item, separate from the workflow change below.
- **Workflow change — MAP-001 superseded:** the prior authorization to create `MAP-001_RAILWAY_MANIA_AND_AI_INFRASTRUCTURE.md` is withdrawn. No AI Mapping work exists or was started. The Research Architect has inserted a new stage between candidate Patterns and any Mapping: [`governance/PATTERN_VALIDATION_FRAMEWORK.md`](PATTERN_VALIDATION_FRAMEWORK.md) — new pipeline is `Candidate Pattern → Pattern Validation Framework → Cross-cycle Historical Validation → Active Pattern → Historical → AI Mapping → Investment Thesis`. All three candidate Patterns remain at `draft` under this framework; none may reach `active` until a second historical revolution (HIS-002 or HIS-003) is studied and run through the framework's Validation Matrix.
  - All three derived only from `REV-HIST-001` and the Evidence Ledger; none eligible for `active`; no `MAP-001` or `THS-001` created. Awaiting Pattern Review.

## Waiting for Review

_None._

## Backlog

Do not begin these tasks. Listed for sequencing only; Phase 2 runs one task at a time (see `governance/RESEARCH_SCOPE.md`).

### HIS-002

- **Title:** Electricity & Automobiles era
- **Status:** Not started. Do not begin.

### HIS-003

- **Title:** Semiconductors → Internet → Cloud
- **Status:** Not started. Do not begin.

## Done

### Phase 1 — Repository Foundation

- **Completed:** 2026-07-12
- Governance layer, naming/frontmatter standards, agent roles, work board, and decision log established.
