---
id: HIS-002-PLAN
type: execution-plan
title: HIS-002 Research Execution Plan — Electricity, Grid Infrastructure, and Industrial Electrification
status: draft
created: 2026-07-14
updated: 2026-07-14
owner: cyberbird
research_lead: claude-code
research_architect: chatgpt
review_date: 2026-08-04
confidence: low
sources: []
related:
  - HIS-002
  - HIS-002-BRIEF
  - HIS-002-GATE-1
  - PAT-001
  - PAT-002
  - PAT-003
  - HIS-001-SCPV
---

# HIS-002 Research Execution Plan — Electricity, Grid Infrastructure, and Industrial Electrification

**Purpose.** This is the operational plan that turns the Gate-1-reviewed `governance/HIS-002_RESEARCH_BRIEF.md` (`id: HIS-002-BRIEF`) into a concrete evidence-collection design. It is a plan, not a research result. **No evidence has been collected**; every named source class or candidate below is a *proposed* search direction, not vetted evidence, and no Pattern verdict is asserted or implied. Its defining job, per the User's instruction and brief §8.4, is to specify **explicit, parallel evidence searches for all four cross-cycle outcomes — Supports, Weakens, Rejects, Undecidable — for each of `PAT-001`, `PAT-002`, and `PAT-003`.**

**Do not begin broad evidence collection** until this plan is complete, internally checked against the approved brief, and the Gate 1 re-review is confirmed PASSED.

## 0. Governing Decisions (binding on this plan)

- **Brief §8 / §8.4** — the four-label canonical vocabulary (Supports / Weakens / Rejects / Undecidable) and the Anti-Confirmation Rule this plan implements.
- **DEC-012** — Gate 1 rulings: four-label vocabulary; two-step lifecycle (this is a *cross-cycle* test only); US-only geography, c. 1900–1935.
- **DEC-013 / `HIS-001-SCPV`** — the Single-Cycle Pattern Validation dispositions. This plan tests the **post-SCPV narrowed** form of each Pattern, not the original drafting:
  - `PAT-001`: core = two-ledger divergence (social/downstream value vs. direct-investor return); operating-profit is a supporting sub-mechanism, not a required leg.
  - `PAT-002`: two separated claims — financing-side impairment (supported in HIS-001) and physical overbuild vs. demand/utilization (HIS-001 load-bearing gap).
  - `PAT-003`: `validated-in-one-cycle`; entering formal cross-cycle testing here.
- **`governance/PATTERN_VALIDATION_FRAMEWORK.md`** — §3 (matrix, Undecidable handling), §4 (promotion requirements), §5 (evidence hierarchy), §6 (contradictory-revolution handling). This plan produces exactly one populated cross-cycle row per Pattern (the HIS-002 row); it cannot by itself promote any Pattern to `cross-cycle-candidate` or beyond.

## 1. Primary Research Question

Restated from brief §1 (unchanged): during the buildout and diffusion of US electricity generation and electric-grid infrastructure, and industrial electrification (c. 1900–1935), how did social value creation, infrastructure capital cycles, financing structure, and investor entry timing affect who created value, who captured returns, and who suffered impairment — and what does this evidence do to `PAT-001`, `PAT-002`, and `PAT-003`?

This is a **validation** task. Its output is a cross-cycle verdict per Pattern, not a free-standing history. The question tree below exists only to service the three Pattern tests plus the minimum contextual scaffolding they require.

## 2. Scope (reaffirmed, not re-expanded)

Per brief §2 and DEC-012 §11.3: United States only; c. 1900–1935; included layers = central-station generation, transmission/distribution grid, utility financing structure (incl. holding-company pyramiding), industrial electrification. Excluded: consumer/appliance electrification, post-1935 New Deal rural cooperatives, electric traction/streetcars, any non-US geography, any AI-era content. Non-US material may be cited only for narrow methodological context, never as a validation row or substantive comparative case.

**Budget guardrail (inherited from HIS-001 plan §13 discipline):** if contextual/background research threatens to crowd out the three Pattern tests, cut the background first. This plan's center of gravity is the four-outcome search design in §4, not a general history of US electrification.

## 3. Question Tree

