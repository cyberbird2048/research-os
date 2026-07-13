---
id: PAT-002
type: pattern
title: Capital-Cycle Overbuild
status: draft
created: 2026-07-12
updated: 2026-07-12
owner: cyberbird
research_lead: claude-code
research_architect: chatgpt
review_date: 2026-08-01
confidence: low
sources:
  - HIS-001-EVIDENCE-LEDGER
related:
  - HIS-001
  - HIS-001-EVIDENCE-LEDGER
  - REV-HIST-001
---

# PAT-002 — Capital-Cycle Overbuild

## Pattern Statement

Abundant speculative capital can accelerate infrastructure deployment beyond near-term economic demand, impairing investors while leaving some productive capacity behind. Whether this constitutes "overbuild" in a welfare sense is partly a measured fact and partly an interpretation, and the two must be kept separate.

## Mechanism

Capital committed to a promotional boom moves through distinct, non-interchangeable stages, and a gap can open between any two of them:

**authorization → subscription → called capital → paid capital → expenditure → completed capacity → (unused or failed capacity) → investor impairment / surviving productive infrastructure**

- **Authorization** is a Parliamentary ceiling on what a scheme *may* raise, not a commitment of cash [C-050, C-063].
- **Subscription** is an investor's nominal liability, not cash paid [C-058].
- **Called capital** is the cash a company has actually demanded from subscribers to date — a cumulative figure, not a schedule of specific dated payments [C-057, C-123].
- **Paid (par) capital** is what has actually been received against calls [C-058, C-059].
- **Expenditure** is what the company has actually spent, which can exceed or lag paid capital depending on debt financing [C-051, C-054].
- **Completed capacity** is the mileage/assets actually placed in revenue service, a fraction of what was authorized [C-056].
- **Unused or failed capacity** is authorized or partly-built capacity that was abandoned, never built, or never authorized at all.
- **Investor impairment** and **surviving productive infrastructure** are two separate outcomes that can coexist: capital can be destroyed for investors even where physical capacity built with that capital continues to operate.

The mechanism that produces overbuild-like dynamics is: a **falling minimum-deposit requirement** widens the gap between subscription and paid capital during the boom phase, cheaply inflating headline commitment [C-060, C-059]; construction spending then continues rising for a period *after* market prices have already turned down, because physical buildout has its own lag independent of financing sentiment [C-069].

## Historical Evidence

- **Authorization vastly exceeded what was built.** Nash's end-1848 tabulation: 42 main lines had invested £172m against £268m in Parliamentary authorizations (~64% realized) [C-050]; had every sanctioned Mania-era scheme been executed, mileage would have grown ×5 rather than the ×3 actually realized [C-055]; only about half of Mania-authorized mileage had been built by 1853 [C-056]. Parliament-authorized new mileage itself swung from 810 (1844) to a peak of 4,540 (1846) and collapsed to single digits by 1849–50 [C-063].
- **Subscription outran paid capital during the boom.** In 1844–45, aggregate nominal (subscribed) capital of new schemes rose sharply while paid (par) capital rose only gradually — investors were principally increasing contingent liabilities, not injecting cash [C-059]. This was directly affected by Parliament cutting the minimum deposit from 10% to 5% in February 1844, then restoring it to 10% in July 1845 [C-060].
- **Calls compounded exposure over time.** New-railway median paid-up capital rose from 6.0% (1844–45) to 92.4% (1850) as calls accumulated [C-123]; calls were legally compulsory (sue or forfeit) [C-057].
- **Realized costs exceeded planned costs.** Planned construction costs of ~£15,600–25,000/mile (1845–47 Parliamentary sessions) were exceeded by realized costs of £31,700–35,200/mile (1846–51) [C-054, and the plan-vs-actual comparison in REV-HIST-001 §C].
- **Investment continued rising after prices turned.** Share prices peaked mid-1845 and then fell for four years to a 1849 trough, while actual construction investment kept rising to its own peak in 1847 before declining — a roughly two-year offset between the market signal and physical capital deployment [C-069].
- **Investor impairment coexisted with retained infrastructure.** The Mania-era price index fell 66–70% peak to trough [C-112, C-113, C-120, C-121] while roughly half of authorized mileage was, in fact, completed and remained in service [C-056].

## Supporting Claim IDs

C-050, C-051, C-054, C-055, C-056, C-057, C-058, C-059, C-060, C-063, C-069, C-112, C-113, C-120, C-121, C-123.

## Counter-Evidence

