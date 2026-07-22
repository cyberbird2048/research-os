---
id: HIS-002-EVIDENCE-LEDGER
type: evidence-ledger
title: HIS-002 Evidence Ledger — Electricity, Grid Infrastructure, and Industrial Electrification
status: draft
created: 2026-07-20
updated: 2026-07-21
owner: cyberbird
research_lead: claude-code
research_architect: chatgpt
review_date: 2026-08-04
confidence: low
sources:
  - HIS-002-SOURCE-REGISTER
related:
  - HIS-002
  - HIS-002-BRIEF
  - HIS-002-PLAN
  - HIS-002-SOURCE-REGISTER
  - HIS-002-GATE-2
  - PAT-001
  - PAT-002
  - PAT-003
---

# HIS-002 Evidence Ledger

**Authorization.** Built under the Research Architect's Source Verification Review verdict (Stage B PASSED; **Stage C AUTHORIZED**), executing `HIS-002_RESEARCH_EXECUTION_PLAN.md` §4 (parallel four-outcome searches). This is a cross-cycle **validation** ledger for `PAT-001`/`PAT-002`/`PAT-003`; it records evidence, **not verdicts**. It does not assign a Pattern verdict, update the Pattern Validation Matrix, write synthesis, promote any Pattern, or contain any AI-era content. **Stop point:** on completion, submit for Evidence Sufficiency Review.

