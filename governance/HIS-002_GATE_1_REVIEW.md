---
type: governance
title: HIS-002 Gate 1 Research Design Review
status: active
id: HIS-002-GATE-1
created: 2026-07-14
updated: 2026-07-14
related: [HIS-002, HIS-002-BRIEF, DEC-012]
---

# HIS-002 Gate 1 Research Design Review

**Reviewer:** ChatGPT (Research Architect)
**Subject:** `governance/HIS-002_RESEARCH_BRIEF.md` (`id: HIS-002-BRIEF`)
**Verdict: CONFIRMED PASSED**

## Verdict

The `HIS-002` research brief is sufficiently bounded and methodologically serious to proceed, subject to **8 required revisions** (see below). The revisions must be applied, and the revised brief confirmed **PASSED** by a Gate 1 re-review, before `HIS-002` evidence collection begins. Even after Gate 1 is confirmed PASSED, a separate **Single-Cycle Pattern Validation (HIS-001)** gate must pass first — see the §11.2 ruling below and `DEC-012`.

This record captures the Research Architect's Gate 1 review as confirmed by the User (Investment Committee) on 2026-07-14 and routed to the Repository Operator (Claude Code) for application via the agent-handoff task `2026-07-14_his-002-gate1-revisions-apply.md`.

## Rulings on Open Research-Design Questions

The three questions the brief logged as open in §11 were ruled on as follows (recorded in full as `DEC-012`, canonicalized into brief §12):

1. **§11.1 Vocabulary mapping — CONFIRM WITH SIMPLIFICATION.** The Validation Matrix uses only four canonical cross-cycle outcomes: Supports / Weakens / Rejects / Undecidable. "Partially supported" is not a separate matrix outcome; it is permitted only as explanatory prose under `Weakens`. Brief §8 is canonicalized accordingly.

2. **§11.2 Pattern lifecycle sequencing — TWO-STEP, NO CONCURRENT.** Originating-cycle validation (`draft` → `validated-in-one-cycle`) must be determined separately, based solely on `HIS-001` evidence, with its own Research Architect ruling and its own entry requirements (Counter-Evidence Review, falsification condition actively checked, no unresolved load-bearing gap). `HIS-002` supplies only the cross-cycle evidence. A Pattern still at `draft` may be tested cross-cycle, but cannot advance directly to `cross-cycle-candidate`; its originating-cycle deficiencies must be resolved or explicitly recorded first. **Programmatic consequence:** after Gate 1 is confirmed PASSED, an additional review — "Single-Cycle Pattern Validation (HIS-001)" — must be executed and pass before `HIS-002` evidence collection begins. No Pattern is promoted by this ruling.

3. **§11.3 Bounded geography — CONFIRMED.** `HIS-002` is bounded to the United States, c. 1900–1935. No second national system is added. Non-US evidence may be used only for narrow methodological context, not as an additional validation row or substantive comparative case.

## Per-§9-Criterion Assessment

Assessed against the five Gate 1 pass criteria in `governance/HIS-002_RESEARCH_BRIEF.md` §9:

| # | Criterion | Verdict | Justification |
|---|---|---|---|
| 1 | Explicit, evaluable validation criteria for each Pattern before evidence collection | **FAIL** | Criteria existed but used a non-canonical five-label vocabulary, and the Rejected conditions did not distinguish a genuine rejection from mere failure to observe, nor require sufficient data quality — so a Pattern could be wrongly "rejected" on absent evidence. Fixed by Revisions 1–7. |
| 2 | No Pattern verdict pre-decided | **PASS** | No section of the brief asserts or implies a likely outcome for any Pattern; each Pattern retains all four possible verdicts. |
| 3 | Failure-case quota, investor-return requirements, operating-profit/shareholder-return distinction specified precisely | **PASS** | §5 (≥3 named failure cases), §6 (cohort-level return requirement with `undecidable` fallback, no interpolation), and §7 (holding-company vs. operating-company separation) are auditable as written. |
| 4 | Brief does not force `HIS-002` to resemble `HIS-001`'s narrative shape | **FAIL** | The original §8 Supports criteria reproduced `HIS-001`'s empirical shape verbatim (e.g., "mirroring `HIS-001`'s leveraged-vs-unleveraged cohort finding [C-116, C-117]"; "preserving the same authorized → built → utilized → impaired distinctness"), biasing the test toward confirming the railway pattern rather than testing the underlying mechanism. Fixed by Revisions 4–6 and the new §8.4 Anti-Confirmation Rule (Revision 8). |
| 5 | Scope boundaries precise enough to spot an out-of-scope addition on sight | **PASS** | §2 (US-only, c. 1900–1935, explicit included/excluded layers) is precise enough that a reviewer can identify an out-of-scope addition immediately. |

