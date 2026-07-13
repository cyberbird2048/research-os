---
id: REV-HIST-001
type: historical-research
title: Steam, Railways, and Wealth Creation in the First Industrial Revolution
status: draft
created: 2026-07-12
updated: 2026-07-12
owner: cyberbird
research_lead: claude-code
research_architect: chatgpt
review_date: 2026-08-01
confidence: low
sources:
  - HIS-001-SOURCE-REGISTER
related:
  - HIS-001
  - HIS-001-EVIDENCE-LEDGER
  - PAT-001
  - PAT-002
  - PAT-003
  - PAT-004
  - MAP-001
---

# REV-HIST-001 — Steam, Railways, and Wealth Creation

**Scope note.** This is a historical asset derived from `HIS-001_EVIDENCE_LEDGER.md`. Every material conclusion cites ledger claim IDs (`C-###`). No material factual claim appears here that is not in the ledger; where the evidence is thin, the conclusion is weakened, marked unresolved, or omitted. **No AI-era analogy, mapping, pattern, or thesis appears in this document** — those are later stages. The candidate `PAT-*`/`MAP-001` IDs in the frontmatter are placeholders for traceability only; no such files exist.

**Confidence convention.** Conclusions carry an explicit confidence (low / medium / high) and a classification inherited from the ledger. "Two-hop" marks a claim whose ultimate source was not read directly (see §5.D).

---

## A. Executive Answer

The steam-and-railway era is the clearest available case of a technology that was **transformative in importance, real but bounded in social value, uneven in enterprise profitability, and sharply timing-dependent in investor return** — five things that the evidence requires be held apart.

**1. Who created economic value?** Steam and railways created real aggregate value, but the measured productivity contribution was *modest and heavily delayed*. Steam did not reach parity with water power until 1830, ~60 years after Watt, and was then only ~1.5% of the capital stock [C-001]; its peak growth-accounting contribution (steam + railways) was ~0.38 pp/yr in 1850–70 [C-007], with railways alone ≤0.26 pp/yr despite a capital stock worth 30% of GDP by 1855 [C-008]; the lag to peak impact was ~80 years [C-009] with "no equivalent to Moore's Law" [C-010]. Social value (a distinct measure) was real but bounded and contested: for US railroads, 2.7% of 1890 GNP (Fogel) to 3.22% (Donaldson & Hornbeck), explicitly "moderately larger," not double [C-272, C-273]; UK passenger social savings were larger but are a within-method refinement debate (Hawke→Leunig) [C-274]. **Confidence: medium. Classification: technological importance and social value creation — held separate from any return measure.**

**2. Who captured operating profit?** Established pre-Mania railway operating companies were the clearest operating-profit earners in the early phase (Fig-3 lines ~8% dividends at start of 1847 [C-233]; YNM's pre-Mania network ~10.1–14% return on shareholders' funds, two-hop [C-191, C-229]). But reported operating profit of this era is contaminated: railways charged no separate depreciation [C-188] and "closed the capital account," charging revenue expenditure to capital to sustain dividends (SER: £150,000 ≈ 30% of dividends over three years) [C-193]. By the later period (1870–1912) even the 15 largest companies' return on capital employed had eroded to ~4.3–4.6% [C-187]. **Confidence: medium, with an explicit accounting-quality caveat.**

**3. Who earned attractive investor returns?** This is where "winners" language most often fails. Broad long-run British equity returns were positive and attractive relative to gilts — 5.4% average total return 1830–1929, almost all from dividends, an equity premium of ~2.6 pp over Consols [C-107, C-108], and even under the most severe survivorship adjustment 4.62%/yr for 1825–70 [C-133]. But *railway* investor experience was timing-dominated: the boom-entry authorization cohorts of 1844–45 earned high **leveraged** realized returns (+57.5%, +36.0%), the 1846 cohort +21.8%, and the 1847 cohort *lost* (−19.6%) [C-117]; and the railway sector's own 1840s decade total return was only +3.7%, dividend-carried against a −0.4% capital gain [C-109]. The dramatic headline gains were overwhelmingly a partial-payment leverage artifact — stripped of leverage, peak price/par ratios were near parity (1.24–1.29) [C-116]. **Confidence: medium-high for the timing/leverage finding; the level of a representative money-weighted railway return is `undecidable` (§5.A).**

