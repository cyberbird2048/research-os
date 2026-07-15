---
type: governance
title: Single-Cycle Pattern Validation (HIS-001)
status: active
id: HIS-001-SCPV
created: 2026-07-14
updated: 2026-07-14
related: [HIS-001, REV-HIST-001, PAT-001, PAT-002, PAT-003, DEC-012, DEC-013]
---

# Single-Cycle Pattern Validation (HIS-001)

**Reviewer:** ChatGPT (Research Architect)
**Subjects:** `patterns/PAT-001`, `patterns/PAT-002`, `patterns/PAT-003`
**Gate:** Single-Cycle Pattern Validation — the originating-cycle gate introduced by `DEC-012` §11.2. It determines, for each candidate Pattern, whether the `HIS-001` evidence alone supports the mechanism well enough (with its own counter-evidence review, no unresolved load-bearing gap, and an actively-checked falsification condition) to reach `validated-in-one-cycle`, per `governance/PATTERN_VALIDATION_FRAMEWORK.md` §2.

## Gate Verdict

**PASSED.** The gate has been executed and each Pattern has a formal disposition (below). This gate is distinct from, and sits before, cross-cycle testing: passing it does **not** advance any Pattern to `cross-cycle-candidate` — that requires a second, independent revolution (`HIS-002`) run through the Validation Matrix.

## Formal Dispositions

### PAT-001 — Social Value / Investor Return Divergence

**Remains `draft` — scope narrowing applied.**

- Core mechanism narrowed to: *measurable social or downstream value and direct-investor return are distinct ledgers and can diverge materially.*
- Enterprise operating-profit divergence is treated as a **supporting sub-mechanism**, not a required third matched leg of the core Pattern.
- The cross-geography, cross-period, and unmatched-cohort limitations are preserved.
- May be tested in `HIS-002` while `draft`; cannot advance directly to `cross-cycle-candidate` (DEC-012 §11.2).

### PAT-002 — Capital-Cycle Overbuild

**Remains `draft` — load-bearing gap and scope narrowing required (applied).**

- Two claims separated explicitly: (1) financing-side capital overcommitment, construction lag, and investor impairment — **supported** within HIS-001; (2) physical capacity exceeding near-term demand/utilization — **not fully measured** within HIS-001 (load-bearing gap).
- An explicit falsification condition was added, based on capital deployment tracking demand, utilization, later-vintage operating returns, abandonment, underutilization, and impairment.
- Equity-price decline alone must not be described as evidence of physical overbuild.
- May be tested in `HIS-002` while `draft`; cannot advance directly to `cross-cycle-candidate` (DEC-012 §11.2).

### PAT-003 — Entry Timing and Financing Structure

**Eligible for `validated-in-one-cycle` → promoted.**

- Originating-cycle evidence is cohort/index-level and bounded to: London-listed railway ordinary equities; 1843–1850; partial-payment and compulsory-call financing; authorization-cohort timing; subscription-to-first-post-authorization-call measurement.
- The YNM money-weighted return gap remains visible but is **precision-only** for the cohort-level mechanism — not a load-bearing gap for this validation.
- Explicit falsification statement added (verbatim): *"With adequate cohort or vintage data, if return dispersion disappears after controlling for broad-market exposure and financing structure or entry timing explains no material portion of the remaining dispersion, the Pattern is rejected for that cycle."*
- Now eligible to enter formal cross-cycle testing through `HIS-002`.

## Gate Interpretation

- The Single-Cycle Pattern Validation Gate is **PASSED**.
- `PAT-001` and `PAT-002` may be tested in `HIS-002` while still `draft`, but cannot advance directly to `cross-cycle-candidate`.
- `PAT-003` (`validated-in-one-cycle`) may now enter formal cross-cycle testing through `HIS-002`.
- No Pattern reached `active`; `validated-in-one-cycle` does not count toward the Phase 3 entry gate's "5 cross-cycle validated Patterns" requirement (`governance/PATTERN_VALIDATION_FRAMEWORK.md` §9).

## Status

Gate PASSED and recorded as `DEC-013`. Dispositions applied to the three Pattern files and reflected in `patterns/PATTERN_VALIDATION_MATRIX.md`. Next research deliverable: `knowledge/industrial-revolutions/HIS-002_RESEARCH_EXECUTION_PLAN.md`, implementing `governance/HIS-002_RESEARCH_BRIEF.md` §8.4.