- **QT-A (context, minimal):** What was the shape and timing of US central-station generation and grid buildout, and industrial-motor electrification, 1900–1935? (Only enough to locate the capital cycle and the demand/utilization series the Pattern tests need.)
- **QT-1 (PAT-001):** Did measurable social/downstream value from industrial electrification coexist with weak/uneven/negative direct-investor returns in electric-utility securities, via a mechanism distinct from HIS-001's accounting practice?
- **QT-2 (PAT-002):** (a) Did financing-side capital overcommitment → construction/commitment lag → investor impairment occur? (b) Did physical capacity exceed near-term demand/utilization (the leg HIS-001 could not measure)?
- **QT-3 (PAT-003):** Did realized returns differ materially by entry cohort / issuance vintage / financing tier / capital structure within US electric-utility equities, surviving a broad-market-exposure control, with financing structure or entry timing explaining a material portion of the dispersion?

Each of QT-1/2/3 is worked through the four-outcome search design in §4. QT-A is scaffolding only and is not itself a Pattern test.

## 4. Pattern Test Design — Parallel Four-Outcome Evidence Searches (implements brief §8.4)

For each Pattern, the plan pre-commits to searching for **all four outcomes with equal seriousness**. Evidence that would force a Weaken or Reject verdict is sought as deliberately as supporting evidence; an inability to find decisive evidence in either direction is recorded as Undecidable, not resolved by default toward Supports. Each search lane names (i) what evidence would land that outcome, and (ii) candidate source directions to look in (proposed, access unverified).

### 4.1 PAT-001 — Social Value / Investor Return Divergence

Tested mechanism (post-SCPV): measurable social/downstream value and direct-investor return are distinct ledgers that can diverge materially; operating-profit divergence is corroborating, not required.

| Outcome | What evidence would land this outcome | Candidate source directions (unverified) |
|---|---|---|
| **Supports** | An independently-measured productivity/social-value estimate from industrial electrification that is real and positive, coexisting over an overlapping window with weak/uneven/negative returns to electric-utility security holders — divergence arising via a mechanism *distinct* from HIS-001's accounting practice (e.g., holding-company financial structure). | Productivity-history literature on factory electrification (unit drive vs. line-shaft); a utility-sector equity total-return series spanning 1900–1935 incl. the 1929–1932 collapse; holding-company vs. operating-company return decomposition. |
| **Weakens** | Divergence found only at a narrower boundary (e.g., holding-company tier only, not directly-held conservatively-financed operating utilities), or a social-value estimate too thin/contested to anchor the comparison. | Same sources, segmented by tier; the contested range of electrification productivity estimates. |
| **Rejects** | (All three per brief §8.1) adequate overlapping social-value and investor-return evidence; no material divergence at *either* tier; data quality sufficient to rule out divergence rather than merely fail to observe it. | Return series showing utility investors broadly earned returns commensurate with the era's realized social/productivity value. |
| **Undecidable** | Firm/cohort/productivity data insufficient to characterize the relationship, or insufficient to distinguish Reject from Undecidable per §8.1. | Recorded explicitly (Notes column) if the utility return series or the productivity estimate cannot be obtained at adequate quality. |

### 4.2 PAT-002 — Capital-Cycle Overbuild

Tested mechanism (post-SCPV): **two separate claims.** Claim 1 = financing-side capital overcommitment → construction/commitment lag → investor impairment. Claim 2 = physical capacity exceeding near-term demand/utilization (the HIS-001 load-bearing gap). Equity-price decline alone is **not** evidence for either claim.