**4. Who lost money?** Late/top-of-boom entrants and holders of new Mania schemes: the all-railway price index fell 66–70% peak-to-trough [C-112, C-113, C-120]; the 1847 cohort lost even on a fully-paid basis [C-117]; shareholders were legally compelled to keep paying calls into assets the market had already discounted by half [C-223, C-230]; dividends across the sector collapsed to an average 1.9% in 1849 [C-224]; and speculators in never-authorized schemes lost before a rail was laid [C-236]. A qualifier: many losers had paid only small deposits, so per-investor losses on the shortest-lived promotions may have been limited [C-134]. **No reliable aggregate £ investor-loss figure exists [§5.C].**

**5. Why did outcomes differ?** Four mechanisms recur in the evidence: (i) **entry timing and price**, amplified by (ii) **partial-payment leverage** [C-116, C-117]; (iii) **accounting quality** that let reported dividends diverge from economic profit [C-188, C-193]; and (iv) the structural **gap between social value and investor return** — the infrastructure kept delivering transport value while much of the capital that financed it was impaired [C-272, C-273 vs C-224]. Technological importance did not translate into investor return; the two must never be equated.

---

## B. Technology and Cost-Curve Change

Only the mechanisms needed for the value question are covered here; this is not a history of the steam engine.

**Why steam became commercially useful, and slowly.** Fuel efficiency improved ~15-fold from the Newcomen engine to early-20th-century very-high-pressure engines (30 → 12.5 → 5 → 2 lb coal/hp/yr) [C-002], and the delivered cost of a benchmark steam horsepower fell from ~£33.5/yr (1760) to ~£4.0/yr (1910) [C-004]. Yet commercial usefulness was gated by **complementary capital**: reliable high-pressure engines required boiler advances, and only after the Lancashire boiler (early 1840s) were they economic in textile mills [C-014]. This is the core "diffusion was slow" finding — steam reached parity with water only in 1830 [C-001] and, on the conventional Factory-Return-based estimates, as late as 1870 ~half of all steam power was still in mining and cotton textiles [C-015].

**A live measurement dispute (kept open).** Whether steam diffusion was genuinely narrow is `contested`: Bottomley's archival Suffolk census implies the Factory Returns undercount steam by a large margin, putting 1870 UK capacity ~60% above the Kanefsky/Crafts figure (3.30m vs 2.07m ihp) [C-016, C-019], and finds a take-off from c.1837 that *preceded* widespread high-pressure adoption [C-020]. This ledger records both estimates as competing rather than adjudicating them.

**Productivity lag.** The growth-accounting contribution was modest throughout — peak ~0.38 pp/yr (1850–70) [C-007], an ~80-year lag after Watt [C-009], with the 1800–30 TFP contribution bounded only to −0.6% to +1.2%/yr [C-013]. **Bounded conclusion (medium confidence):** steam/railways were technologically decisive but their *measured* productivity impact was gradual and modest — a finding that already separates "importance" from "value creation rate."

**Gaps.** These sources contain **no railway freight/passenger unit-cost-decline series** [C1 gaps] — a real limitation for any cost-curve claim about transport prices specifically.

---

## C. Infrastructure Buildout and Capital Formation

**Acceleration and the boom-bust in authorizations.** Parliament-authorized new mileage rose from 810 (1844) to a peak of 4,540 (1846), then collapsed to 1,295 (1847), 373 (1848), and 7 (1850) [C-063]. Actual construction investment rose £13m (1845) → £44m peak (1847), roughly 8% of GDP on Odlyzko/Nash figures [C-053] — though a competing reconstruction (Mitchell 1964) gives 5.7/6.7/4.7% for 1846–48 [C-064]; the two are unreconciled (`contested`).

