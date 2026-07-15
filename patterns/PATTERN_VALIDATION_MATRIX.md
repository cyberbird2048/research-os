---
type: governance
title: Pattern Validation Matrix
status: active
created: 2026-07-14
updated: 2026-07-14
related: [PAT-001, PAT-002, PAT-003, HIS-001-SCPV, DEC-013]
---

# Pattern Validation Matrix

**This is a tracking asset, not evidence.** It consolidates, in one canonical location, the cross-cycle validation state that `governance/PATTERN_VALIDATION_FRAMEWORK.md` §3 defines — one row per Pattern per revolution — so the same information is not duplicated inside each `PAT-###` file's own text. Per Constitutional Principle 6 ("No second system"), this file *is* the Validation Matrix for all Patterns; it does not coexist with a separate, independently-maintained matrix inside each Pattern file. Populating or changing a cell here does not, by itself, change any Pattern's `status`; status changes still require the process in `governance/PATTERN_VALIDATION_FRAMEWORK.md` §8 and a recorded decision in `governance/DECISIONS.md`.

No Pattern is promoted by this document. No Pattern may be promoted this sprint.

## Matrix

| Pattern | HIS-001 (originating cycle) | HIS-002 (Electricity) | HIS-003 (Semiconductor→Internet→Cloud) | Current Status |
|---|---|---|---|---|
| `PAT-001` — Social Value / Investor Return Divergence | Supports — core two-ledger divergence; operating-profit leg supporting only (DEC-013) | pending | pending | `draft` (scope narrowed, DEC-013) |
| `PAT-002` — Capital-Cycle Overbuild | Supports for financing-side impairment; physical-overbuild leg = load-bearing gap (DEC-013) | pending | pending | `draft` (DEC-013) |
| `PAT-003` — Entry Timing and Financing Structure | Supports — cohort/index-level, bounded (DEC-013) | pending | pending | `validated-in-one-cycle` (DEC-013) |

**Column semantics.** The HIS-001 column records the **originating-cycle** disposition from the Single-Cycle Pattern Validation Gate (DEC-013), not a cross-cycle test. The canonical four-label cross-cycle vocabulary (Supports / Weakens / Rejects / Undecidable — DEC-012, Framework §3) applies to the HIS-002 and HIS-003 columns, which remain the first genuine cross-cycle tests each Pattern will face.

## Notes (HIS-001 column — Single-Cycle Pattern Validation dispositions, DEC-013)

The Single-Cycle Pattern Validation Gate (`governance/HIS-001_SINGLE_CYCLE_PATTERN_VALIDATION.md`, `id: HIS-001-SCPV`; recorded as DEC-013) formally dispositioned each Pattern against the `HIS-001` evidence:

- **`PAT-001` — remains `draft`, scope narrowed.** Core mechanism narrowed to the two-ledger divergence (measurable social/downstream value vs. direct-investor return); enterprise operating-profit divergence demoted to a supporting sub-mechanism, not a required third leg. Cross-geography, cross-period, and unmatched-cohort limitations preserved. Consistent with `REV-HIST-001`'s H2 verdict (partially supported, medium confidence).
- **`PAT-002` — remains `draft`, load-bearing gap.** Financing-side capital overcommitment → construction lag → investor impairment is supported within HIS-001; physical capacity exceeding near-term demand/utilization is not fully measured (load-bearing gap). Explicit falsification condition added; equity-price decline alone barred as evidence of physical overbuild. Consistent with `REV-HIST-001`'s H3 verdict (partially supported, medium-low confidence).
- **`PAT-003` — promoted to `validated-in-one-cycle`.** Originating-cycle evidence is cohort/index-level and bounded (London-listed railway ordinary equities; 1843–1850; partial-payment/compulsory-call financing; authorization-cohort timing; subscription-to-first-post-authorization-call measurement). YNM money-weighted gap is precision-only, not load-bearing. Explicit falsification statement added. Consistent with `REV-HIST-001`'s H5 verdict (supported, medium-high — the best-supported hypothesis in HIS-001).

`validated-in-one-cycle` is **not** `active` and does not count toward the Phase 3 entry gate's "5 cross-cycle validated Patterns" requirement (`governance/PATTERN_VALIDATION_FRAMEWORK.md` §9). Per DEC-012 §11.2, `PAT-001` and `PAT-002` may be tested cross-cycle while `draft` but cannot advance directly to `cross-cycle-candidate`; `PAT-003` may now enter formal cross-cycle testing through `HIS-002`.

## How to Read "pending"

`pending` means no `HIS-###` chain (Evidence Ledger → Historical Asset) has been completed for that revolution yet. Per `governance/PATTERN_VALIDATION_FRAMEWORK.md` §3, a cell is populated only once a full evidence chain exists — never from narrative impression or in anticipation of research not yet done. `HIS-002`'s brief (`governance/HIS-002_RESEARCH_BRIEF.md`) defines, in advance, the Supports/Weakens/Rejects/Undecidable criteria each Pattern will be tested against (§8 of that brief) — but no evidence collection has begun, and this matrix will not be updated until `HIS-002`'s own evidence ledger and historical synthesis exist and have passed their respective gates.

## Relationship to Other Governance

- `governance/PATTERN_VALIDATION_FRAMEWORK.md` — defines the lifecycle, the Validation Matrix concept, and promotion requirements this file tracks against. This file does not redefine or duplicate that methodology.
- `governance/HIS-002_RESEARCH_BRIEF.md` §8 — defines the specific per-Pattern validation criteria this matrix's `HIS-002` column will eventually record.
- `governance/WORK_BOARD.md` — the live task tracker; this file is the Pattern-specific cross-cycle view, not a replacement for it.
