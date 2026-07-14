---
type: governance
title: Pattern Validation Matrix
status: active
created: 2026-07-14
updated: 2026-07-14
---

# Pattern Validation Matrix

**This is a tracking asset, not evidence.** It consolidates, in one canonical location, the cross-cycle validation state that `governance/PATTERN_VALIDATION_FRAMEWORK.md` §3 defines — one row per Pattern per revolution — so the same information is not duplicated inside each `PAT-###` file's own text. Per Constitutional Principle 6 ("No second system"), this file *is* the Validation Matrix for all Patterns; it does not coexist with a separate, independently-maintained matrix inside each Pattern file. Populating or changing a cell here does not, by itself, change any Pattern's `status`; status changes still require the process in `governance/PATTERN_VALIDATION_FRAMEWORK.md` §8 and a recorded decision in `governance/DECISIONS.md`.

No Pattern is promoted by this document. No Pattern may be promoted this sprint.

## Matrix

| Pattern | HIS-001 (Steam & Railways) | HIS-002 (Electricity) | HIS-003 (Semiconductor→Internet→Cloud) | Current Status |
|---|---|---|---|---|
| `PAT-001` — Social Value / Investor Return Divergence | Supports (partial) | pending | pending | `draft` |
| `PAT-002` — Capital-Cycle Overbuild | Supports (partial) | pending | pending | `draft` |
| `PAT-003` — Entry Timing and Financing Structure | Supports | pending | pending | `draft` |

## Notes (HIS-001 column, as recorded in the repository)

- **`PAT-001`.** Recorded as `Supports (partial)`, drawn directly from the Pattern's own Pattern Eligibility table ("HIS-001 evidence sufficient: partial") and from `REV-HIST-001`'s H2 verdict ("Social Value Exceeds Investor Value" — partially supported, medium confidence). The divergence is evidenced at the cohort/firm level (York and North Midland Railway) via a two-hop citation, not a single reconciled national accounting of social value against investor return — see `PAT-001`'s own Measurement Cautions section. Not simplified to a bare "Supports": the qualifier is load-bearing.
- **`PAT-002`.** Recorded as `Supports (partial)`, drawn from `PAT-002`'s own Pattern Eligibility table ("HIS-001 evidence sufficient: partial") and `REV-HIST-001`'s H3 verdict ("Overbuild Can Be Economically Productive" — partially supported, medium-low confidence). Both a rational-investment and a speculative-excess interpretation are preserved in `PAT-002` without a forced binary; "overbuild" itself is partly a measured fact (authorized-vs-built gap) and partly a welfare interpretation, per `PAT-002`'s own Measurement Caution.
- **`PAT-003`.** Recorded as `Supports` (not qualified `partial`), drawn from `PAT-003`'s own Pattern Eligibility table ("HIS-001 evidence sufficient: yes") and `REV-HIST-001`'s H5 verdict ("Timing Dominates Category Selection" — supported, medium-high confidence, explicitly the best-supported hypothesis in `HIS-001`). This is deliberately recorded as stronger than `PAT-001`/`PAT-002`'s HIS-001 support, matching what the evidence actually shows rather than flattening all three Patterns to the same rating.

None of the above is a cross-cycle test — `HIS-001` is each Pattern's *originating* revolution, not an independent validation case. The `HIS-002` and `HIS-003` columns are the first genuine tests each Pattern will face.

## How to Read "pending"

`pending` means no `HIS-###` chain (Evidence Ledger → Historical Asset) has been completed for that revolution yet. Per `governance/PATTERN_VALIDATION_FRAMEWORK.md` §3, a cell is populated only once a full evidence chain exists — never from narrative impression or in anticipation of research not yet done. `HIS-002`'s brief (`governance/HIS-002_RESEARCH_BRIEF.md`) defines, in advance, the Supports/Weakens/Rejects/Undecidable criteria each Pattern will be tested against (§8 of that brief) — but no evidence collection has begun, and this matrix will not be updated until `HIS-002`'s own evidence ledger and historical synthesis exist and have passed their respective gates.

## Relationship to Other Governance

- `governance/PATTERN_VALIDATION_FRAMEWORK.md` — defines the lifecycle, the Validation Matrix concept, and promotion requirements this file tracks against. This file does not redefine or duplicate that methodology.
- `governance/HIS-002_RESEARCH_BRIEF.md` §8 — defines the specific per-Pattern validation criteria this matrix's `HIS-002` column will eventually record.
- `governance/WORK_BOARD.md` — the live task tracker; this file is the Pattern-specific cross-cycle view, not a replacement for it.
