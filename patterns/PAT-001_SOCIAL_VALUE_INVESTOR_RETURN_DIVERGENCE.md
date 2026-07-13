---
id: PAT-001
type: pattern
title: Social Value / Investor Return Divergence
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

# PAT-001 — Social Value / Investor Return Divergence

## Pattern Statement

Infrastructure can create durable social and downstream economic value while direct investors experience weak, uneven, or negative returns. Social value creation, enterprise operating profit, and shareholder return are three distinct measures that need not move together, and a single episode can show all three diverging at once.

## Historical Mechanism

Three sub-mechanisms recur in the HIS-001 evidence:

1. **A downstream/user benefit is realized independently of investor outcomes.** The transport-cost benefit to the wider economy (social savings) is measured at the level of the whole economy, not at the level of the specific investors who financed the specific assets — the two ledgers are not the same ledger.
2. **Reported operating results can diverge from investor economic return.** No separate depreciation was charged on railway assets, and revenue expenditure could be charged to capital instead, letting a company sustain a stable dividend while its underlying return diverged sharply by cohort or vintage [C-188, C-193, C-190, C-191, C-192].
3. **Timing and cohort effects further separate operating performance from realized investor return** (see PAT-003) — meaning even "the same sector" can show simultaneous winners and losers among investors while the aggregate social/technological picture looks uniformly positive.

## Evidence from HIS-001

- **Social value, real but bounded and contested.** US railroads: social saving of ≤2.7% of 1890 GNP under Fogel's partial-equilibrium method (reported via Donaldson & Hornbeck; Fogel's own text not read) [C-272], vs. 3.22% under Donaldson & Hornbeck's general-equilibrium "market access" method — explicitly characterized by the authors as "moderately larger," not a multiple [C-273]. UK passenger social savings (Leunig, revising Hawke) are larger but are a within-method refinement of the same partial-equilibrium approach, not an independent second estimate [C-274].
- **Investor return, weak and uneven over the same broad era.** The railway sector's own 1840s decade total return was +3.7%/yr, carried almost entirely by dividends against a −0.4% capital gain [C-109]; the Mania-era price index fell 66–70% peak to trough [C-112, C-113, C-120, C-121]; sector-wide dividends collapsed to an average 1.9% in 1849 [C-224].
- **Operating-report vs. investor-return divergence within a single firm.** The York and North Midland Railway (YNM) held a flat, round 10% half-yearly dividend across 1845–1847 [C-190] while an independently-sourced (two-hop) estimate puts its return on equity at 10.1% for its pre-Mania network vs. −0.3% for its Mania-era-constructed extensions [C-191] — a single stable reported dividend coexisting with value-destroying investment in the same company [C-192]. This is reinforced by a documented industry practice of charging revenue expenditure to capital to sustain reported dividends [C-193].
- **Broad market context.** Long-run British equity returns over the same century were positive and attractive relative to gilts (5.4%/yr total return, ~2.6 pp premium over Consols [C-107, C-108]; a 4.62%/yr floor even under the most severe survivorship adjustment [C-133]) — so the divergence identified here is a *railway/cohort-specific* finding, not evidence that all 19th-century British investing was unrewarding.

## Supporting Claim IDs

C-107, C-108, C-109, C-112, C-113, C-120, C-121, C-133, C-188, C-190, C-191, C-192, C-193, C-224, C-272, C-273, C-274.

## Counter-Evidence

- Broad UK equity markets delivered positive, gilt-beating returns across the same century [C-107, C-108, C-133] — the divergence is not a claim that investing generally failed to reward capital.
- Established, pre-Mania railway operators earned real operating returns early in the period (~8% dividends at the start of 1847 for a small sample of established lines) [REV-HIST-001 §E, citing the ledger's established-operator evidence] — profitability and investor return were not uniformly weak; they were **uneven**, concentrated in specific cohorts and periods.
- Donaldson & Hornbeck frame their higher social-value estimate as an *extension* of Fogel's method, not a repudiation of it — the two social-value estimates are not in sharp conflict with each other, even though both sit apart from the investor-return evidence [C-273].

## Boundary Conditions

- Evidenced specifically for **UK railway equity investors, primarily London-Stock-Exchange-listed** securities during and shortly after the 1843–1850 Railway Mania, and for **US agricultural social-savings estimates** for 1890 — not demonstrated as a general property of infrastructure investment.
- Depends on accounting conventions of the era (no mandated depreciation, revenue-to-capital reclassification) [C-188, C-193] that are specific to pre-1868 British railway accounting and may not generalize to differently-regulated eras.
- The divergence is documented at the level of *cohorts and individual firms* (YNM), not as a single reconciled national accounting of total social value against total investor return.

## Measurement Cautions

**The HIS-001 evidence chain supporting this pattern is cross-geography and cross-period.** The social-value side draws on US estimates for 1890 [C-272, C-273] and UK passenger-savings estimates spanning 1843–1912 [C-274]; the investor-return side draws on UK railway share-price and dividend data for 1843–1850 [C-109, C-112, C-224]; the firm-level divergence evidence (YNM) is a two-hop citation to unread material [C-191]. This is **not a single UK cohort reconstruction linking specific investor losses to the social value created by those same assets** — no such reconstruction exists in the ledger, and none is claimed here. No reliable aggregate UK investor-capital-loss figure has been established [REV-HIST-001 §5.C].

## Failure Cases

- North British Railway: dividend on common shares eliminated within roughly two years of 1849 despite recent operating performance [C-221].
- Leeds and Thirsk Railway: realized construction costs and revenue both departed sharply from plan (costs ~50% above, revenue ~67% below projection by 1852) [C-222], with shareholders compelled to keep paying calls into an asset the market had already discounted by half [C-223].
- George Hudson's fraud on three of his four controlled lines is the best-established fraud case of the era, though not shown to be representative of the industry as a whole [C-220].

## What Would Validate This Across Another Revolution

- A second historical revolution (HIS-002 or HIS-003) showing an independently-measured social/downstream-value estimate that is real and positive, occurring **at the same time** direct-investor returns in the financing vehicles for that infrastructure are shown to be weak, uneven, or negative, ideally with firm- or cohort-level evidence of the same operating-report-vs.-investor-return gap documented here for YNM.

## What Would Falsify or Materially Weaken the Pattern

- Finding that, once accounting distortions are corrected for, operating profit and shareholder return in fact tracked social value closely in this era (i.e., the apparent divergence was mostly a measurement artifact, not real).
- Finding a reliable aggregate UK investor-loss figure showing investor returns were, in fact, broadly commensurate with social value created (this would require resolving the gap noted in Measurement Cautions).
- A second revolution in which social value and investor return move together, with no comparable divergence — this alone would not falsify a "can diverge" pattern, but would weaken confidence that the mechanism is common rather than an idiosyncrasy of 1840s British railway accounting and financing structure.

## Pattern Eligibility

| Criterion | Status |
|---|---|
| Mechanism defined | yes |
| HIS-001 evidence sufficient | partial |
| Counter-evidence included | yes |
| Boundary conditions defined | yes |
| Cross-cycle validation complete | no |
| Eligible for active | no |