**Authorized ≠ built ≠ paid — kept strictly separate.** The ledger's discipline here is load-bearing:
- **Authorized:** ~£268m across Nash's 42 main lines by end-1848 [C-050]; had every sanctioned scheme been built, mileage would have grown ×5 not ×3 [C-055].
- **Built / spent:** only ~half of Mania-authorized mileage was actually built by 1853 [C-056]; of Nash's £172m *invested*, only £138m had reached revenue-service mileage and only ~£99m was earning a return [C-051].
- **Subscribed vs paid:** during 1844–45 investors were mainly *increasing liabilities*, not injecting cash — nominal (subscribed) capital rose sharply while par (paid) capital rose only gradually [C-059], a gap widened by Parliament cutting the minimum deposit from 10% to 5% (Feb 1844) before restoring it (Jul 1845) [C-060].
- **Called:** collected later via legally compulsory "calls" [C-057, C-058]; new-railway median paid-up capital rose from 6.0% (1844–45) to 92.4% (1850) as calls accumulated [C-123].

**Financing structure shaped investor exposure.** Partial payment meant investors held leveraged positions: this both amplified boom gains [C-116, C-117] and, via compulsory calls, forced continued payment into assets the market had already marked down [C-223, C-230].

**Where "overbuild" is measured vs interpreted.** *Measured:* the authorization-vs-built gap (~half unbuilt) [C-056] and the two-year offset by which construction kept rising to its 1847 peak *after* prices peaked in mid-1845 [C-069]. *Interpretation:* that this constituted economically excessive investment (as opposed to rational completion of viable lines) is Odlyzko's reading [C-055], not a directly measured fact — cost overruns are documented (planned £15,600–25,000/mile vs realized £31,700–35,200 [C-068]) but "overbuild" as a welfare judgment remains partly interpretive.

---

## D. Railway Mania: Bubble, Rational Response, or Both?

Two full-text-verified interpretations disagree at citation level [C-270, C-271].

**Odlyzko — market inefficiency / collective hallucination.** Core claim: contemporaries had "trustworthy quantitative measures" showing insufficient future demand, so the bust was predictable ex ante and investors sustained a collective hallucination [C-270]. Mechanism: available information was ignored. Evidence: contemporary demand/traffic estimates and committee reports. Strongest counter-evidence: Campbell's finding (below) that relative pricing was internally consistent. Unresolved: Odlyzko does not re-estimate Campbell's regressions.

**Campbell — myopic but rational.** Core claim: once short-term (1–2 year) dividend growth is controlled for, railway shares were priced consistently with non-railways; the "key failure" was inability to forecast *longer-term* dividend declines, implying the bust was hard to prevent ex ante [C-271]. Mechanism: rational pricing on short-horizon information. Evidence: weekly cross-sectional dividend-yield regressions. Strongest counter-evidence: Odlyzko's contemporary-information argument. Unresolved — and a **citation-fidelity flag**: the exact Campbell abstract wording Odlyzko quotes is not in the published 2012 text on file (Odlyzko quoted an earlier draft) [C-271].

**Bounded synthesis (medium confidence, no forced binary).** The evidence supports *multiple mechanisms operating simultaneously*: (i) a genuine fundamental component — established-railway dividend changes explained much of the price path [C-125, C-232], and the bubble pattern persists even among established railways [C-122]; (ii) a large **leverage/partial-payment amplifier** that made headline swings far exceed underlying fundamental moves [C-116]; and (iii) at least a *segment* of genuinely excessive promotion (≥1,000 lines projected [C-061], half never built [C-056], never-authorized schemes that still ran up and crashed [C-236]). The discriminating test that would separate Odlyzko from Campbell — whether the specific contemporary estimates had the power to forecast the realized dividend decline, and whether their authors traded on them — has not been run by either paper [C-271]. So: neither "pure bubble" nor "fully rational" is supported; a **fundamentals-plus-leverage-plus-tail-of-excess** reading is the bounded conclusion.