**Claim-ID scheme.** `E-###` (distinct from HIS-001's `C-###`). PAT-001 = E-1xx; PAT-002 = E-2xx; PAT-003 index-tier module = E-3xx; PAT-003 security-level module = E-35x/E-37x.

**Four lanes (anti-confirmation, per brief §8.4).** Every claim is tagged to exactly one of: **Supports / Weakens / Rejects / Undecidable-pending-access**. Weaken/Reject evidence was searched with the same seriousness as support (see the §Anti-Confirmation Balance Check). Each claim carries: Pattern · lane · source · exact location · class · statement · method/unit · confidence · counter-evidence · limitations.

**Source restrictions in force (RA, Source Verification Review).**
- **S-005 (FTC Utility Corporations), S-011 (Taylor 1962 Insull), S-012 (Moody's PU manuals):** full text not yet obtained → **no substantive evidence claim** rests on them here; they appear only as `Undecidable-pending-access` pointers.
- **S-016 (David & Wright):** not load-bearing (verified-partial only) → orientation only.
- **S-019 (Gaggl et al.):** supporting adjacency only (measures employment reallocation, not value or return).
- **S-014 (Schrade & Walls):** non-load-bearing; a financing-efficiency counter-explanation candidate only; **never** written as realized-return evidence.
- **S-008 (Cowles):** every return claim retains its boundaries — "Electric, Gas, Etc." **mixes electric+gas**, the indexes are **value-weighted, changing-composition, chained** (survivorship embedded), and the **total-return file is based to inception=100 per series, NOT 1926=100** (price file ≈1926=100); only **within-series ratios** are valid. These caveats apply to every E-3xx and every S-008-sourced E-1xx claim below.

**Pattern-specific boundaries in force (RA).**
- **PAT-001** compares two *different outcome constructs* — productivity/social/downstream value vs. securities investor return. Temporal overlap ≠ matched-cohort causal correspondence. Any supportive reading is stated only as **"coexisting divergence,"** never as proof that the same assets' social value transferred (or failed to transfer) to the same investors.
- **PAT-002** primary quantitative window ≈**1920–1935**; pre-1920 is low-frequency/sensitivity only; the **1912** census scope (includes street/electrical railways) must not be spliced with other years. **Equity-price decline, holding-company collapse, and securities impairment may NOT, alone, establish physical overbuild** — a physical-overbuild reading must rest on capacity/output/utilization or later-vintage operating evidence.
- **PAT-003** has two independent modules: an **index-tier module** (S-008) and a **security-level module** (bounded S-010 sample; the rest `Undecidable-pending-access`). **Index-tier dispersion alone does not make PAT-003 `Supports`.**

---

## Quantitative Backbone

### QB-1 — Cowles tier total return (S-008; Series C, inception=100 per series; within-series ratios only)

| Date | C-1 ALL | C-4 UTIL | C-11 ELEC/GAS OPERATING | C-16 ELEC/GAS HOLDING |
|---|---|---|---|---|
| Dec-1900 | 647.5 | 910.2 | 412.6 | 44.8 |
| Dec-1913 | 1378 | 1148 | 547.3 | 74.7 |
| Dec-1921 | 2091 | 1728 | 690.6 | 104.0 |
| Dec-1925 | 4479 | 3733 | 1706 | 609.4 |
| Sep-1929 (peak) | 11841 | 13997 | 6996 | 2810 |
| Dec-1929 | 8182 | 8821 | 4487 | 1587 |
| Jun-1932 (trough) | 2099 | 2741 | 1778 | 287.9 |
| Dec-1935 | 6762 | 5682 | 2672 | 531.7 |
| Dec-1938 (last) | 7497 | 5692 | 2920 | 400.5 |

Location: `Stock_PricesincDvds-Cowles.xls`/Sheet1, blocks C-1=R5, C-4=R257, C-11=R845, C-16=R1265; Year in col0, Jan=col1…Dec=col12. Operating series populated from Oct-1886, holding from Aug-1890; 428/432 months populated 1900–1935 (only market-wide Aug–Nov-1914 gap).

### QB-2 — US electric-utility physical series (S-001, Historical Statistics Chapter G; output thousand kWh, capacity kW, G-204 kWh/kW)

| Year | Capacity G-218 | private G-219 | public G-220 (muni G-221) | Output G-184 | private G-185 | public G-186 | G-204 | cap factor |
|---|---|---|---|---|---|---|---|---|
| 1902 | 1,212,235 | 1,098,855 | 113,380 (113,380) | 2,507,051 | 2,311,147 | 195,904 | 2,068 | 23.6% |
| 1912\* | 5,165,439 | 4,768,762 | 396,677 | 11,569,110 | 11,031,583 | 537,527 | 2,240 | 25.6% |
| 1920 | 12,713,608 | 12,022,329 | 691,279 (601,232) | 39,404,639 | 37,715,985 | 1,688,654 | 3,099 | 35.4% |
| 1925 | 21,472,077 | 20,044,597 | 1,427,480 | 61,451,091 | 58,684,988 | 2,766,103 | 2,862 | 32.7% |
| 1929 | 29,839,459 | 27,952,571 | 1,886,888 | 92,180,273 | 87,513,677 | 4,666,596 | 3,089 | 35.3% |
| 1932 | 34,386,739 | 32,033,125 | 2,353,614 | 79,392,929 | 74,488,136 | 4,904,793 | 2,309 | 26.4% |
| 1935 | 34,435,768 | 31,820,357 | 2,615,411 | 95,287,390 | 89,329,706 | 5,957,684 | 2,767 | 31.6% |
| 1937 | 35,620,011 | 31,958,043 | 3,661,968 | 118,912,675 | 110,463,615 | 8,449,060 | 3,338 | 38.1% |

\*1912 = census scope broadened (street/electrical railways) — **not spliceable**. Internal checks verified: G-185+G-186=G-184; G-219+G-220=G-218; G-204=G-184/G-209; 1902 census HP×0.746=S-001 kW. Federal/Other ownership split only from 1920.

### QB-3 — CFC security-level micro-sample (S-010; integers reliable, eighths OCR-uncertain; 5 issuers, 2 issues)

| Issuer (tier) | ~Year-end 1928 (CFC 1929-01-05) | ~Year-end 1931 (CFC 1932-01-02) |
|---|---|---|
| Commonwealth Edison (operating, Insull) | ~207–219 (CY1928 range 157–227) | 115–118 |
| American & Foreign Power common (holding, EBASCO) | ~80 | ~7 |
| Electric Bond & Share common (holding, EBASCO) | (CY1928 high ~180⅞) | ~11 |
| Middle West Utilities common (holding, Insull) | ~170–184 | dividend paid **in common stock**; its 5% bonds at 38–55 |

---

## PAT-001 — Social Value / Investor Return Divergence (two-ledger core)

*Supports = "coexisting divergence" only. S-008 caveats (QB-1) apply to E-114/E-115/E-116.*

**E-101 | PAT-001 | Supports (coexisting) | S-018 | Intro p.2 (PDF p.3) + Abstract | quantitative estimate.** By 1920, hydropower proximity is associated with ~10% faster labor-productivity growth for a 75th- vs 25th-percentile energy-intensity industry, with gains appearing from 1900 — a large early manufacturing-productivity (social/downstream value) signal coexisting in 1900–1920 with the separately-measured Cowles utility-investor-return series. *Method:* cross-industry×cross-county DiD, IV = energy intensity × ≤70km hydro proximity; labor productivity (VA/worker). *Conf:* high. *Counter:* authors concede it may be largely cheaper-hydro energy access (E-106). *Limits:* different constructs; localized to hydro-proximate counties; working paper.

**E-102 | PAT-001 | Supports (coexisting) | S-018 | §4.1 p.16 (PDF p.18), Fig 3 + Table 3 | quantitative estimate.** Productivity differential ~4% by 1900 rising to ~11% by 1920 and holding to 1940; +1% electric-HP/value-added → +1.5% labor productivity (1920). *Conf:* high. *Counter:* no-1890-control panel slightly larger (mean-reversion). *Limits:* local differential, not an aggregate level.

**E-103 | PAT-001 | Supports (coexisting) | S-018 | §4.2 p.19 (PDF p.21), Table 5 | quantitative estimate + interpretation.** Electrified energy-intensive cells raised capital-per-worker and saw a negative labor-share effect (significant 1920) — the productivity value was partly captured by capital, not fully shared with labor. *Conf:* high (direction), medium (magnitude). *Counter:* runs against the era's rising-labor-share macro trend (isolable to treated cells). *Limits:* qualifies a "social value = broad welfare" reading.

**E-104 | PAT-001 | Supports (coexisting, adjacency) | S-018 | §4.1 p.16–17 (PDF p.18–20), App Fig A.3 | quantitative estimate.** Gains came from faster output than employment growth; employment coefficients smaller/less significant; "new jobs were on net lower paying." *Conf:* high (direction). *Limits:* mixed employment sign qualifies the welfare reading.

**E-105 | PAT-001 | Weakens | S-018 | §4.3 p.21–22 (PDF p.23–24), Table 6/7 | quantitative estimate + interpretation.** In concentrated (large-firm-1890) markets, electrification raised measured productivity but muted output — consistent with higher **markups** rather than pass-through to consumers; "market structure mediated how gains were shared." So a high productivity coefficient is **not** a clean proxy for diffuse social value. *Conf:* high. *Limits:* markups inferred, not measured.

**E-106 | PAT-001 | Weakens | S-018 | Intro p.2–3 (PDF p.3–4) | scholarly interpretation.** The authors' own hedge: the effect "may have been largely the direct result of access to a cheaper source of energy through hydropower" — electrification-as-organizational-GPT is not cleanly separable from cheap-hydro/geography. *Conf:* high. *Limits:* undercuts treating S-018 as electrification-alone social value.

**E-107 | PAT-001 | Weakens | S-018 | §4.1 p.17 (PDF p.19–20), App Table A.10 | quantitative estimate.** Using cross-industry variation alone (dropping the hydro interaction), productivity effects are insignificant and visible only ~1930 (20–30 years later) — the "rapid" social-value headline is **localized** to hydro-proximate counties; the national signal was slow. *Conf:* high. *Limits:* any coexisting-divergence reading must be geographically bounded, not read as broad national 1900–1920 realization.

**E-108 | PAT-001 | Supports (coexisting, edge/straddle) | S-020 | AER 93(4) p.1403, Table 2 | quantitative estimate.** 1929–1941 peak-to-peak MFP growth ≈2.27–2.36%/yr (highest peacetime peak-to-peak of the century), coexisting with the collapse in utility investor returns. *Conf:* high (table values). *Counter/Limits:* window **straddles 1935** (only 1929–1935 in scope; no 1929–1935-only figure); broad-economy MFP, not electrification-specific or utility-sector; attribution shared across technologies → load-bearing partial.

**E-109 | PAT-001 | Adjacency — no outcome weight (excluded from the Supports lane) | S-019 | Abstract (NBER w26477; pub. Labour Economics 2020) | quantitative estimate.** 1910–1940 transmission-line expansion raised the operative employment share +3.3pp and cut farmers −2.1pp (explains 50.5% of the operative rise). *Conf:* high (abstract). *Limits:* measures **structural transformation (employment reallocation)**, a third construct — not productivity value and not investor return; 1910–1940, no clean 1910–1935 cut. **Reclassified per the Evidence Sufficiency Review (condition 1): this claim carries no outcome-lane weight for PAT-001 and is excluded from the Supports tally; it is context/adjacency only.**

**E-110 | PAT-001 | Framing only (no lane weight) | S-017 | AER 80(2):355–361 (1990) | scholarly interpretation.** The dynamo/computer diffusion-lag thesis (~1880s–1920s referent); **no dated numeric estimate**. Supplies the narrative S-018 contests. *Conf:* framing only — cannot carry a value lane.

**E-111 | PAT-001 | Orientation — NON-load-bearing | S-016 | RePEc landing only (full text not fetched) | scholarly interpretation.** Orientation reading in which the 1920s manufacturing-TFP surge is a **confluence** of electrification + a labor-market regime change (end of mass immigration) — co-cause, not an isolated electrification estimate. *Conf:* medium; **explicitly non-load-bearing**. *Limits:* shared attribution is a genuine limit on any "electrification = social value" claim.

**E-112 | PAT-001 | Weakens candidate — Undecidable-pending-access | S-014 | Abstract only (JSTOR 24812845 / RG 403; two-hop) | scholarly interpretation.** A cost-of-capital / market-liquidity (financing-efficiency) rationale for **why** the holding-company form emerged (GE used it to form Electric Bond & Share). *Method:* NONE extractable — no realized-return series verified. *Conf:* low. **HARD RULE: must not be entered as realized-return evidence**; it only weakens a naïve "holding companies were purely value-destructive" reading, and cannot Reject PAT-001. *Limits:* full text unreached.

**E-113 | PAT-001 | Weakens / methodological (cross-cutting) | S-018 + S-020 vs S-008 | construct comparison | scholarly interpretation.** PAT-001 juxtaposes two different outcome constructs on different units — manufacturing/economy productivity (E-101–E-108) vs. utility **securities** investor return (E-114–E-116). Their 1900–1935 overlap is **coexisting divergence, not matched-cohort causal correspondence**: no source here shows the same assets' social value did or did not accrue to the same investors. *Conf:* high. *Limits:* the load-bearing honesty constraint on the entire PAT-001 Supports column.

**E-114 | PAT-001 | Supports (coexisting — investor-return side) | S-008 | QB-1, C-11/C-16 Dec-1921 & Dec-1929 | quantitative estimate.** Utility-securities investors saw large 1920s gains then a deep collapse: electric/gas holding total return compounded +1426% (104.0→1587) and operating +550% (690.6→4487) Dec-1921→Dec-1929, vs all-stocks +291%. Set beside the coexisting productivity gains (E-101–E-108), this is the investor-return ledger of the divergence. *Conf:* high. *Counter:* the same high beta that lifted holding later amplified its losses (E-115). *Limits:* S-008 caveats (QB-1); coexisting, not transfer.

**E-115 | PAT-001 | Supports (coexisting — investor-return side) | S-008 | QB-1, Sep-1929 peak & Dec-1935 | quantitative estimate.** Six-year total return from the Sep-1929 peak to Dec-1935 was −61.8% (operating), −81.1% (holding), −42.9% (all-stocks) — the utility investor's post-peak experience was worse than the market at both tiers, worst for holding, coexisting with high measured electrification productivity. *Conf:* high. *Counter:* peak-anchored windows overstate loss vs Dec-anchored. *Limits:* S-008 caveats; coexisting, not transfer.

**E-116 | PAT-001 | Weakens / context | S-008 | QB-1, C-16 Dec-1900 & Dec-1913 | quantitative estimate.** The holding-tier index was flat-to-down over its first two decades (Aug-1890=100 → 44.8 in 1900 → 74.7 in 1913) — holding-company shares were poor long-run compounders before the 1920s, cautioning against reading the 1921–29 surge as typical. *Conf:* medium. *Limits:* thin early sample; inception=100 base non-comparable across series.

**E-117 | PAT-001 | Rejects — search disposition (added per Evidence Sufficiency Review, condition 2) | S-008 + S-018 (scope statement) | cross-cutting | research inference.** Formal record that the Rejects search was executed, not skipped: to **Reject** PAT-001 for this cycle, the evidence would have to show — within a single sufficiently-overlapping window — that **neither** the operating tier **nor** the holding tier exhibits material divergence between measured social/productivity value and direct-investor return. The open HIS-002 evidence does **not** meet that standard (the investor-return series E-114/E-115 shows a deep collapse coexisting with high measured productivity E-101–E-108; the two are on different constructs per E-113). **Disposition: "Rejects not established."** This must not auto-convert to Supports — it means the Rejects test could not be passed on current evidence, not that the Pattern is affirmed. *Conf:* high (as a disposition). *Limits:* references the construct limit (E-113) and the return evidence (E-114, E-115); a genuine Reject would require matched-cohort data that does not exist (E-118).

**E-118 | PAT-001 | Undecidable (with current evidence; added per Evidence Sufficiency Review, condition 3) | S-018/S-020 (value) vs S-008 (return) | construct gap | research inference.** The **matched-cohort value-transfer question** — whether the social/downstream value created by specific electrified assets did or did not accrue to the specific investors who financed those same assets — is **Undecidable with current evidence**: no source links a cohort of assets' measured social value to the same cohort's investor return. This is distinct from, and must be kept separate from, the narrower **coexisting-divergence question** (did high measured value and weak/uneven investor return occur in the same window?), which the open evidence *can* address and which may proceed to synthesis. *Conf:* high (as a scope statement). *Limits:* this is a genuine data-nonexistence Undecidable (not merely pending-access); it caps any PAT-001 claim from being read as a proven value transfer.

---

## PAT-002 — Capital-Cycle Overbuild (financing-side vs physical-overbuild claims kept separate)

*No equity-price/impairment evidence is imported; all claims rest on capacity/output/utilization. Window ≈1920–1935; 1902/1912 sensitivity-only; 1912 not spliced.*

**E-201 | PAT-002 | Supports | S-001 | G-218, 1920→1937 | physical/capacity.** Installed capacity rose 12,713,608 kW (1920) → 29,839,459 (1929) → 34,386,739 (1932), plateauing at 35,620,011 (1937) — a 2.35× expansion 1920→1929. *Conf:* high. *Counter:* growth tracked demand (E-210). *Limits:* includes small standby plants; source switch USGS→FPC 1936.

**E-202 | PAT-002 | Supports | S-001 | G-219 vs G-218, 1920/1929/1932 | ownership/capacity.** Investor-owned capacity dominated: 94.6% (1920), 93.7% (1929), 93.2% (1932); public/municipal never exceeded ~7% in-window. *Conf:* high. *Counter:* public rises to ~10.3% by 1937 (Federal). *Limits:* Federal/Other split only from 1920.

**E-203 | PAT-002 | Supports | S-001 | G-184, 1929 & 1932 | physical/output.** Utility output peaked 92,180,273 thousand kWh (1929), troughed 79,392,929 (1932), recovered to 95,287,390 (1935). *Conf:* high. *Counter:* 1930/1931 (91.1M/87.4M) show a gradual, not cliff, decline. *Limits:* totals include electric railroads.

**E-204 | PAT-002 | Weakens (overbuild-only reading) | S-001 | G-209/G-218, 1929→1932 | physical/capacity.** Capacity **kept rising** +15.2% into the demand collapse (29,839,459→34,386,739 kW; peak 34.59M in 1933), with no retirement. *Conf:* high. *Counter:* rising capacity into falling demand is itself an overbuild signature — but it reflects pre-1929 pipeline commitments, not a fresh oversupply decision. *Limits:* year-end capacity.

**E-205 | PAT-002 | Weakens (overbuild-only reading) | S-001 | G-218 & G-184, 1932→1937 | physical/utilization.** After 1932 capacity was near-frozen (+3.6% over five years) while output grew +49.8% — recovery was demand-led, not achieved by scrapping "excess" plant. *Conf:* high. *Counter:* consistent with real slack existing in 1932.

**E-206 | PAT-002 | Supports | S-001 | G-204, 1902–1937 | physical/utilization (native).** Utilization (production per kW): 2,068/2,240\*/3,099/2,862/3,089/2,309/2,767/3,338 kWh/kW — capacity factors 23.6/25.6/35.4/32.7/35.3/26.4/31.6/38.1%. *Conf:* high. *Counter:* 1937 (38.1%) exceeds any 1920s year — no permanent utilization impairment. *Limits:* G-204 uses end-of-year capacity (understates fast-growth years).

**E-207 | PAT-002 | Supports | S-001 | G-204 / G-184 / G-209, 1929→1932 | physical/utilization.** The core signal: utilization fell −25.3% (3,089→2,309 kWh/kW; capacity factor 35.3%→26.4%). *Conf:* high. *Counter:* a ratio decline, not proof of overbuild (decomposed at E-208). *Limits:* end-of-year capacity.

**E-208 | PAT-002 | Weakens (physical-overbuild thesis) | S-001 | G-184 & G-209, 1929→1932 | decomposition.** Of the −780 kWh/kW utilization drop, ≈−428 (55%) comes from output falling on fixed capacity (a Depression **demand** shock) and ≈−352 (45%) from continued capacity additions: output fell −13.9% while capacity rose +15.2%. The utilization collapse is majority demand shock, not pure overbuild. *Conf:* high (arithmetic), medium (interpretation). *Counter:* the 45% from capacity growth is real physical slack accumulation. *Limits:* order-dependent first-order decomposition.

**E-209 | PAT-002 | Weakens (overbuild) | S-001 | G-204 & G-218, 1932→1935 | physical/utilization.** Utilization recovered +19.8% (2,309→2,767) while capacity was essentially unchanged (+0.14%) — the trough was reversed by returning demand on a fixed physical base, a demand-shock signature, not permanent physical oversupply. *Conf:* high. *Counter:* 1935 (31.6%) still below 1929 (35.3%), so some slack persisted.

**E-210 | PAT-002 | Rejects (physical-overbuild in the 1920s) | S-001 | G-218 & G-184, 1920→1929 | growth-rate.** Through the 1920s capacity and output grew at essentially the same rate — capacity CAGR ≈+9.9%/yr vs output CAGR ≈+9.9%/yr — with flat utilization (G-204 3,099→3,089). No pre-Depression utilization erosion from overbuilding. *Conf:* high. *Counter:* flat utilization also means no efficiency banked before the crash; see E-211. *Limits:* endpoints sensitive (1920 was a strong utilization year).

**E-211 | PAT-002 | Weakens (mixed; reclassified per Evidence Sufficiency Review, condition 4 — data obtained, pending-access removed) | S-001 | G-218 & G-184, 1923→1925→1929 | growth-rate (intra-decade).** Capacity ran ahead of output mid-decade (1923→1925 capacity +37.3% vs output +20.0%, G-204 3,275→2,862) then demand caught up (1925→1929 output +50.0% vs capacity +39.0%) — a capacity **wave** / transient slack, not sustained overbuild. The data are in hand; the finding is mixed and reads as Weakens (transient mid-decade slack that demand absorbed), not an access gap. *Conf:* high (data), medium (pattern). *Counter:* the mid-decade dip could equally read as recurring transient overbuild.

**E-212 | PAT-002 | Weakens | S-001 | G-185/G-186, 1929→1932 | ownership/output.** The utilization stress was concentrated in the investor-owned sector: private output fell −14.9% (1929→1932) but public output rose +5.1% and public capacity grew +24.7%. *Conf:* high. *Counter:* public sector is <7%, so the aggregate is private-driven. *Limits:* public class heterogeneous.

**E-213 | PAT-002 | Supports (corroborates ownership series) | S-002 | 1902 Census, dynamo capacity | corroboration/capacity.** 1902 total dynamo capacity 1,624,980 HP = private 90.6% / municipal 9.4%; ×0.746 = S-001 G-218/G-219/G-221 (1902) to the unit. *Conf:* high. *Limits:* pre-window sensitivity only; early HP↔kW conversion is the ±20–25% drift S-001 warns of.

**E-214 | PAT-002 | Supports (corroborates ownership series) | S-002 | 1902 Census, output | corroboration/output.** 1902 output 2,507,051,115 kWh = private 92.2% / municipal 7.8%, matching S-001 G-184/G-185/G-187 (1902) exactly — independent primary confirmation of the early ownership split. *Conf:* high. *Limits:* pre-window sensitivity only.

**E-215 | PAT-002 | Supports (operating-group output) | S-006 | FTC 1933 AR p.24, 1930 | operating-group/output.** Nine investor-owned holding-company groups generated 17,208,201,086 kWh in 1930 (≈18% of US generation; ≈18.9% of the S-001 1930 utility total), of which ≈24% moved interstate. *Conf:* high. *Counter:* groups selected for hearings, not a random sample; describes holding structure, not physical plant. *Limits:* **no kW capacity and no utilization ratio** here — output/interstate flow only; municipal out of scope.

**E-216 | PAT-002 | Supports (operating-group output) | S-006 | FTC 1933 AR p.24, 1930 | operating-group/output.** A broader eleven-group tally: >19% of US output, ≈25% interstate. *Conf:* medium-high (narrative percentages, not a reprinted table). *Limits:* granular per-group schedules point to S.Doc 92 (S-005, pending); interstate flow ≠ capacity/utilization.

**E-217 | PAT-002 | Weakens (splice caution) | S-001 / S-002 | 1912 census scope; G-183–190 footnote | scope/comparability.** The 1912 figures sit at a scope break (1912 census added street/electrical railways); do not splice 1912 across the 1907↔1917 gap. S-001 confirms utility totals "include electric railroads and railways," and warns pre-1920 totals varied "as much as 20 to 25 percent" from definitional variance. *Conf:* high. *Limits:* 1912 sensitivity-only, not for growth-rate use.

**E-218 | PAT-002 | Rejects-guardrail (method note) | S-001 | G-204 fn 2; G-209 note | method/limitation.** Bounding caveats on the utilization series: (a) G-204 uses **end-of-year** capacity, mechanically depressing the ratio in fast-growth years (understates true 1920s utilization); (b) G-209 capacity includes small standby plants and publicly-owned non-central stations (inflates installed kW). Both push measured utilization **down** independent of any overbuild. *Conf:* high. *Counter:* biases are roughly constant across years, so trend comparisons remain valid. *Limits:* the standby share is not quantifiable from S-001 alone.

---

## PAT-003 — Entry Timing and Financing Structure

### Module A — Index-tier (S-008; QB-1 caveats apply to every claim)

> **Reclassification per Evidence Sufficiency Review (condition 5).** The index-tier dispersion claims below retain their numerical facts but are relabelled **Descriptive — no independent Supports weight**: E-307 shows the raw dispersion is fully absorbed by static market beta, and the ledger's own boundary forbids treating index-tier dispersion *alone* as `Supports` for the Pattern. Only a claim that leaves a mechanism-relevant residual **after** a broad-market control, or that combines with security-level financing data, may carry PAT-003 `Supports` weight — and no such claim currently exists (the security-level module is Undecidable-pending-access). These descriptive claims are Weakens-compatible in the balance tally.

**E-301 | PAT-003 | Descriptive (tier-dispersion; no independent Supports weight) | S-008 | QB-1, C-16 vs C-11, Sep-1929→Jun-1932 | quantitative estimate.** The electric/gas **holding** total-return index fell −89.8% peak-to-trough (2810→287.9) vs **operating** −74.6% (6996→1778) — a 15.2pp deeper drawdown; holding retained ~40% as much residual value. *Conf:* high (as a numerical fact). *Counter:* the gap is fully explained by beta (E-307), so it carries no standalone Supports weight. *Limits:* S-008 caveats; index-level.

**E-302 | PAT-003 | Descriptive (tier-dispersion; no independent Supports weight) | S-008 | QB-1, C-1 vs tiers, Sep-1929→Jun-1932 | quantitative estimate.** The tiers straddle the market: holding −89.8% was worse than the all-stocks control (−82.3%), while operating −74.6% was **shallower** than the market. *Conf:* high (numerical fact). *Counter:* operating being defensive undercuts a simple "utilities crashed harder" story; beta-absorbed (E-307). *Limits:* S-008 caveats.

**E-303 | PAT-003 | Descriptive (tier-dispersion; no independent Supports weight) | S-008 | QB-1, C-11 & C-16, Dec-1929→Dec-1935 | quantitative estimate.** Six-year cumulative total return −40.5% (operating) vs −66.5% (holding); holding investors held ~one-third of 1929 value, operating ~60%. *Conf:* high (numerical fact). *Counter:* beta-absorbed (E-307). *Limits:* S-008 caveats.

**E-304 | PAT-003 | Descriptive (existence/coverage; no independent Supports weight) | S-008 | QB-1; col13 first Oct-1886, col18 first Aug-1890 | historical fact.** A genuine, separately-indexed electric/gas **operating vs holding** split exists, densely populated monthly (428/432 months 1900–1935). *Conf:* high. *Limits:* establishes data coverage only, not a mechanism; "Etc." + electric/gas mixing → neither tier is pure-electric.

**E-305 | PAT-003 | Descriptive (tier-dispersion; no independent Supports weight) | S-008 | price file cols 13 & 18, Sep-1929 & Jun-1932 | quantitative estimate.** Price-only (ex-dividend) confirms the pattern — operating −77.7% vs holding −90.7% peak-to-trough — so dividends are not what creates the tier gap. *Conf:* high (numerical fact). *Counter:* still beta-absorbed (E-307). *Limits:* price file base ≈1926=100.

**E-306 | PAT-003 | Weakens | S-008 | derived, C-16 vs C-1 monthly returns 1929–1932 (n=47) | quantitative estimate.** In the crash the holding index co-moves with the whole market at correlation 0.974 and beta 1.46 — holding largely **is** the market ×1.46, not an independently-timed collapse. *Conf:* medium (analyst computation). *Counter:* operating tier is β≈0.95 (E-308). *Limits:* index-level; beta cannot be decomposed into leverage vs other sources.

**E-307 | PAT-003 | Weakens (load-bearing) | S-008 | derived, C-16/C-1, Sep-1929→Jun-1932 | quantitative estimate.** The holding tier's −89.8% drawdown is **fully explained by static market beta**: its β (1.38 full-window / 1.46 crash) applied to the market's drawdown predicts −90.8% to −92.0% — equal to or slightly worse than actual, leaving **no positive residual** for a distinct financing-structure crash *at the index level*. *Conf:* medium. *Counter:* leverage is itself one *source* of high beta, so "beta explains it" does not exclude the mechanism — it shows only that Cowles cannot isolate it. *Limits:* observational equivalence; index-level only. **This is why index-tier dispersion alone cannot make PAT-003 `Supports`.**

**E-308 | PAT-003 | Descriptive (tier beta-gap; Supports weight only if combined with security-level financing data — currently Undecidable-pending-access) | S-008 | derived, C-11 vs C-16, full window (n=570) | quantitative estimate.** Two same-sector tiers have sharply different risk — operating β≈0.86 (defensive, below market) vs holding β≈1.38 — a ~0.5 beta gap consistent with holding-company pyramiding/leverage. *Conf:* medium. *Counter:* at index level this is indistinguishable from "the holding portfolio simply held higher-beta names"; per the Evidence Sufficiency Review principle (condition 5), the beta gap *is* the market-exposure difference, not a residual after controlling for it, so it carries no standalone Supports weight and would gain weight only combined with security-level financing data. *Limits:* no capital-structure data to attribute the gap to leverage.

**E-309 | PAT-003 | Weakens (methodological) | S-008 | index construction | historical fact.** The indexes are value-weighted, changing-composition, and chained; a failed constituent that is dropped stops contributing while survivors carry the index — so **survivorship is embedded** and true holding-company investor loss (including total wipeouts) is **understated** by the index drawdown. *Conf:* medium. *Counter:* the understatement, if anything, strengthens "holding was worse." *Limits:* the bias cannot be quantified from the index alone.

**E-310 | PAT-003 | Descriptive (tier-dispersion; no independent Supports weight) | S-008 | QB-1, C-4 vs C-11 vs C-16 | quantitative estimate.** The broad utilities aggregate (C-4, −80.4%) sits between operating (−74.6%) and holding (−89.8%) — the aggregate **masks** the operating/holding dispersion PAT-003 targets. *Conf:* medium (numerical fact). *Counter:* C-4 also includes traction/telephone, so it is not a pure blend of C-11+C-16; beta-absorbed (E-307). *Limits:* C-4 composition not itemized.

**E-311 | PAT-003 | Undecidable-pending-access | S-008 | whole source | historical fact.** Cowles is **index-level only** — no security identities, issuance vintages, capital structure, leverage ratios, or individual delistings — so it cannot on its own establish PAT-003's security-level financing-structure mechanism (which holding companies failed, and why). *Conf:* high. *Limits:* the mechanism requires firm-level data (S-005 FTC / S-012 Moody's / S-011 Taylor — all pending).

**E-312 | PAT-003 | Methodological caveat | S-008 | TR file vs price file base convention | historical fact.** The total-return file is chained to **inception=100 per series** (C-1 Jan-1871, C-11 Oct-1886, C-16 Aug-1890), NOT 1926=100 as commonly assumed; the price file is ≈1926=100. Cross-series **level** comparisons are invalid; only within-series ratios (used throughout QB-1 and E-301–E-310) are sound. *Conf:* high. *Limits:* any downstream claim comparing raw levels across the C-series would be unreliable.

### Module B — Security-level (bounded S-010 sample; everything beyond it is Undecidable-pending-access)

*Tier tags below are the researcher's identity-based classification; CFC does not pre-tag tiers. OCR: integers reliable, eighths uncertain; no digit was invented.*

**E-351 | PAT-003 | Supports (bounded sample) | S-010 | CFC Vol.128 No.3315 (1929-01-05) p.76 | historical fact.** Commonwealth Edison (operating, Insull) declared its regular quarterly dividend of $2.00/share, payable Feb 1 1929. *Conf:* high. *Limits:* declaration ≠ proof of later payment; single issuer.

**E-352 | PAT-003 | Supports (bounded sample) | S-010 | CFC 1929-01-05 p.103 (NY Curb record) | historical fact.** Commonwealth Edison (operating) last sale ~215, week ~207½–219¾, CY1928 range 157 (Jan) – 227 (Dec). *Conf:* medium (issuer name OCR-garbled but unambiguous; integers clean). *Limits:* eighths uncertain.

**E-353 | PAT-003 | Supports (bounded sample) | S-010 | CFC 1929-01-05 p.97 | historical fact.** Middle West Utilities (holding, Insull) week 170–177, CY1928 range 123¾–184. *Conf:* high (integers). *Limits:* holding vehicle; identity-based tag.

**E-354 | PAT-003 | Supports (bounded sample) | S-010 | CFC 1929-01-05 p.2 | historical fact.** American & Foreign Power common (holding, EBASCO) ≈80 on Fri Jan 4 1929 (vs 77½ prior week). *Conf:* high (integer). *Limits:* fraction garbled.

**E-355 | PAT-003 | Supports (bounded sample) | S-010 | CFC 1929-01-05 p.3 | historical fact.** Public Service Corp of New Jersey common 87½ (Jan 4 1929) vs 81½ prior. *Conf:* high. *Limits:* hybrid parent/operating — tiering ambiguous (flagged; authoritative tiering pending S-005).

**E-356 | PAT-003 | Supports (bounded sample) | S-010 | CFC 1929-01-05 p.103 | historical fact.** Electric Bond & Share **preferred** (holding, EBASCO) week ~108¾–109¾. *Conf:* medium. *Counter:* an adjacent heavy-volume no-par line (CY1928 78→180⅞) is likely EB&S common but the OCR label is unreliable → **not** recorded as a clean common quote. *Limits:* label uncertainty.

**E-357 | PAT-003 | Supports (bounded sample) | S-010 | CFC Vol.134 No.3471 (1932-01-02) p.6 | historical fact.** American & Foreign Power common (holding, EBASCO) ≈7 (vs 7⅞ prior). Direct comparand to E-354: ≈80 → ≈7. *Conf:* high. *Limits:* single issuer.

**E-358 | PAT-003 | Supports (bounded sample) | S-010 | CFC 1932-01-02 p.82 | historical fact.** Commonwealth Edison (operating, Insull) 115→118 during the week. Comparand to E-352: ~207–219 → 115–118. *Conf:* high (integers). *Limits:* eighths uncertain.

**E-359 | PAT-003 | Supports (bounded sample) | S-010 | CFC 1932-01-02 p.82 | historical fact.** Electric Bond & Share **common** (holding, EBASCO) ≈10¾–11⅞ that week (vs a CY1928 high near 180⅞ at E-356). *Conf:* medium-high. *Limits:* upper eighth uncertain.

**E-360 | PAT-003 | Supports (bounded sample) | S-010 | CFC 1932-01-02 p.136 (+ p.95 footnote) | historical fact.** Middle West Utilities (holding, Insull) declared its quarterly common dividend as 2% **payable in common stock** (a stock dividend, not cash), and its $6 pref as $1.50 cash **or** 3/80ths share of common — a cash-conservation/distress signal. *Conf:* high. *Limits:* a distress signal, **not** a liquidation outcome (see Undecidable block).

**E-361 | PAT-003 | Supports (bounded sample) | S-010 | CFC 1932-01-02 p.121 | historical fact.** Middle West Utilities (holding, Insull) 5s due 1932 traded at 55, and 5s due 1935 at 38 (per 100 par), Dec 18 1931 — senior-debt-tier distress pricing. *Conf:* high (prices; par amount OCR-ambiguous). *Limits:* single system.

**E-370 | PAT-003 | Undecidable-pending-access | S-010 (limits) → blocked on S-005/S-011/S-012 | historical fact.** The bounded S-010 sample **cannot** establish, and none of the blocked sources may yet be used for: (1) issuance vintage; (2) capital-structure tier / full capitalization and seniority; (3) authoritative operating-vs-holding tiering (esp. hybrids like PSNJ — E-355); (4) individual delisting / quotation-cessation dates; (5) liquidation / recovery outcomes (the Insull collapse of April–June 1932 post-dates the Jan-1932 issue; the distress signals E-360/E-361 are **not** liquidation outcomes); (6) population-scale security-level reconstruction (this is a capped 5-issuer sample); (7) security-level total return; (8) dividend continuity / actual payment. *Method finding:* reliable table extraction from the ~104–112 MB rough-OCR CFC issues is partially defeated for the NYSE columnar "Stock Record" and "Dividends Declared" tables (names split from number columns); the NY Curb records and prose reviews are readable, which is where E-351–E-361 come from. A population sweep would require manual/visual table work, not OCR — or the pending sources (S-012 Moody's, S-005 FTC, S-011 Taylor). *Conf:* high (as a scope statement).

---

## Anti-Confirmation Balance Check (per brief §8.4)

The RA requires that no Pattern's Weakens/Rejects lane be "obviously weaker" than its Supports lane. Assessment (restated per the Evidence Sufficiency Review, condition 6, on the post-correction lane weights):

- **PAT-001.** **Coexisting-divergence Supports** can be synthesized (E-101–E-104, E-108 on the value side; E-114/E-115 on the investor-return side — both load-bearing) **but only as coexisting divergence, not as a value transfer.** The **matched-cohort value-transfer question is Undecidable with current evidence (E-118)**, and the **Rejects test was executed and "Rejects not established" (E-117)** — it does not convert to Supports. Weakens/limitations remain strong: E-105 (markups capture), E-106 (hydro/shared attribution), E-107 (localization; national signal slow), E-113 (different-constructs, load-bearing), E-112 (financing-efficiency counter), E-116 (holding a poor pre-1920 compounder). E-109 carries **no** outcome weight. **Balanced; Supports capped by an explicit Undecidable and a not-established Rejects.**
- **PAT-002.** Supports: E-201–E-203, E-206–E-207 (capacity/output/utilization; the 1929→1932 utilization drop). Weakens/Rejects: E-204/E-205 (capacity rose into falling demand = pipeline; recovery not by scrapping), E-208 (utilization drop ≈55% demand shock), E-209 (recovery on frozen capacity), E-211 (mid-decade capacity wave / transient slack), **E-210 (Rejects: 1920s capacity tracked demand ~1:1, flat utilization), E-218 (measurement biases understate utilization)**. **The Weakens/Rejects lane is at least as strong as — arguably stronger than — Supports: a US national physical-overbuild reading is not supported in the 1920s, and the crash-era utilization drop is majority demand shock.** Not obviously weaker.
- **PAT-003.** **Index-tier dispersion is observed (descriptive: E-301–E-305, E-310, E-308) but carries no independent Supports weight — the beta attribution fully absorbs the index residual (E-307, load-bearing Weakens); no mechanism-relevant residual survives a broad-market control.** The **security-level financing/entry mechanism is Undecidable-pending-access (E-311, E-370)**; the bounded S-010 sample (E-351–E-361) is qualitatively consistent but cannot establish vintage, capital structure, delistings, liquidation, or population-scale return. Additional Weakens: E-306, E-309 (survivorship). **There is currently no claim carrying standalone PAT-003 Supports weight; the Supports column for the full Pattern is effectively empty pending security-level data.** Not obviously weaker — if anything Weakens/Undecidable dominate.

**Conclusion:** after the condition-1–5 reclassifications, each Pattern's Weakens/Rejects/Undecidable lanes are **not** obviously weaker than its Supports lane — indeed for PAT-002 and PAT-003 they dominate. The ledger meets the anti-confirmation gate.

## Carried gaps / Undecidable-pending-access

1. **PAT-003 security-level mechanism** — issuance vintage, capital-structure tier, individual delistings, liquidation outcomes, population-scale reconstruction, security-level total return: all Undecidable-pending-access, blocked on S-012 (Moody's PU manuals), S-005 (FTC full text via a browser HathiTrust session), and S-011 (Taylor 1962). A bounded access escalation was recommended in the Source Register Stage B section; not yet granted.
2. **Pure-electric isolation** — S-008 mixes electric + gas ("Etc."); no pure-electric utility return series is available.
3. **PAT-002 pre-1920** — quinquennial only and ±20–25% definitional variance; the strong physical window is ~1920–1935.
4. **PAT-001 construct gap** — productivity and investor-return evidence are different constructs on different units; only coexisting divergence is establishable, never a matched-cohort value transfer (E-118 Undecidable).
5. **S-016/S-017** — orientation/framing only (S-016 not load-bearing; S-017 carries no numeric estimate).

## Evidence Sufficiency Review — result and fixed synthesis boundaries

**Verdict: PASS WITH CONDITIONS → PASS.** The Research Architect's Evidence Sufficiency Review returned PASS WITH CONDITIONS with six required ledger corrections; **all six are applied in this ledger** (condition 1 → E-109 reclassified to no-outcome-weight adjacency; condition 2 → E-117 Rejects "not established" disposition added; condition 3 → E-118 matched-cohort value-transfer Undecidable added; condition 4 → E-211 reclassified to Weakens, pending-access removed; condition 5 → E-301–E-305, E-308, E-310 relabelled Descriptive / no independent Supports weight; condition 6 → Anti-Confirmation Balance Check restated above). The review therefore stands at **PASS — the historical synthesis `REV-HIST-002` is authorized.** Full record: `governance/HIS-002_GATE_2_REVIEW.md` (`id: HIS-002-GATE-2`).

**Three fixed boundaries the synthesis (`REV-HIST-002`) must carry (RA-imposed):**
1. **PAT-001** — coexisting divergence only, **not** a matched-cohort value transfer (E-113, E-117, E-118).
2. **PAT-002** — a US 1920s national physical overbuild is **not supported**; the 1930s slack is mainly a combination of Depression demand shock and pre-1929 pipeline capacity (E-208, E-210, E-204/E-205).
3. **PAT-003** — index-tier dispersion exists but is **absorbed by market beta**; the security-level financing/entry mechanism remains **Undecidable-pending-access** (E-307, E-311, E-370).

Pattern statuses are unchanged by this review: `PAT-001`/`PAT-002` `draft`, `PAT-003` `validated-in-one-cycle`. No Pattern verdict is set here; cross-cycle Matrix verdicts are set later (after the synthesis passes Gate 3), per `governance/PATTERN_VALIDATION_FRAMEWORK.md` §8.

## Stage C stop point

HIS-002 Evidence Ledger complete and its Evidence Sufficiency Review conditions applied. No historical synthesis has yet been written; the Pattern Validation Matrix HIS-002 verdicts remain **pending** (not updated); no Pattern has been promoted; no `MAP-001`, `THS-001`, AI-era mapping, or investment conclusion has been created. **Next authorized deliverable: `REV-HIST-002` historical synthesis, carrying the three fixed boundaries above, then Gate 3 (Historical Stability Review).**
