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
**Verdict: PASS WITH CONDITIONS**

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

> **Provenance note.** The handoff task referenced six escalation triggers from the Research Architect's review but did not transcribe their verbatim text into the handoff package. Per the project's no-fabrication rule (`governance/OPERATING_PRINCIPLES.md`), the conditions below are **reconstructed by the Repository Operator** from the brief, the Pattern Validation Framework, and `DEC-012` — they are *not* the Research Architect's verbatim wording and must be confirmed (or replaced with the original text) at the Gate 1 re-review before Gate 2 opens.

During `HIS-002` evidence collection (Stage A onward, once unblocked), Claude Code must escalate to the User (Investment Committee) / Research Architect rather than deciding alone if any of the following occur:

1. A source load-bearing for one of §8's four-outcome tests for any Pattern has no open-access substitute after a genuine search (per the `HIS-001` U5 paid-access trigger, applied here).
2. The US-only boundary (§2, DEC-012 §11.3) cannot be honored for a load-bearing test — i.e., only non-US evidence exists for a claim the validation depends on — rather than silently importing a non-US case as a de facto second validation row.
3. Evidence would force a change to the primary research question (§1) or the scope (§2) themselves, as opposed to simply returning a Weaken/Reject/Undecidable verdict on a Pattern (which are all expected, in-process outcomes).
4. The Anti-Confirmation Rule (§8.4) cannot be satisfied for a Pattern — i.e., no serious Weaken/Reject search is possible for lack of the relevant data — which should be recorded as an Undecidable disposition, not worked around.
5. The operating-company vs. holding-company separation (§7) cannot be maintained from the available sources, threatening to collapse the two into a single "utility sector return" figure the brief forbids.
6. Any attempt (by any agent) to promote a Pattern, create `MAP-001`/`THS-001`, or begin AI-era mapping on the strength of `HIS-002` evidence before both the Single-Cycle Pattern Validation (HIS-001) gate and the cross-cycle process in `governance/PATTERN_VALIDATION_FRAMEWORK.md` have been satisfied.

## Status

**PASS WITH CONDITIONS — 8 revisions applied in this change set; Gate 1 re-review pending.** The Gate 1 re-review prompt is held in the agent-handoff task `2026-07-14_his-002-gate1-revisions-apply.md` (reply zone) for the User to route to the Research Architect. Evidence collection, Source Register, Evidence Ledger, and historical synthesis remain blocked until (a) the re-review confirms **PASSED**, and then (b) the Single-Cycle Pattern Validation (HIS-001) gate passes, per `DEC-012` §11.2. No Pattern is promoted by this review; `PAT-001`–`PAT-003` remain `status: draft`, `confidence: low`.