---

## E. Value Creation versus Value Capture

Evidence strength is graded per actor. Where evidence is insufficient, the category is left explicitly empty rather than filled with narrative.

| Actor | Evidence strength | What the ledger supports |
|---|---|---|
| 1. Inventors / technology developers | **insufficient** | The ledger documents the *technology* (efficiency, boilers, diffusion; C-002/C-014) but contains **no evidence on returns to inventors/patentees**. No claim made. |
| 2. Equipment / locomotive suppliers | **insufficient** | No supplier-level profit or return data in the ledger. The "sell the shovels" proposition is **not testable** from current evidence — explicitly unresolved. |
| 3. Coal, iron, other complements | **insufficient** | Complementary assets are shown to be *necessary* (C-014) but no complement-supplier return data exists. No claim made. |
| 4. Promoters / financiers | **weak** | Indirect only: promotion boom scale (≥1,000 lines [C-061]), Hudson's fraud on 3 of 4 controlled lines [C-220], and the incentive to inflate via capital-account manipulation [C-193]. No return figure for promoters as a class. |
| 5. Railway operating companies | **moderate** | Established pre-Mania operators earned real operating returns early (~8% dividends start-1847 [C-233]; YNM pre-Mania ~10.1–14%, two-hop [C-191, C-229]); operating economics deteriorated as the network extended (profit/mile £1,811→£1,231, 1843→1850 [C-195]); long-run ROCE eroded to ~4.3–4.6% by 1870–1912 [C-187]. |
| 6. Railway shareholders | **strong (timing-conditional)** | Returns were cohort- and timing-dependent: boom cohorts +36–57% leveraged, 1847 cohort −19.6% [C-117]; sector decade total return +3.7% (1840s) [C-109]; 66–70% peak-to-trough price fall [C-112, C-120]; dividend collapse to 1.9% (1849) [C-224]. |
| 7. Bondholders | **insufficient (UK) / partial (US)** | UK: return on total capital incl. loans 2.8% (1849), 3.6% decade [C-225] — not decomposed to bondholders specifically. US comparative: bond defaults in the 1873 panic (89 railroads) [C-315]. |
| 8. Landowners / logistics hubs | **insufficient** | **No landowner or hub value-capture evidence in the ledger.** Brief §4 Challenge A wanted this; it is a genuine gap. No claim made. |
| 9. Downstream businesses / users | **moderate (aggregate only)** | Users captured the transport-cost / social-savings benefit (Fogel 2.7% / D&H 3.22% of US GNP [C-272, C-273]; UK passenger savings large [C-274]) — but this is an economy-wide aggregate, not identified downstream firms. |

**Bounded conclusion (medium-low confidence).** On current evidence the identifiable *value capture* accrued to (a) **users/downstream via social savings** (aggregate, well-evidenced) and (b) **early established operating companies and well-timed leveraged shareholders** (firm/cohort-evidenced) — while the "sell-the-shovels" beneficiaries (suppliers, coal/iron, landowners) that the research question specifically asked about are **not evidenced at all** in this ledger. This is itself a material finding: the popular "suppliers/builders were the winners" story is **not supported here — it is untested**, which is different from being false.

---

## F. Operating Profit versus Investor Return

These are distinct measures and the ledger shows them diverging:

- **Revenue growth** was strong in aggregate (mileage tripled [C-054]) but revenue *per mile* fell (£3,280 → ~£2,200, 1844→1851 [C-054]) as the network extended into thinner traffic.
- **Operating economics / accounting profit:** reported net revenue is not a clean profit measure — no depreciation was charged [C-188], and capital-account manipulation inflated it [C-193]. YNM's flat 10% half-yearly dividend across 1845–47 [C-190] coexisted with a −0.3% return on its Mania-era extensions [C-191, two-hop] — a single stable *reported dividend* masking value destruction inside the same firm [C-192].
- **Return on paid-up capital (ROCE):** 15 major companies fell from ~5.1% (1872) to ~4.3% (1893), recovering to ~4.5% (1910) [C-187] — but this is *post-Mania* and must not be read back onto the 1840s.
- **Shareholder total return vs benchmark:** railway sector 1840s decade total return +3.7% [C-109]; broad UK equity 5.4% with a 2.6 pp premium over Consols [C-107, C-108]; survivorship-adjusted floor 4.62% [C-133].

**Why they diverge (medium confidence):** reported dividends were sustained by accounting choices [C-188, C-193] and by leverage timing [C-116] even as economic returns on new capital were weak [C-191, C-229] and market prices collapsed [C-112]. **Hard rule preserved: a reported dividend is never treated here as proof of economic profitability [C-192].**

---

## G. Who Lost Money and Why?