Two of five criteria failed; both are closed by the required revisions below. Criteria 2, 3, and 5 passed as originally drafted.

## Required Revisions (8)

All 8 must be applied to `governance/HIS-002_RESEARCH_BRIEF.md` before Gate 1 is confirmed PASSED. All 8 are applied in the same change set as this review record (see `CHANGELOG.md`, 2026-07-14, and `DEC-012`).

1. **Canonicalize §8 vocabulary to four labels** (Supports / Weakens / Rejects / Undecidable), matching `governance/PATTERN_VALIDATION_FRAMEWORK.md` §3; remove "partially supported" as a separate outcome, permitting it only as explanatory prose under `Weakens`.
2. **§8.1 PAT-001 — rewrite Supports** to require the divergence operate via a mechanism *distinct* from `HIS-001`'s accounting practice, not a reproduction of it.
3. **§8.1 PAT-001 — rewrite Rejected** to require three joint conditions (adequate overlapping evidence; no divergence at either tier; sufficient data quality to rule out rather than merely fail to observe), routing to Undecidable if any condition is unmet.
4. **§8.2 PAT-002 — rewrite Supports** around pre-specified overbuild indicators (capacity vs. demand/utilization; duplicated infrastructure; declining returns on later vintages; abandonment/underutilization; continued investment despite worsening economics) rather than the authorized → built → utilized shape borrowed from `HIS-001`.
5. **§8.2 PAT-002 — rewrite Rejected** so that absence of an authorized-versus-built gap does not by itself reject the Pattern (US utilities may lack Britain's authorization structure), and equity-price decline alone does not establish overbuild.
6. **§8.3 PAT-003 — rewrite Supports** to broaden the dispersion axes (entry cohort, issuance vintage, financing tier, capital structure), require the difference to survive a broad-market-exposure control, and require financing structure or entry price to explain a material portion of the dispersion.
7. **§8.3 PAT-003 — rewrite Rejected** to require adequate cohort/vintage/financing-tier/capital-structure return data after controls, routing to Undecidable if such data cannot be constructed.
8. **Add §8.4 Anti-Confirmation Rule**, binding the eventual `HIS-002` Execution Plan (not merely the brief) to allocate explicit, parallel evidence searches for all four outcomes of each Pattern, with Weaken/Reject evidence sought as seriously as supporting evidence.

The §11 rulings are additionally canonicalized into the brief as a new §12 (Resolved Research-Design Decisions) in the same change set; that recording is the mechanism by which Revisions 1–8 are made binding, and is governed by `DEC-012`.

## Escalation Conditions for Gate 2+

The Research Architect confirmed the following original six conditions verbatim during Gate 1 re-review:

1. No credible utility-sector return benchmark can be constructed for a meaningful portion of 1900–1935.
2. Operating-company and holding-company securities cannot be separated with sufficient reliability.
3. Industrial-electrification productivity evidence and investor-return evidence have no materially overlapping period, making PAT-001 structurally untestable.
4. Generation, transmission, and utilization data cannot be reconciled well enough to test PAT-002 without substituting market-price decline for physical overbuild.
5. No cohort, issuance-vintage, financing-tier, or capital-structure return evidence can be constructed for PAT-003.
6. Evidence collection requires adding a second country, expanding materially beyond 1935, or reincorporating excluded streetcar, residential-appliance, or rural-electrification histories.

## Status

**CONFIRMED PASSED.** All 8 revisions were confirmed correctly applied by the Research Architect. The Single-Cycle Pattern Validation (HIS-001) gate also passed under `DEC-013`; HIS-002 Stage A source orientation is therefore unblocked. No Pattern is promoted by this re-review.