| Outcome | What evidence would land this outcome | Candidate source directions (unverified) |
|---|---|---|
| **Supports** | Capital deployment materially outrunning near-term economic absorption, via ≥1 pre-specified indicator (capacity vs. demand/utilization; duplicated infrastructure; declining returns on later vintages; abandonment/underutilization; continued investment despite worsening operating economics), **plus** investor impairment coexisting with retained productive infrastructure. Claim 2 in particular needs direct utilization/demand data. | Generation-capacity vs. output/load-factor series; capital-expenditure series vs. demand growth; holding-company investigation materials on inter-affiliate write-ups and duplicated assets; utility abandonment/receivership records. |
| **Weakens** | Overbuild-like pattern only in a narrow segment (e.g., pyramided holding companies, not municipally-owned systems), or one/more pre-specified indicators materially weak or absent. | Segmented capacity/utilization data by ownership type; regional subsets. |
| **Rejects** | Adequate evidence that capital deployment broadly tracked demand, utilization, and economic returns without material excess under US institutions. **Absence of an authorized-vs-built gap does not reject** (US utilities may lack Britain's authorization structure); **equity-price decline alone does not establish overbuild.** | Load-factor/utilization series showing capacity closely tracked demand; later-vintage operating returns not declining; low abandonment/underutilization. |
| **Undecidable** | Data absent at the granularity needed to test the pre-specified indicators — especially likely for Claim 2 (physical capacity vs. demand), the leg HIS-001 also could not measure. | Recorded explicitly; Claim 1 and Claim 2 may receive *different* outcomes and must be reported separately. |

### 4.3 PAT-003 — Entry Timing and Financing Structure

Tested mechanism: realized returns differ materially by entry cohort / issuance vintage / financing tier / capital structure within the same nominal sector, surviving a broad-market-exposure control, with financing structure or entry timing explaining a material portion of the dispersion. (`validated-in-one-cycle`; this is its first cross-cycle test.)

| Outcome | What evidence would land this outcome | Candidate source directions (unverified) |
|---|---|---|
| **Supports** | Return dispersion by cohort/vintage/financing-tier/capital-structure that remains after controlling for broad-market exposure, with financing structure (candidate: holding-company pyramiding) or entry timing explaining a material portion. | Security-level or tier-level return data across the 1920s buildout and 1929–1932 collapse; holding-company capital-structure/leverage data; issuance-vintage return breakdowns. |
| **Weakens** | Dispersion exists but is not clearly attributable to financing structure or entry timing (e.g., mostly sub-sector or regional), or a materially weaker effect than the criterion requires. | Return data decomposed by region/sub-sector vs. by vintage/tier, to see which axis dominates. |
| **Rejects** | Adequate cohort/vintage/financing-tier/capital-structure return data showing neither entry timing nor financing structure materially explains dispersion after relevant controls. Per brief §8.3, if such data cannot be built to that standard, the result is **Undecidable, not Rejected.** | Return series showing undifferentiated market-beta behavior across vintages/tiers once controls applied. |
| **Undecidable** | No cohort/vintage/financing-tier/capital-structure return data reconstructable for the sector and era (the disposition HIS-001 gave its own YNM cash-flow gap). | Recorded explicitly; this is a live risk given US data availability and must not be resolved toward Supports by assumption. |

### 4.4 Anti-Confirmation Controls (binding on execution)

1. **Balanced search budget.** Each Pattern's four lanes receive comparable search effort; the plan does not front-load the Supports lane. A search log records effort/searches per lane so imbalance is visible at Gate 2.
2. **Reject/Weaken evidence is first-class.** Any evidence that would weaken or reject a Pattern is entered in the ledger with the same rigor as supporting evidence; it is never omitted or downgraded because it is inconvenient (per `OPERATING_PRINCIPLES.md` counter-evidence rule).
3. **Undecidable is a real verdict, not a fallback.** Where data does not exist at the required granularity, the outcome is Undecidable and is recorded in the matrix Notes column (Framework §3); it does not count as Supports and does not advance the Pattern.
4. **No HIS-001-shape confirmation.** A finding "Supports" only if the *mechanism* holds under US institutions — not because the US story superficially resembles the railway story. Boundary-mismatch cases are handled per Framework §6 (narrow the boundary → Weakens, not a forced Supports).
5. **Completeness check before synthesis.** Before any REV-HIST-002 drafting, a checklist confirms each Pattern×outcome lane was actually searched and its result (incl. Undecidable) recorded.

## 5. Source Strategy

Per brief §3 and `OPERATING_PRINCIPLES.md` evidence priority order (primary > company accounts/prices > official statistics > academic economic history > synthesis > popular books):

- **Open-access-first.** Verify access at Stage B by actually reaching the source (the HIS-001 access-status taxonomy applies: `verified-open` / `verified-partial` / `verified-paywalled` / `access-failed` / `not-yet-checked`). Do not label a source `verified-*` on assumption.
- **Candidate source classes (directions only, access unverified):** a US electric-utility equity total-return series (pre-boom → boom → 1929–1932 collapse); the FTC 1928–1935 utility holding-company investigation (as a primary/near-primary source on holding-company structure and leverage, *if* verified accessible and read in full, not assumed); the economic-history literature on factory-electrification productivity (as the social-value estimate, read in full before citation); operating-company financial data (revenue, generating cost/kWh, operating income) kept separate from holding-company shareholder-return data.
- **Paid-access escalation** follows the HIS-001 U5 trigger: escalate to the User only when a source is load-bearing for a §8 outcome test and no open-access substitute exists after a genuine search.

## 6. Evidence Ledger Plan

- File: `knowledge/industrial-revolutions/HIS-002_EVIDENCE_LEDGER.md` (`id: HIS-002-EVIDENCE-LEDGER`), created at Stage C, before any REV-HIST-002 narrative.
- **Claim-ID scheme:** `E-###` (distinct from HIS-001's `C-###`, to keep cross-references unambiguous across the two cycles and the matrix). This is a plan-level naming decision for Gate 2 to confirm.
- Every claim row carries: claim, evidence quote, exact source location, classification (historical fact / quantitative estimate / scholarly interpretation / research inference — **no AI-era analogy permitted**), confidence, counter-evidence (searched-and-found or searched-and-none, never blank), and **which Pattern and which of the four outcomes the claim bears on**. A claim may bear on more than one lane; it is tagged for each.
- No claim from search-snippet-only evidence once full-text access exists (HIS-001 discipline).

## 7. Failure-Case Quota & Survivorship Controls

Per brief §5 and `OPERATING_PRINCIPLES.md`: document **≥3 distinct, named** failure/impairment cases (candidate directions, unconfirmed: a major holding-company collapse in the 1932 utility crisis; ≥1 documented utility holding-company receivership/reorganization; ≥1 quantitative measure of aggregate utility-security price decline through the collapse). A synthesis documenting only surviving/successful utilities is incomplete and cannot pass Gate 3. Failed and impaired investors must be represented in the return evidence, not just survivors.

## 8. Value-Separation Discipline

Per brief §7 and `OPERATING_PRINCIPLES.md` required value separation: operating-company-level metrics (electricity revenue, generating cost/kWh, reported operating income) are tabulated **separately** from holding-company-level metrics (holding-company dividend, holding-company equity price return) at every stage. The two must never be merged into a single "utility sector return" figure. The candidate divergence mechanism for this era (holding-company pyramiding) is explicitly *different* from HIS-001's accounting-practice mechanism and is tested as such, not assumed equivalent.

## 9. Planned Repository Files

Per the brief; no files outside this list without a scope change approved at review.

| File | Created at | Gate |
|---|---|---|
| `knowledge/industrial-revolutions/HIS-002_RESEARCH_EXECUTION_PLAN.md` | now (this file) | Gate 1 re-review + internal check |
| `knowledge/industrial-revolutions/HIS-002_SOURCE_REGISTER.md` (`id: HIS-002-SOURCE-REGISTER`) | Stage A/B | Gate 2 |
| `knowledge/industrial-revolutions/HIS-002_EVIDENCE_LEDGER.md` (`id: HIS-002-EVIDENCE-LEDGER`) | Stage C | Gate 2 |
| `knowledge/industrial-revolutions/REV-HIST-002_*.md` (`id: REV-HIST-002`) | after Gate 2 | Gate 3 |
| `patterns/PATTERN_VALIDATION_MATRIX.md` (HIS-002 column) | after Gate 3 | — (tracking update, not a promotion) |
| `MAP-###` / `THS-###` | **not in HIS-002** | out of scope |

No Pattern file is created or promoted by HIS-002 execution; the cross-cycle result is recorded as one matrix row per Pattern, and any status change is a separate decision under the Pattern Validation Framework, not an automatic consequence of this task.

## 10. Staged Stopping Conditions

Evidence collection for a given Pattern stops when: each of its four outcome lanes has been genuinely searched and its result recorded (including Undecidable); the failure-case quota is met; the operating-vs-holding-company separation is maintained; and further searching is not changing the outcome. Do not continue merely to accumulate sources. A Pattern whose decisive data cannot be found returns Undecidable and stops — it is not kept open indefinitely.

## 11. Risks & Biases

- **Confirmation toward the HIS-001 shape** — the primary risk for a validation task; mitigated by §4.4 and the mechanism-not-shape rule.
- **US data availability for cohort-level returns** — PAT-003's cross-cycle test may return Undecidable if vintage/tier return data cannot be reconstructed; this is an acceptable, pre-authorized outcome, not a failure to be worked around.
- **Holding-company data quality** — inter-affiliate write-ups and pyramiding can make reported figures unreliable; the ledger must flag data-quality caveats rather than treat holding-company reports as clean.
- **Social-value estimate contestedness** — the electrification-productivity literature may be as contested as the railway social-savings literature; represent the range, do not pick a single figure uncritically.
- **Scope drift** — into consumer electrification, traction, or non-US systems; cut on sight per §2.

## 12. What This Plan Does Not Do

No evidence is collected here. No Source Register, Evidence Ledger, or synthesis is created here. No Pattern is created, promoted, or demoted here. No `MAP-###` or `THS-###` is created. No AI-era analogy or investment content appears anywhere in HIS-002 work prior to a separately-authorized Mapping stage. Broad evidence collection begins only after this plan is internally checked against the approved brief and the Gate 1 re-review is confirmed PASSED.