The failure evidence (the plan's mandatory failure quota) is concrete and not confined to survivors:

- **Failed / weak schemes:** North British Railway — no common dividend within ~2 years of 1849 [C-221]; Leeds & Thirsk — cost >£30,000/mile vs £20,000 planned, revenue ~£1,000/mile vs £3,000 expected by 1852 [C-222].
- **Boom-entry timing:** the 1847 authorization cohort lost −19.6% (leveraged) and −2.7% (unleveraged) [C-117, C-228]; YNM's Mania extensions earned 2.3% vs 14% on its earlier lines [C-229].
- **Capital calls as a loss amplifier:** shareholders were legally compelled to keep paying calls into assets already discounted ~50% [C-223, C-230].
- **Dividend collapse:** sector-wide average 1.9% (1849), below the ~3% Consol yield [C-224].
- **Never-built / never-authorized:** ~half of authorized mileage unbuilt [C-056]; many promoted lines never authorized, yet still ran up and crashed [C-236].
- **Restructuring / fraud:** Hudson's fraud on 3 of 4 controlled lines [C-220]; US comparative receiverships (119 companies in the 1893 panic alone) [C-313].

**Survivorship bias — actively controlled.** Rule Britannia's survivorship correction cuts the 1825–70 return from 9.28% to as low as 4.62% [C-133], but the authors concede it *omits* losses from companies listed <12 months (the fraudulent Mania promotions) [C-134]; Campbell's Mania data show losses were *not* confined to those short-lived promotions [C-113, C-117]. **Bounded conclusion (medium confidence):** losses were real, timing-concentrated, and amplified by compulsory leverage — but a headline aggregate loss figure is not available (§5.C), and the smallest-deposit failures may have imposed limited per-investor losses [C-134].

---

## H. Was Overbuild Economically Productive?

Proposition: *investor capital can be destroyed while the infrastructure it financed continues to generate social and downstream value.*

- **Strongly supporting:** investor capital *was* impaired (price collapse [C-112], dividend collapse [C-224]) while roughly half of authorized mileage *was* built [C-056] and continued in service; downstream users captured a real transport-cost benefit (social savings [C-272, C-273, C-274]).
- **Partially supporting:** the surviving infrastructure's downstream value is measured only at the economy-wide aggregate (social savings), and that aggregate is itself modest and contested (Fogel 2.7% vs D&H 3.22% of GNP [C-272, C-273]) — so "enormous productive legacy" overstates what is measured.
- **Unresolved measurement issues:** there is no aggregate £ investor-loss figure to place on one side of the ledger [§5.C], and no dated cohort reconstruction to establish *how much* capital was destroyed for *whom* [§5.A]. The proposition is therefore **partially supported (medium-low confidence)**: the *direction* (capital impaired, infrastructure retained, social value real) is evidenced; the *magnitudes* on both sides are not jointly quantified.

**Discipline preserved:** high social value is **not** used to infer attractive investor returns — the dividend/return evidence [C-109, C-117, C-224] is the only basis for investor-return statements.

---

## I. Profit-Pool Migration

Assessing movement of value capture across stages (technology → equipment → infrastructure buildout → network operation → downstream users) as a **historical finding only** (no AI mapping).

- **What the ledger supports:** a *temporal* shift within the operating layer — established operators' returns were high early (~8–14% [C-233, C-229]) and eroded over decades (ROCE ~5.1%→4.3% by 1870–1912 [C-187]; profit/mile £1,811→£1,231 [C-195]); and a persistent **downstream/user** capture via social savings [C-272, C-273].
- **What is insufficient:** the ledger has **no returns data for the equipment, coal/iron, or promoter/financier stages** (§E rows 1–4), so migration *across the value chain* cannot be traced. The technology→equipment→infrastructure hand-offs are untestable from current evidence.

**Bounded conclusion (low confidence):** the evidence supports *within-operator temporal decay* of returns and *durable downstream user capture*, but **does not support (or refute) cross-stage profit-pool migration** — that specific proposition is `undecidable` here for lack of supplier/downstream firm-level return data.

---

## J. Hypothesis Verdicts

| Hyp | Verdict | Confidence | Supporting Claim IDs | Strongest counter-evidence | Boundary conditions |
|---|---|---|---|---|---|
| **H1 — Bottleneck Capture** | partially supported (infrastructure layer only); supplier side **undecidable** | low | Early established operators captured returns [C-233, C-191, C-229] | Returns eroded over time [C-187]; **no supplier/coal/iron/locomotive return data at all** (§E) | Holds, weakly, for early infrastructure *operators*; untested for the "scarce complements" the hypothesis names |
| **H2 — Social Value Exceeds Investor Value** | partially supported | medium | Social value real [C-272, C-273, C-274] alongside weak/negative railway investor outcomes [C-109, C-117, C-224] | Broad UK equity returns were positive [C-107, C-133]; no aggregate investor-loss figure [§5.C] | "Exceeds" is directional, not a measured inequality; strongest for late/new-cohort railway shareholders, not all investors |
| **H3 — Overbuild Can Be Economically Productive** | partially supported | medium-low | Capital impaired [C-224] while ~half of mileage built & retained [C-056] and social value delivered [C-272, C-273] | Social-value magnitude modest/contested [C-272 vs C-273]; "overbuild" partly interpretive [C-055 vs C-056] | Direction evidenced; magnitudes on both sides not jointly quantified |
| **H4 — Profit Pools Migrate** | undecidable | low | Temporal return decay within operators [C-187, C-195]; durable downstream capture [C-272] | No equipment/supplier/downstream firm-level return data (§E, §I) | Cross-stage migration untestable; only within-operator temporal decay is evidenced |
| **H5 — Timing Dominates Category Selection** | supported | medium-high | Cohort dispersion by authorization year [C-115, C-117]; leverage artifact [C-116]; boom-top compulsion [C-223]; price/investment offset [C-069] | Fundamental component also present [C-125, C-232]; LSE-only sample [C-119, C-124] | Bounded to the partial-payment/leverage mechanism and London-listed railways; strongest-evidenced hypothesis |

**H5 is the best-supported; H4 and the supplier side of H1 are the least — a direct consequence of the ledger being rich on prices/returns/failure and thin on supplier/downstream/landowner returns.**

---

## K. What We Still Do Not Know

| Open item | Materiality | Basis |
|---|---|---|
| 1. Aggregate UK investor-capital-loss figure | **material only to precision** (not to the qualitative "many investors lost, timing-dependent" conclusion) | Absent from Odlyzko's full text; no called-vs-paid national series to derive it [C-224, C2 gaps] |
| 2. YNM cash-flow-aware return reconstruction | **material only to precision** (the timing/leverage conclusion stands on the cohort data [C-117]) | `undecidable` — no dated call schedule in any located source [C-166] |
| 3. Provincial-market underrepresentation magnitude (1843–50) | **material to precision, potentially to §E/§G scope** | Direction documented (railways foundational to provincial exchanges; 1870 shows 61–85% railway concentration) but 1843–50 magnitude unquantified [C-137, C-141] |
| 4. Conclusions dependent on unread Arnold & McCartney material | **material to the YNM operating-vs-return sub-claim only** | The YNM 10.1%/−0.3% and 14%/2.3% figures are two-hop citations to McCartney & Arnold (2001), unread [C-191, C-194, C-229] — do not over-weight |
| 5. Railway-investment/GDP-share discrepancy (Odlyzko ~8% vs Mitchell 5.7–6.7%) | **non-critical** | `undecidable` from available files (different denominators/definitions) [C-053, C-064] |

None of these overturns the main Executive Answer; items 1–2 affect precision, item 3 could affect the breadth of the failure/return picture, item 4 is contained to one sub-claim.

---

## L. Candidate Reusable Mechanisms

Candidates only — **no `PAT-*` file is created**, and all remain provisional pending cross-cycle validation (which requires a second revolution, not yet studied).

| Candidate mechanism | Historical evidence strength | Boundary conditions | Evidence against | Eligible for later Pattern drafting? |
|---|---|---|---|---|
| **M1 — Social-value / investor-return divergence** | moderate–strong | Holds for late/new-cohort railway shareholders vs users; "divergence" is directional | Broad equity returns positive [C-107]; no aggregate loss figure [§5.C] | Yes (candidate) — best-evidenced divergence |
| **M2 — Timing & entry-price dependence (with leverage)** | strong (within this case) | Bounded to partial-payment leverage and LSE-listed railways | Fundamental component also present [C-125] | Yes (candidate) — strongest single mechanism |
| **M3 — Capital-cycle overbuild** | moderate | Direction measured (half unbuilt [C-056]; investment lagged prices [C-069]); welfare judgment interpretive | "Overbuild" partly interpretation not fact [C-055] | Yes (candidate), with the interpretive caveat explicit |
| **M4 — Accounting quality decouples reported profit from economic return** | moderate | No depreciation + capital-account manipulation [C-188, C-193] | Odlyzko argues abuse was overstated [C-193 counter] | Yes (candidate) |
| **M5 — Bottleneck / infrastructure-owner early capture** | weak | Early operators only; erodes over time | No supplier-side evidence (§E); erosion [C-187] | Provisional — weak; not yet eligible |
| **M6 — Profit-pool migration across the value chain** | insufficient | — | Untestable on current evidence (§I) | No — undecidable, ineligible until supplier/downstream data exist |

---

## 5. Gate 2 Conditions Preserved (visible limitations)

**A. YNM cash-flow reconstruction — `undecidable` with current evidence.** No dated call schedule was found in any of three Tuck editions read. **No complete money-weighted return is estimated or interpolated** [C-166, C-162].

**B. Provincial-market coverage — partially resolved.** The *direction* of underrepresentation is documented; the *magnitude* for 1843–1850 is not quantified [C-141]. All 1843–50 railway price/return figures here are London-Stock-Exchange samples [C-119, C-124].

**C. Aggregate UK investor-capital loss — no reliable aggregate figure established.** No headline number is invented; the loss evidence is cohort/company/price-index based [C-117, C-222, C-224, C-112].

**D. Two-hop citations — labelled.** The YNM 10.1%/−0.3% and 14%/2.3% return figures originate in the unread, paywalled McCartney & Arnold (2001) and carry only the confidence their provenance permits [C-191, C-194, C-229].

---

*Historical synthesis complete. Derived from the Evidence Ledger; no material claim added beyond it. No AI-era analogy, `MAP-001`, `PAT-*`, or `THS-001` created. Next: Gate 3 Historical Stability Review.*