- Contemporaries and modern scholars disagree on whether the "calls" mechanism itself was the primary driver of the price collapse: Campbell's regression finds the change-in-par-value variable statistically significant but with R² under 1%, and both Odlyzko and Campbell conclude calls had only a transitory effect relative to low underlying profitability [C-232] — i.e., financing structure alone does not fully explain the bust.
- The gap between Nash's and a company's own ("LNWR") authorized-liability figures (£40m vs. £30m for the same company) shows that even contemporaries disagreed on what "authorized capital" meant in practice, cautioning against treating any single authorized-capital figure as precise [REV-HIST-001 §C].
- A directly competing estimate of railway investment as a share of GDP (Mitchell 1964: 5.7%/6.7%/4.7% for 1846–48) is substantially lower than the Odlyzko/Nash-derived ~8% figure for 1847, and the discrepancy is unresolved — the scale of the "overbuild" is itself contested, not a single settled number.

## Rational-Investment Interpretation

Completing already-authorized lines, even at a loss to some investors, could reflect rational behavior given sunk costs, competitive pressure to pre-empt rival routes, or genuine (if overestimated) demand expectations. Campbell's finding that share prices tracked short-term dividend expectations consistently, once fundamentals are controlled for, supports reading much of the buildout as a rational (if ultimately mistaken) response to available information rather than pure speculation [C-271, cited in REV-HIST-001 §D].

## Speculative-Excess Interpretation

The scale of promotion (at least 1,000 lines projected [REV-HIST-001 §C]), the gap between authorized and built mileage [C-055, C-056], and the continuation of construction spending well past the point where prices signaled trouble [C-069] together support reading a meaningful portion of the buildout as genuinely excessive relative to any realistic demand estimate — a reading Odlyzko argues directly [C-270, cited in REV-HIST-001 §D].

**Neither interpretation is treated as the sole mechanism.** The HIS-001 evidence supports both operating simultaneously across different segments of the boom (REV-HIST-001 §D) — a genuinely rational core alongside a genuinely excessive tail.

## Boundary Conditions

- Evidenced for a setting with (a) a falling-then-rising minimum-deposit rule that widened the subscription-to-paid gap [C-060], (b) legally compulsory calls [C-057], and (c) a construction process with its own multi-year lag independent of financing sentiment [C-069]. Different financing/legal structures (e.g., no partial-payment mechanism, no compulsory calls) may not exhibit the same dynamic.
- The "half of authorized mileage unbuilt" finding [C-056] is specific to the 1844–1853 window; it is not shown to generalize to other capital cycles without further study.

## Observable Indicators

- A widening gap between authorized/subscribed capital and paid/called capital during the acceleration phase [C-059].
- Rising realized construction cost per unit relative to planned cost [C-054].
- Continued physical investment after a price-based market signal (e.g., a broad asset-price index for the sector) has already turned down [C-069].
- Rising share of paid-up capital over time within newly authorized cohorts, indicating accumulating compulsory exposure [C-123].

## Failure Modes

- Investors compelled to keep funding calls into assets already discounted by the market, unable to exit without loss (Leeds and Thirsk: final call paid in 1848 when the market was already discounting the investment by half) [REV-HIST-001 §G, ledger C-223].
- Entire cohorts of new capital showing negative realized returns even before accounting for leverage (the 1847 authorization cohort: −19.6% leveraged, −2.7% unleveraged) [C-117, cited in REV-HIST-001 §J].
- Schemes authorized but never built, and schemes never even authorized despite active promotion and speculative trading [C-056, C-236, cited in REV-HIST-001 §G].

## Cross-Cycle Validation Requirements

Confirmation requires a second historical revolution (HIS-002 or HIS-003) showing: (a) a measurable gap between authorized/committed capital and actually-completed capacity, (b) investor impairment concentrated in the acceleration/deceleration phase of the cycle, and (c) at least partial retention of built capacity as productive infrastructure after the capital-market correction — with the same discipline of keeping authorized/subscribed/called/paid/expenditure/completed/impaired categories distinct rather than treated as interchangeable.

## Measurement Caution

**HIS-001 does not provide a reliable aggregate UK investor-loss figure and does not quantify one complete investor-capital-to-social-benefit chain.** The authorized/subscribed/called/paid/expenditure figures above are drawn from named contemporary compilations (principally Nash, via Odlyzko) that are not audited totals, and the "overbuild" characterization itself is partly a scholarly interpretation rather than a directly measured welfare judgment [REV-HIST-001 §C].

## Pattern Eligibility

| Criterion | Status |
|---|---|
| Mechanism defined | yes |
| HIS-001 evidence sufficient | partial |
| Counter-evidence included | yes |
| Boundary conditions defined | yes |
| Cross-cycle validation complete | no |
| Eligible for active | no |
