---
id: HIS-001-EVIDENCE-LEDGER
type: evidence-ledger
title: HIS-001 Evidence Ledger
status: draft
created: 2026-07-12
updated: 2026-07-12
owner: cyberbird
research_lead: claude-code
research_architect: chatgpt
review_date: 2026-08-01
confidence: low
sources: []
related:
  - HIS-001
  - HIS-001-SOURCE-REGISTER
---

# HIS-001 Evidence Ledger

Stage C deliverable. Every substantive future narrative claim (in `REV-HIST-001`) must exist here first, tied to a source **actually read** at an **exact location**, with unit/period/sample explicit and counter-evidence recorded. Built by reading the full text of the Tier 1 verified sources (see `HIS-001_SOURCE_REGISTER.md`), extracted from local full-text copies of each source via `curl` + `pypdf`/`bs4`.

**No AI-era analogy claims exist in this ledger** (forbidden in Stage C). No historical narrative, Pattern, Mapping, or Thesis has been created.

## How to read

- **Claim ID scheme (stable, block-allocated per section so IDs never renumber):** C1 Technology/cost/diffusion `C-001–C-049`; C2 Capital formation/overbuild `C-050–C-099`; C3 Prices/investor returns `C-100–C-149`; C4 Cash-flow reconstruction `C-150–C-179`; C5 Operating vs shareholder return `C-180–C-219`; C6 Failure/impairment `C-220–C-269`; C7 Competing interpretations `C-270–C-309`; C8 Canals + US comparative `C-310–C-349`.
- **Classification** ∈ {`historical fact`, `quantitative estimate`, `scholarly interpretation`, `research inference`}. (`ai-era analogy` is defined in governance but is **not used** in Stage C.)
- **Status** ∈ {`supported`, `partially-supported`, `contested`, `gap`, `rejected`, `undecidable`}.
- **Source key** references the entry in `HIS-001_SOURCE_REGISTER.md`. **Location** is the page/section/table/figure as printed in the document.
- Branch = question-tree branch (QT1–QT6, plan §1). Hypotheses H1–H5 per the brief.

## Provenance corrections surfaced during extraction (also applied to the Source Register)

1. **`B5-McCartney-ManagerialFailure-2024` is mis-keyed.** The file read at `railwaymania_managerial.txt` is actually **Campbell & Turner (2015), "Managerial Failure in Mid-Victorian Britain?"** (Business History, DOI 10.1080/00076791.2015.1026260) — byline read directly from its title page. Re-keyed here as `B5-CampbellTurner-ManagerialFailure-2015`. See C-197.
2. **The York & North Midland 10.1% / −0.3% return-to-equity figure** (and the parallel 14% / 2.3% figure) originates in **McCartney & Arnold (2001), "Capital Clamours for Profitable Investment…"** (Journal of Industrial History 4(2): 94–116), cited by Campbell & Turner (2015) and by Odlyzko. The 2001 primary was **not read** — claims resting on it are two-hop citations, marked `partially-supported`. See C-191, C-194, C-229.
3. The Dec-1870-IMM survivorship check + buy-and-hold/−100% bounds belong to **Rule Britannia! (Acheson et al. 2009)**, not "Before the Cult of Equity" (which does no survivorship adjustment). See C-102, C-131, C-132.
4. Donaldson & Hornbeck's result is **"moderately larger,"** 3.22% of GNP vs Fogel's 2.7% — **not "more than double."** See C-273.

---

## Section C1 — Technology, cost decline, and diffusion

Sources: `B4-Crafts-2004` (Crafts 2004, LSE WP 75/03), `B4-Bottomley-2025` (Bottomley 2024/25, EHR 78(3)).

### C-001
- **Branch:** QT1.1 · **Hyp:** — · **Class:** quantitative estimate · **Status:** supported
- **Claim:** Steam power did not overtake water as Britain's dominant source of installed mechanical horsepower until 1830, ~60 years after Watt's patent, and even then was only ~1.5% of the total capital stock.
- **Evidence/quote:** "it was only in 1830 that steam reached parity with water as a source of power in the economy at which point only 160,000 steam horse power had been installed representing about 1.5 per cent of the total capital stock."
- **Source/loc:** B4-Crafts-2004, p.4–5 + Table 3 p.18 · **Period:** 1760–1830 · **Geo:** Great Britain · **Unit:** installed hp by prime-mover type; % of capital stock · **Conf:** medium
- **Counter/limits:** Bottomley (2025) argues the Factory-Return-based series undercounts steam from 1838 (see C-016/C-019); 1800–1838 data gap; Kanefsky figures "broadly accurate" only.

### C-002
- **Branch:** QT1.2 · **Hyp:** — · **Class:** quantitative estimate · **Status:** supported
- **Claim:** Steam-engine fuel efficiency (coal per installed hp per year) improved ~15-fold from the pre-Watt Newcomen engine to early-20th-century very-high-pressure engines.
- **Evidence/quote:** "coal consumption (per hp per year) improved from about 30 lb. with the Newcomen engines prior to James Watt, to 12.5 lb. with the Watt engine, 5 lb. with the move to high pressure in the mid 19th century and 2 lb with very high pressure in the early 20th century."
- **Source/loc:** B4-Crafts-2004, p.5 · **Period:** pre-1769 – early 20th c. · **Geo:** Great Britain · **Unit:** lb coal per installed hp per **year** (not per hour) · **Conf:** medium
- **Counter/limits:** Four discrete benchmark points, not a series; likely stationary/textile-mill practice, not locomotives.

### C-003
- **Branch:** QT1.2 · **Hyp:** — · **Class:** quantitative estimate · **Status:** supported
- **Claim:** Maximum working steam pressure in British textile mills rose from 60 psi (1850) to 200 psi (1900).
- **Evidence/quote:** "maximum steam pressure in textile mills had risen from 60 in 1850 to 200 p.s.i in 1900 (Hills, 1989)."
- **Source/loc:** B4-Crafts-2004, p.5 · **Period:** 1850–1900 · **Geo:** GB textile mills · **Unit:** psi max working pressure · **Conf:** medium
- **Counter/limits:** Sector-specific; single secondary citation.

### C-004
- **Branch:** QT1.3 · **Hyp:** — · **Class:** quantitative estimate · **Status:** supported
- **Claim:** Annual cost of a benchmark steam hp in a low-coal-cost Lancashire textile mill fell from £33.5/yr (1760) to £4.0/yr (1910); capital cost per hp from £42 to £15 (current prices).
- **Evidence/quote:** "the estimates are for a benchmark textile mill in a low coal cost region like Manchester annual costs include depreciation and interest costs, and running costs including coal and labour."
- **Source/loc:** B4-Crafts-2004, Table 4 p.19 + text p.6 · **Period:** 1760–1910 · **Geo:** benchmark Manchester mill (national proxy) · **Unit:** £ current per steam hp per year · **Conf:** medium
- **Counter/limits:** Single-sector/region, explicitly non-representative; Bottomley disputes the substitutability assumption behind such cost series (C-021).

### C-005
- **Branch:** QT1.3 · **Hyp:** — · **Class:** quantitative estimate · **Status:** supported
- **Claim:** US evidence corroborates scale: annual cost per hp of US steam fell just over 80% between the 1820s and 1890s.
- **Evidence/quote:** "the annual costs of a horsepower of steam fell by just over 80 per cent between the 1820s and the 1890s Atack (1979, p. 423)."
- **Source/loc:** B4-Crafts-2004, p.6 · **Period:** 1820s–1890s · **Geo:** United States (external cross-check) · **Unit:** % decline in annual $ cost per hp · **Conf:** medium
- **Counter/limits:** From Atack's simulation, not archival cost records; US geography, analogical use only.

### C-006
- **Branch:** QT1.4 · **Hyp:** — · **Class:** quantitative estimate · **Status:** partially-supported
- **Claim:** Stationary-steam contribution to British labour-productivity growth was negligible before 1830, peaking at 0.12 pp/yr in 1850–70 (0.14 in 1870–1910).
- **Evidence/quote:** "The contribution to growth made by the stationary steam engine was very small prior to 1830, was considerably bigger in the second half of the 19th century than during the industrial revolution but was always quite modest."
- **Source/loc:** B4-Crafts-2004, Table 5 p.20 + p.8 · **Period:** 1760–1910 · **Geo:** GB · **Unit:** pp/yr contribution to labour-productivity growth · **Conf:** medium
- **Counter/limits:** Derived from the single-sector Table-4 cost benchmark; model-dependent; Bottomley's undercount would affect the capital-deepening input.

### C-007
- **Branch:** QT1.4 · **Hyp:** — · **Class:** quantitative estimate · **Status:** partially-supported
- **Claim:** Steam (stationary + railways) contribution to British labour-productivity growth peaked at 0.38 pp/yr in 1850–70, falling to 0.21 in 1870–1910.
- **Evidence/quote:** Table 7: 1760-1800 0.01; 1800-30 0.02; 1830-50 0.20; 1850-70 0.38; 1870-1910 0.21 (%/yr).
- **Source/loc:** B4-Crafts-2004, Table 7 p.22 · **Period:** 1760–1910 · **Geo:** GB · **Unit:** pp/yr (capital-deepening + own-TFP) · **Conf:** medium
- **Counter/limits:** Never approaches ICT's 0.68 pp/yr (C-010); inherits all upstream Table 4–6 assumptions; omits spillovers (C-012).

### C-008
- **Branch:** QT1.4 · **Hyp:** — · **Class:** quantitative estimate · **Status:** supported
- **Claim:** Railways alone contributed at most 0.26 pp/yr to British labour-productivity growth (1850–70), despite railway capital stock reaching 30% of GDP by 1855.
- **Evidence/quote:** "by 1855 their capital stock was equal to 30 per cent of GDP." Table 6 total contribution: 0.16 (1830-50), 0.26 (1850-70), 0.07 (1870-1910).
- **Source/loc:** B4-Crafts-2004, Table 6 p.21 + p.6 · **Period:** 1830–1910 · **Geo:** GB (England & Wales for underlying Hawke) · **Unit:** pp/yr; % of GDP · **Conf:** medium
- **Counter/limits:** Pre-1870 from Hawke 1970, post-1870 from Foreman-Peck 1991 — a methodological splice; same social-savings method Bottomley critiques (C-021).

### C-009
- **Branch:** QT1.5 · **Hyp:** — · **Class:** scholarly interpretation · **Status:** supported
- **Claim:** Steam's peak productivity impact was delayed ~80 years after Watt's 1769 patent — about twice electricity's ~40-year US lag.
- **Evidence/quote:** "the lag following James Watt's steam engine was about 80 years."
- **Source/loc:** B4-Crafts-2004, p.10 · **Period:** 1769–1850s · **Geo:** GB (steam), US (electricity comparator) · **Unit:** years to peak measured contribution · **Conf:** medium
- **Counter/limits:** "~80 years" is retrospectively constructed from when Table 5/7 peaks; cross-study comparability asserted.

### C-010
- **Branch:** QT1.5 · **Hyp:** — · **Class:** quantitative estimate · **Status:** supported
- **Claim:** Steam's annual productivity-growth contribution never matched ICT's 0.68 pp/yr (US, 1974–90); "no equivalent to Moore's Law in the age of steam."
- **Evidence/quote:** "at no time does steam's contribution match the 0.68 per cent per year of ICT in 1974-90... there was no equivalent to Moore's Law in the age of steam."
- **Source/loc:** B4-Crafts-2004, p.8–9 + Table 2 p.17 + Table 7 p.22 · **Period:** 1760–1910 (steam) vs 1974–90 (ICT) · **Geo:** GB vs US · **Unit:** pp/yr, same growth-accounting formula · **Conf:** medium-high
- **Counter/limits:** Crafts flags ICT's hedonic deflation exaggerates the gap by <0.1 pp/yr each component (fn 1); cross-country/era comparison.

### C-011
- **Branch:** QT1.6 · **Hyp:** — · **Class:** scholarly interpretation · **Status:** supported
- **Claim:** The hypothesis that a late-19th-c. "climacteric" was caused by weakening steam application is not supported; the aggregate TFP climacteric fails econometric testing, and industrial steam mechanization was still accelerating.
- **Evidence/quote:** "the revisionist notion of a late 19th century climacteric in TFP growth at the level of the aggregate economy does not survive serious econometric investigation (Crafts et al., 1989)... any reduction in TFP growth from steam was very small − around 0.1 percentage points."
- **Source/loc:** B4-Crafts-2004, p.11 (+ fn 2) · **Period:** 1870–1910 · **Geo:** GB · **Unit:** pp change in steam-attributable TFP growth · **Conf:** medium
- **Counter/limits:** Rests on one time-series reanalysis (Crafts/Leybourne/Mills 1989); engages the older Phelps-Brown climacteric claim and Musson's counter.

### C-012
- **Branch:** QT1.7 · **Hyp:** — · **Class:** scholarly interpretation · **Status:** partially-supported
- **Claim:** Steam TFP spillovers were likely negligible pre-1850 but possibly larger after; the Corliss engine (first UK install 1861) illustrates efficiency/agglomeration gains.
- **Evidence/quote:** "The first Corliss steam engine was installed in Britain in 1861." (reporting Rosenberg & Trajtenberg 2001 on valve gear enabling agglomeration).
- **Source/loc:** B4-Crafts-2004, p.9 · **Period:** pre/post-1850; 1861 · **Geo:** GB · **Unit:** qualitative — spillover magnitude not quantified · **Conf:** low-medium
- **Counter/limits:** Crafts states his tables quantify no spillovers; reports another paper's claim, entirely non-quantified.

### C-013
- **Branch:** QT1.4 · **Hyp:** — · **Class:** research inference · **Status:** supported
- **Claim:** TFP growth attributable to steam in 1800–30 can be bounded only to −0.6% to +1.2%/yr; Crafts states his conclusions are insensitive within this band.
- **Evidence/quote:** "the bounds within which TFP growth lies is −0.6 to 1.2 per cent per year. None of the major conclusions of this paper would change significantly..."
- **Source/loc:** B4-Crafts-2004, p.7–8 · **Period:** 1800–1830 · **Geo:** GB (Cornwall vs Manchester divergence) · **Unit:** % TFP growth/yr in steam provision · **Conf:** medium
- **Counter/limits:** ~2 pp band is wide relative to Table-5 contributions (mostly <0.2%/yr); regional divergence shows measurement fragility.

### C-014
- **Branch:** QT1.2 · **Hyp:** — · **Class:** historical fact · **Status:** supported
- **Claim:** Fuel-efficient high-pressure steam was bottlenecked by boiler tech: pioneered by Woolf in Cornwall early-19th-c., but only economic in textile mills after the Lancashire boiler (early 1840s).
- **Evidence/quote:** "only after the invention of the Lancashire boiler in the early 1840s were they an economic proposition in textile mills (von Tunzelmann, 1978)."
- **Source/loc:** B4-Crafts-2004, p.5 · **Period:** early-19th-c. – early 1840s · **Geo:** Cornwall→Lancashire · **Unit:** qualitative complementary-asset chronology · **Conf:** high
- **Counter/limits:** Single secondary citation; Lancashire-boiler contribution not separately quantified.

### C-015
- **Branch:** QT1.1 · **Hyp:** — · **Class:** historical fact · **Status:** contested
- **Claim:** As late as 1870, ~half of British steam power was still in mining and cotton textiles; agriculture/services "virtually untouched" — per Factory-Return-based estimates.
- **Evidence/quote:** "Even in 1870 almost half of all steam power was used in mining and in cotton textiles while important sectors... were virtually untouched by steam."
- **Source/loc:** B4-Crafts-2004, p.5 · **Period:** 1870 · **Geo:** GB · **Unit:** sectoral share of installed steam hp · **Conf:** medium
- **Counter/limits:** **Directly rejected by Bottomley (2025)**: "the suggestion that large parts of the economy 'were virtually untouched by steam' is an artefact of [the Factory Returns' incompleteness]"; his revised 1870 UK total is 3.30m ihp vs 2.07m (C-016). Clearest Crafts–Bottomley contradiction.

### C-016
- **Branch:** QT1.8 · **Hyp:** — · **Class:** quantitative estimate · **Status:** contested (revises the Kanefsky/Crafts consensus)
- **Claim:** Bottomley's reconstruction implies UK installed steam capacity in 1870 was ≥3,297,150 ihp — ~60% above Kanefsky's 2,065,000 ihp (the figure under Crafts 2004).
- **Evidence/quote:** "whereas Kanefsky estimates a total installed capacity in the United Kingdom (including Ireland) of 2,065,000 ihp for steam, here the estimate is 60 per cent higher at 3,297,150 ihp."
- **Source/loc:** B4-Bottomley-2025, p.14 + Table 3 p.15 · **Period:** 1870 · **Geo:** UK incl. Ireland (Suffolk extrapolation) · **Unit:** ihp installed capacity · **Conf:** medium
- **Counter/limits:** Single-county extrapolation with sector scaling rules; author calls county figures a lower bound.

### C-017
- **Branch:** QT1.8 · **Hyp:** — · **Class:** quantitative estimate · **Status:** supported
- **Claim:** For Suffolk 1850 the Factory Return recorded 17 nhp of steam (3 silk-mill engines) vs Bottomley's census of 66 engines / 697 nhp — a ~41× undercount.
- **Evidence/quote:** "The Factory Return for 1850 records a total of 17 nhp... By contrast, the census indicates that there were 66 stationary steam engines working in Suffolk, yielding a combined 697 nhp."
- **Source/loc:** B4-Bottomley-2025, p.10 + Table 1 p.11 · **Period:** 1850 · **Geo:** Suffolk · **Unit:** nhp installed capacity · **Conf:** high
- **Counter/limits:** Discrepancy mostly a scope artifact (1850 Return = textile mills only); census assumes 8 ihp for unrated engines (downward bias).

### C-018
- **Branch:** QT1.8 · **Hyp:** — · **Class:** quantitative estimate · **Status:** supported
- **Claim:** For Suffolk 1870 (a "full" return county) the Factory Return recorded 1,792 ihp vs Bottomley's 5,186 ihp / 305 engines — ~3× the official figure, even post-1867 extension.
- **Evidence/quote:** Table 2 final row "Total 1792 5161 5186 305" (Factory Return / census comparable sectors / combined / engines).
- **Source/loc:** B4-Bottomley-2025, p.12 + Table 2 p.13–14 · **Period:** 1870 · **Geo:** Suffolk · **Unit:** ihp in use (nhp→ihp and capacity→use adjusted) · **Conf:** high
- **Counter/limits:** Suffolk had an unusually diligent inspector → undercount ratio may be a lower bound elsewhere; ihp "in use" ≠ capacity.

### C-019
- **Branch:** QT1.8 · **Hyp:** — · **Class:** quantitative estimate · **Status:** partially-supported
- **Claim:** Extrapolated nationally, British manufacturing used ≥2× the previously-estimated 1870 steam: Bottomley's omitted-steam estimate is 1,009,000 ihp vs Kanefsky's 195,347 ihp (steam+water).
- **Evidence/quote:** "Here, the figure for steam alone is 1,009,000 ihp... at least twice as much steam power in British manufacturing in 1870 than previously thought."
- **Source/loc:** B4-Bottomley-2025, p.14 · **Period:** 1870 · **Geo:** UK manufacturing (Suffolk extrapolation) · **Unit:** ihp omitted from Factory Return · **Conf:** medium
- **Counter/limits:** National claim on one agrarian county; industrial counties untested; no CI given; explicit lower bound.

### C-020
- **Branch:** QT1.1 · **Hyp:** — · **Class:** quantitative estimate · **Status:** partially-supported
- **Claim:** Suffolk steam was negligible into the 1830s (16 engines / 145 nhp in 1837) then took off, doubling every 6–7 years to 1870 — and the take-off preceded widespread high-pressure industrial steam.
- **Evidence/quote:** "As late as 1837, there were only 16 (documented) engines... After this, however, we enter the 'take-off' stage... doubling every 6–7 years until at least 1870. This 'take-off' precedes the widespread application of high-pressure steam..."
- **Source/loc:** B4-Bottomley-2025, p.16 + Fig. 1 p.17 · **Period:** 1800–1870 (inflection c.1837) · **Geo:** Suffolk · **Unit:** ihp capacity; doubling period · **Conf:** medium
- **Counter/limits:** Complicates the Crafts/von Tunzelmann high-pressure-diffusion narrative (C-002/C-014); attributed instead to falling coastal coal-freight costs (Ipswich wet dock 1842); engines dated to first record (conservative).

### C-021
- **Branch:** QT1.9 · **Hyp:** — · **Class:** scholarly interpretation · **Status:** contested
- **Claim:** The social-savings "modest contribution" conclusion rests on an assumption — steam always substitutable with water/wind at only a cost difference — that is untenable where no environmental power could meet the requirement.
- **Evidence/quote:** "Social savings' assumption of substitutability predetermines its results."
- **Source/loc:** B4-Bottomley-2025, p.17 + p.21 · **Period:** 19th c. · **Geo:** GB · **Unit:** qualitative methodological critique of B4-Crafts-2004's framework · **Conf:** medium-high
- **Counter/limits:** Crafts already flags omitted spillovers (C-012); the two partly agree the method understates steam but disagree on magnitude; Bottomley offers no aggregate re-estimate to replace Table 7.

### C-022
- **Branch:** QT1.9 · **Hyp:** — · **Class:** historical fact · **Status:** supported
- **Claim:** Steam had no feasible environmental substitute for concentrated urban infrastructure: London main-drainage pumping needed 2,528 ihp combined (Abbey Mills 1,168 ihp) vs a max ~40 ihp from the best waterwheel.
- **Evidence/quote:** "four massive pumping stations, generating a combined 2528 ihp... This concentration of power output was not technically feasible using water power. An 'above average' vertical waterwheel of the period generated 40 ihp."
- **Source/loc:** B4-Bottomley-2025, p.18 · **Period:** from 1875 · **Geo:** London · **Unit:** ihp per installation · **Conf:** high
- **Counter/limits:** One extreme case; world's most powerful waterwheel ~280 ihp, still far short.

**C1 gaps:** railway freight/passenger cost-decline series — **GAP** (absent from Crafts & Bottomley; do not infer). Locomotive coal-per-hp-hour — partial gap (only per-year, stationary context). A single reconciled national steam-diffusion series — the Crafts (2.07m ihp) vs Bottomley (3.30m ihp) 1870 estimates are unreconciled (recorded as `contested`, not adjudicated).

---

## Section C2 — Capital formation and overbuild

Sources: `A5-Odlyzko-Collapse-2011`, `A2-Campbell-Deriving-2013`, `B5-MitchellChambersCrafts-2011`, `A1-NBER-FRED-Mileage`.

### C-050
- **Branch:** QT2.1 · **Hyp:** H3 · **Class:** quantitative estimate · **Status:** supported
- **Claim:** By Nash's end-1848 tabulation, the 42 main British lines had invested £172m of equity + loan capital against £268m Parliamentary authorizations (~64% realized; ~£96m authorized-but-uninvested).
- **Evidence/quote:** "the 42 main lines that he was tracking had invested a total of £172 million in equity and loan capital. They had Parliamentary authorizations to raise a total of £268 million."
- **Source/loc:** A5-Odlyzko-Collapse-2011, p.6–7 · **Period:** end-1848 · **Geo:** GB (42 lines) · **Unit:** £m invested vs £m authorized · **Conf:** medium
- **Counter/limits:** Nash's figures are a journalist's compilation, not audited; LNWR disputed its own figure (C-067); 42-line subset only.

### C-051
- **Branch:** QT2.1 · **Hyp:** H3 · **Class:** quantitative estimate · **Status:** supported
- **Claim:** Within Nash's £172m "invested," only £138m had gone to revenue-service mileage, and only ~£99m was capital the latest accounts treated as chargeable to/earning revenue — three nested quantities.
- **Evidence/quote:** "The revenue-producing mileage had at that stage cost £138 million, but the portion of this capital which... was made chargeable upon revenue, or which received dividend and interest from revenue, was [£99 million]."
- **Source/loc:** A5-Odlyzko-Collapse-2011, p.6–7 · **Period:** end-1848 · **Geo:** GB (42 lines) · **Unit:** £m, invested ⊃ completed-mileage cost ⊃ dividend-earning capital · **Conf:** medium
- **Counter/limits:** "[£99m]" is Odlyzko's bracketed reconstruction of Nash's wording.

### C-052
- **Branch:** QT2.1 · **Hyp:** H3 · **Class:** research inference · **Status:** partially-supported
- **Claim:** Nash projected the capital "chargeable upon revenue" across the 42 lines would ~double from ~£99m to £198m within 2–3 years (by ~1850–51), even on a conservative £26m-to-complete assumption.
- **Evidence/quote:** "the capital becoming chargeable upon the general revenue of the whole will, in the course of the next two or three years, be 198 millions, or exactly double the present amount."
- **Source/loc:** A5-Odlyzko-Collapse-2011, p.7 · **Period:** end-1848 → ~1850–51 · **Geo:** GB (42 lines) · **Unit:** £m projected · **Conf:** low-medium
- **Counter/limits:** Nash calls his £26m completion estimate "very insufficient" (lower bound); a forecast, no realized reconciliation in the file.

### C-053
- **Branch:** QT2.2 · **Hyp:** H3 · **Class:** quantitative estimate · **Status:** partially-supported
- **Claim:** Actual UK railway construction investment rose £13m (1845) → £30m (1846) → £44m peak (1847, ~8% of GDP, twice the 1847 military budget), not falling back to £13m/yr until 1850.
- **Evidence/quote:** "rising from £13 million in 1845, to £30 million in 1846, and a peak of £44 million in 1847, almost 8% of British GDP, and twice the military budget of that year... did not decline back to the £13 million per year level until 1850."
- **Source/loc:** A5-Odlyzko-Collapse-2011, p.3 · **Period:** 1845–1850 · **Geo:** GB · **Unit:** £m/yr actual construction spend (flow) · **Conf:** medium
- **Counter/limits:** GDP share contested by Mitchell 1964 (C-064); underlying GDP denominator in an uncollected companion manuscript, unverifiable here.

### C-054
- **Branch:** QT2.3 · **Hyp:** H3 · **Class:** quantitative estimate · **Status:** supported
- **Claim:** Mileage in service tripled 2,240 (1844) → 6,890 (1851); avg construction cost/mile £35,700 (1844) then £31,700–£35,200 (1847–51); revenue/mile fell £3,280 (1844) → £2,080–£2,220 (1850–51).
- **Evidence/quote:** Table 1 (Tooke & Newmarch): 1844: 2,240 mi/£35,700/£3,280; 1847: 3,945/£31,700/£2,870; 1851: 6,890/£35,100/£2,220.
- **Source/loc:** A5-Odlyzko-Collapse-2011, p.8 (Table 1) · **Period:** 1844–1851 · **Geo:** GB · **Unit:** miles in service; £/mile cost; £/mile revenue · **Conf:** medium
- **Counter/limits:** Industry-wide aggregate (includes established-line spend); Odlyzko notes alternate tables differ slightly; primary Tooke & Newmarch not independently read.

### C-055
- **Branch:** QT2.4 · **Hyp:** H3 · **Class:** scholarly interpretation · **Status:** partially-supported
- **Claim:** Had every Parliament-sanctioned Mania project been built, mileage would have grown ×5 not ×3 — realized overbuild was severe but well short of full execution.
- **Evidence/quote:** "Had all the projects sanctioned by Parliament been carried out, British railway mileage would have grown by a factor of 5, not 3, and a far greater investment disaster would surely have resulted."
- **Source/loc:** A5-Odlyzko-Collapse-2011, p.8 · **Period:** 1844–1851 vs counterfactual · **Geo:** GB · **Unit:** mileage-growth ratio · **Conf:** medium
- **Counter/limits:** No itemized authorized-mileage total shown; cross-check vs FRED (C-063).

### C-056
- **Branch:** QT2.4 · **Hyp:** H3 · **Class:** quantitative estimate · **Status:** supported
- **Claim:** Only ~half of the mileage authorized during the Mania had been built by 1853.
- **Evidence/quote:** "Only about half of the total mileage authorized by Parliament during the Mania was actually built by 1853."
- **Source/loc:** A5-Odlyzko-Collapse-2011, p.33 · **Period:** 1844–47 auth. vs 1853 built · **Geo:** GB · **Unit:** share of authorized route-mileage built · **Conf:** medium
- **Counter/limits:** No citation in-passage; Odlyzko's synthesis; consistent with C-055.

### C-057
- **Branch:** QT2.5 · **Hyp:** H3 · **Class:** historical fact · **Status:** supported
- **Claim:** The financing mechanism required only a small deposit at subscription with the rest collected via later "calls" — so subscribed, called, and paid capital were three distinct quantities.
- **Evidence/quote:** "it was usual for initial shareholders to pay only a small deposit when a company was formed, and then to pay the rest... in installments, in response to 'calls' from management as funds were needed."
- **Source/loc:** A5-Odlyzko-Collapse-2011, p.10 · **Period:** 1840s · **Geo:** GB · **Unit:** institutional/procedural · **Conf:** high
- **Counter/limits:** Corroborated by Campbell (C-058).

### C-058
- **Branch:** QT2.5 · **Hyp:** — · **Class:** historical fact · **Status:** supported
- **Claim:** Campbell's definitions: nominal value = total eventual obligation; par value = amount paid to date; uncalled capital = nominal − par. These map to authorized/subscribed, paid, and called-but-outstanding.
- **Evidence/quote:** "The total amount that subscribers were obliged to pay... was referred to as the nominal value... The amount that shareholders had already paid... was referred to as the par value. The difference... reflected uncalled capital."
- **Source/loc:** A2-Campbell-Deriving-2013, p.6–7 · **Period:** 1843–1850 · **Geo:** GB (LSE) · **Unit:** £/share definitions · **Conf:** high
- **Counter/limits:** Operational definition for Campbell's dataset; matches contemporary usage.

### C-059
- **Branch:** QT2.5 · **Hyp:** H3 · **Class:** quantitative estimate · **Status:** supported
- **Claim:** During 1844–45, aggregate nominal (subscribed) capital of new schemes rose dramatically while par (paid) capital rose only gradually — investors were mainly increasing liabilities, not injecting capital.
- **Evidence/quote:** "Rather than investing large amounts of capital, investors were actually increasing their liabilities at this time."
- **Source/loc:** A2-Campbell-Deriving-2013, p.22–23 (Fig. 8) · **Period:** 1844–1845 · **Geo:** GB (LSE new schemes) · **Unit:** aggregate nominal vs par value · **Conf:** medium-high
- **Counter/limits:** Underlying Fig. 8 £-values not recoverable from the text; only the directional claim verified.

### C-060
- **Branch:** QT2.5 · **Hyp:** H3 · **Class:** historical fact · **Status:** supported
- **Claim:** Parliament's minimum deposit requirement was cut from 10% to 5% (Feb 1844) then raised back to 10% (Jul 1845), directly affecting the subscribed-vs-paid gap.
- **Evidence/quote:** "in an attempt to make railway investment easier it was proposed that this should be reduced to 5 per cent in February 1844... it was raised to 10 per cent again in July 1845."
- **Source/loc:** A2-Campbell-Deriving-2013, p.23 · **Period:** 1837–1845 · **Geo:** GB · **Unit:** min deposit as % of nominal · **Conf:** high
- **Counter/limits:** Policy fact; Hansard citation not independently checked.

### C-061
- **Branch:** QT2.6 · **Hyp:** H3 · **Class:** quantitative estimate · **Status:** supported
- **Claim:** At least 1,000 new railway lines were projected during the Mania — far more than were authorized or built.
- **Evidence/quote:** "with at least 1,000 new railway lines being projected at this time."
- **Source/loc:** A2-Campbell-Deriving-2013, p.2 · **Period:** mid-1840s · **Geo:** GB · **Unit:** count of projected lines · **Conf:** medium
- **Counter/limits:** Round "at least" figure; no breakdown by outcome.

### C-062
- **Branch:** QT2.6 · **Hyp:** H3 · **Class:** quantitative estimate · **Status:** supported
- **Claim:** By 1850, Mania-authorized new railways were 39.5% of the industry's total par (paid-in) value — a substantial minority of realized capital.
- **Evidence/quote:** "represented 39.5 per cent of the railway industry's par value in 1850."
- **Source/loc:** A2-Campbell-Deriving-2013, p.9 · **Period:** 1850 · **Geo:** GB (LSE) · **Unit:** % of total industry par value · **Conf:** medium-high
- **Counter/limits:** Established railways also >doubled par value; LSE-listed only.

### C-063
- **Branch:** QT2.7 · **Hyp:** H3 · **Class:** quantitative estimate · **Status:** supported
- **Claim:** Parliament-authorized new mileage rose 810 (1844) → 2,816 (1845) → peak 4,540 (1846), then collapsed 1,295 (1847), 373 (1848), 16 (1849), 7 (1850) — a ~2-orders-of-magnitude swing in six years.
- **Evidence/quote:** FRED series "Mileage of New Railway Lines Authorized by Parliament for Great Britain," annual, miles, NSA.
- **Source/loc:** A1-NBER-FRED-Mileage (A0284DGBA374NNBR + CSV, retrieved 2026-07-12) · **Period:** 1822–1852 · **Geo:** GB · **Unit:** miles authorized/yr (flow) · **Conf:** medium
- **Counter/limits:** Companion series A024DAGBA374NNBR (1847–79) differs slightly for overlap years (1847: 1,354 vs 1,295) due to different source (Lewin vs Parl. Papers); 1840 negative = net abandonments; possible Ireland inclusion in the 1847–79 variable.

### C-064
- **Branch:** QT2.2 · **Hyp:** H3 · **Class:** quantitative estimate · **Status:** contested
- **Claim:** A competing GDP-share estimate: Mitchell (1964, via Campbell) puts railway investment at 5.7% (1846), 6.7% (1847), 4.7% (1848) — below Odlyzko/Nash's ~8% for 1847; unreconciled.
- **Evidence/quote:** "Estimates by Mitchell (1964) suggest that railway investment represented 5.7 per cent of GDP in 1846, 6.7 per cent in 1847, and 4.7 per cent in 1848."
- **Source/loc:** A2-Campbell-Deriving-2013, p.8 · **Period:** 1846–1848 · **Geo:** GB · **Unit:** railway investment as % of GDP · **Conf:** medium
- **Counter/limits:** Odlyzko's ~8% (1847) is ~1.3 pp higher than Mitchell's 6.7%; denominators/definitions not disambiguated; Mitchell 1964 not directly read.

### C-065
- **Branch:** QT2.8 · **Hyp:** — · **Class:** historical fact · **Status:** supported
- **Claim:** Reported "paid-up capital" can include large "nominal additions" reflecting accounting conventions, not new investment — e.g. the Midland's 1897–8 conversions raised reported paid-up capital £100m→£168m with "less than £5 million representing actual investment."
- **Evidence/quote:** "with less than £5 million representing actual investment... The effect of this on the recorded rate of return would appear to suggest catastrophic misfortune... but this is actually quite illusory."
- **Source/loc:** B5-MitchellChambersCrafts-2011, p.6 · **Period:** 1897–8 example (general 1870–1912) · **Geo:** GB (Midland et al.) · **Unit:** £m reported vs actual · **Conf:** high
- **Counter/limits:** Post-Mania example; nominal additions not separately recorded before 1890, so Mania-era equivalents can't be quantified from this source.

### C-066
- **Branch:** QT2.8 · **Hyp:** — · **Class:** quantitative estimate · **Status:** supported
- **Claim:** For 15 major companies (~¾ of route miles), adjusted paid-up capital rose £400.5m (1870) → £866.4m (1912); cumulated capital expenditure £361.9m → £843.6m — a long-run capital-formation series, well after the Mania.
- **Evidence/quote:** Table 1 (data "extracted by Brian Mitchell in 1962/3... project... directed by Phyllis Deane"): 1870 £400,549k / £361,929k; 1912 £866,439k / £843,596k.
- **Source/loc:** B5-MitchellChambersCrafts-2011, p.29–30 (Table 1) · **Period:** 1870–1912 · **Geo:** GB (15 named companies) · **Unit:** £000 adjusted paid-up capital; cumulated capex · **Conf:** high
- **Counter/limits:** 1870–1912 only — does NOT fill the Mania-era capital-formation gap; excludes nominal additions.

### C-067
- **Branch:** QT2.9 · **Hyp:** H3 · **Class:** scholarly interpretation · **Status:** supported
- **Claim:** Nash and the LNWR's own statement gave incompatible authorized-capital figures for the same company (£40m vs "only" £30m, further capped to £26m) — contemporaries couldn't agree what "authorized" liability meant.
- **Evidence/quote:** "The most directly comparable figures in Nash's analysis and the LNWR 'financial statement' were £40 million in one, and £30 million in the other."
- **Source/loc:** A5-Odlyzko-Collapse-2011, p.32–33 · **Period:** 1848 · **Geo:** GB (LNWR) · **Unit:** £m company authorized/potential liability · **Conf:** medium
- **Counter/limits:** Odlyzko argues the two are "largely compatible... differing judgment"; single-company example.

### C-068
- **Branch:** QT2.3 · **Hyp:** H3 · **Class:** quantitative estimate · **Status:** partially-supported
- **Claim:** Pre-Mania business plans assumed construction costs of ~£15,600/mile (1845 session), rising to ~£21,000 (1846) and ~£25,000 (1847) — all below the £31,700–£35,200/mile actually realized (C-054).
- **Evidence/quote:** "expected construction cost of £15,600 per mile... for the 1846 session... approximately £21,000 per mile, and for the 1847 session they were about £25,000 per mile."
- **Source/loc:** A5-Odlyzko-Collapse-2011, p.8 · **Period:** 1845–1847 sessions · **Geo:** GB · **Unit:** £/mile planned construction cost · **Conf:** medium
- **Counter/limits:** 1846/47 figures from incomplete business-plan data (author-flagged).

### C-069
- **Branch:** QT2.10 · **Hyp:** H3 · **Class:** scholarly interpretation · **Status:** supported
- **Claim:** Price-boom and real-investment-boom timing were offset ~2 years: share prices peaked mid-1845 and slid 4 years to end-1849, while construction investment kept rising to its 1847 peak — real deployment grew well after the market signaled trouble.
- **Evidence/quote:** "peak prices reached in mid-1845. After that, railway shares went into a prolonged, 4-year slide... However, actual investments in railway construction moved in the opposite direction, rising... to a peak of £44 million in 1847."
- **Source/loc:** A5-Odlyzko-Collapse-2011, p.3 · **Period:** 1845–1850 · **Geo:** GB · **Unit:** qualitative timing (index vs £m flow) · **Conf:** medium-high
- **Counter/limits:** Interpretive synthesis of two series; lead-lag not formally tested. Directly relevant to H5 (timing) and H3 (overbuild).

---

## Section C3 — Railway prices and investor returns

Sources: `B2-CGT-BeforeCult-2019` (Campbell, Grossman & Turner, QUCEH WP19-01), `A2-Campbell-Deriving-2013` (Campbell sole), `A2-CampbellTurner-GreatestBubble-2010`, `B2-Acheson-RuleBritannia-2009`, `WP16-03-CampbellRogersTurner`. All indices are **London Stock Exchange** samples unless noted.

### C-100
- **Branch:** QT3.1 · **Hyp:** — · **Class:** quantitative estimate · **Status:** supported
- **Claim:** Before the Cult of Equity builds three capital-appreciation indices (all-share, UK/domestic, blue-chip-30) for 1829–1929 and decomposes monthly return into capital-gain + dividend-yield terms summing to total return.
- **Evidence/quote:** "We construct three indices of capital appreciation from 1829 to 1929: an all-share index; a UK-share index...; and a blue-chip index..." (Eq.1: R = (P_t−P_t-1)/P_t-1 + D_t/P_t-1).
- **Source/loc:** B2-CGT-BeforeCult-2019, §1 p.2–3 + §3 Eq.1 ~p.11 · **Period:** 1829–1929 · **Geo:** GB (London 1829–68; +provincial 1869–1929) · **Unit:** index construction, market-cap weighted · **Conf:** high
- **Counter/limits:** Weighting uses t-1 market cap (corrects an error in Acheson 2009 / Grossman 2017).

### C-101
- **Branch:** QT3.1 · **Hyp:** — · **Class:** historical fact · **Status:** supported
- **Claim:** The database is not London-only: 1829–68 (Course of the Exchange) is a London list, but 1869–1929 (Investor's Monthly Manual) covers London AND provincial exchanges. ~5,800 securities / ~4,500 companies.
- **Evidence/quote:** "The IMM... published a much more extensive list of securities which included securities listed on both the London and provincial stock exchanges."
- **Source/loc:** B2-CGT-BeforeCult-2019, §2 ~p.6 · **Period:** 1829–1929 · **Geo:** GB · **Unit:** data-source description · **Conf:** high
- **Counter/limits:** IMM coverage "extensive, but not exhaustive," time-varying (C-103).

### C-102
- **Branch:** QT3.1 · **Hyp:** — · **Class:** historical fact · **Status:** supported
- **Claim:** Before the Cult of Equity makes **no** delisting/survivorship adjustment — indices reflect only behaviour while a stock is in the source.
- **Evidence/quote:** "We make no attempt to examine the gains or losses from newly listing, delisting, or merging, which are major areas of research in their own right..."
- **Source/loc:** B2-CGT-BeforeCult-2019, §3 ~p.11 · **Period:** 1829–1929 · **Geo:** GB · **Unit:** methodological scope · **Conf:** high
- **Counter/limits:** Contrast Rule Britannia (C-131–C-134), which DOES adjust. First-order limitation for high-attrition periods (railways during/after the Mania). **Correction:** the survivorship machinery belongs to Rule Britannia, not this paper.

### C-103
- **Branch:** QT3.1 · **Hyp:** — · **Class:** historical fact · **Status:** supported
- **Claim:** The paper warns its post-1869 IMM data must NOT be read as London-only; many securities were listed on London/provincial/foreign exchanges — resolving that the main indices' post-1869 universe is a mixed London-and-provincial one.
- **Evidence/quote:** "Implying that the IMM data is representative of the London Stock Exchange (e.g., Grossman 2015) is incorrect." (Appendix 1, fn 31)
- **Source/loc:** B2-CGT-BeforeCult-2019, App. 1 fn 31 (~doc p.57) · **Period:** 1869–1929 · **Geo:** GB (London + provincial) · **Unit:** representativeness caveat · **Conf:** high
- **Counter/limits:** The exact provincial share of the index is never quantified (see closing flag C-141).

### C-104
- **Branch:** QT3.1 · **Hyp:** — · **Class:** research inference · **Status:** partially-supported
- **Claim:** For one auxiliary exercise (Figure 1 nominal-value benchmarking vs Michie's Official List) the authors restrict to securities "chiefly traded in London," excluding provincial-only — a narrower universe than the main return indices use.
- **Evidence/quote:** "we include all corporate securities which were reported by the IMM as being chiefly traded in London (i.e., excluding securities listed only on provincial markets)."
- **Source/loc:** B2-CGT-BeforeCult-2019, §2 ~p.7 · **Period:** 1869–1929 · **Geo:** London (this calc only) · **Unit:** nominal value of all corporate securities · **Conf:** medium
- **Counter/limits:** Restriction is local to Fig. 1, not restated for the return indices — inferred by contrast with fn 31.

### C-105
- **Branch:** QT3.2 · **Hyp:** — · **Class:** quantitative estimate · **Status:** supported
- **Claim:** The UK-share capital-gains (price-only) index fell 53% during 1845–1850 — the largest % decline in the 1829–2018 series — after the Mania collapse.
- **Evidence/quote:** "The largest percentage decline occurred during 1845-1850, following the collapse of the Railway Mania, when the index fell by 53 per cent."
- **Source/loc:** B2-CGT-BeforeCult-2019, §3 Fig.4 ~p.12 · **Period:** 1845–1850 · **Geo:** GB · **Unit:** capital-gains (price-only) index; NOT total return · **Conf:** high
- **Counter/limits:** All-UK index statistic, NOT railway-sector-specific nor total return (cf. railway decade total return +3.7%, C-109).

### C-106
- **Branch:** QT3.2 · **Hyp:** — · **Class:** quantitative estimate · **Status:** supported
- **Claim:** The UK-share price-only index rose 52% from 1842 to mid-1845 (Mania boom).
- **Evidence/quote:** "The most dramatic market advances took place from 1842 until mid-1845 during the Railway Mania (52 percent)…"
- **Source/loc:** B2-CGT-BeforeCult-2019, §3 ~p.12 · **Period:** 1842–mid-1845 · **Geo:** GB · **Unit:** price-only index · **Conf:** high · **Counter/limits:** Price-only; no delisting adjustment.

### C-107
- **Branch:** QT3.2 · **Hyp:** — · **Class:** quantitative estimate · **Status:** supported
- **Claim:** Over 1830–1929, average annual geometric total return was 5.4% (all equities), 5.3% (UK), 4.9% (blue-chip), with almost all coming from dividends not capital gains.
- **Evidence/quote:** "The total return for the 100-year period averaged 5.4 per cent per year for all equities... with almost all of this coming from dividends."
- **Source/loc:** B2-CGT-BeforeCult-2019, §5 Table 1 ~p.17 · **Period:** 1830–1929 · **Geo:** GB · **Unit:** geometric total return, market-cap weighted, nominal · **Conf:** high
- **Counter/limits:** No survivorship adjustment; period averages mask the 1845–50 crash; small/mid firms earned higher (5.8%/6.7%).

### C-108
- **Branch:** QT3.2 · **Hyp:** — · **Class:** quantitative estimate · **Status:** supported
- **Claim:** Consols returned ~2.8%/yr over 1830–1929, implying an equity premium of ~2.6 pp over long bonds (~1.9 pp over bills); ~0.4%/yr inflation → ~5.0% real equity return.
- **Evidence/quote:** "For Consols, including both coupon payments and price changes, the average return was about 2.8 per cent, implying an equity premium over long-term bonds of about 2.6 per cent."
- **Source/loc:** B2-CGT-BeforeCult-2019, §5 ~p.17–18 · **Period:** 1830–1929 · **Geo:** GB · **Unit:** Consols total return (coupon+price) · **Conf:** high
- **Counter/limits:** Premium "modest compared to recent experience." (This is the U1/U6 secondary benchmark.)

### C-109
- **Branch:** QT3.3 · **Hyp:** — · **Class:** quantitative estimate · **Status:** supported
- **Claim:** The railway sector's 1840–1849 decade averages were: capital gain −0.4%, dividend yield 4.0%, total return +3.7%/yr — a positive decade total return coexisting with the 53% peak-to-trough price crash (C-105), because dividends offset much of the price fall.
- **Evidence/quote:** Table 8 railways 1840–49: CapGain −0.4% / DivYield 4.0% / Return 3.7%. Note: "only calculated for an industry decade where more than five companies were listed continuously."
- **Source/loc:** B2-CGT-BeforeCult-2019, §6 Table 8 ~p.50–52 · **Period:** 1840–1849 · **Geo:** GB railways · **Unit:** annual geometric CG/DY/TR, market-cap weighted · **Conf:** medium
- **Counter/limits:** Decade-mean ≠ peak-to-trough; the ">5 continuously-listed" rule is itself a decade-level survival filter.

### C-110
- **Branch:** QT3.3 · **Hyp:** — · **Class:** quantitative estimate · **Status:** supported
- **Claim:** Railways had a CAPM beta of 1.267 vs the all-equities market (R²=0.700, N=1,156), one of five sectors with beta>1.
- **Evidence/quote:** Table 9: "Railways 1.267 0.028 1156 0.700."
- **Source/loc:** B2-CGT-BeforeCult-2019, §6 Table 9 ~p.53 · **Period:** 1830–1929 · **Geo:** GB railways · **Unit:** CAPM beta on total return · **Conf:** high
- **Counter/limits:** Full-100-yr beta; doesn't isolate 1843–50 Mania risk (likely higher).

### C-111
- **Branch:** QT3.1 · **Hyp:** — · **Class:** historical fact · **Status:** supported
- **Claim:** The domestic share of the "UK equities" universe fell from ~97% (early 1830s) to ~70% (1860s), <65% (1890s), ~50% (WWI) — so the UK-share and all-share indices are not interchangeable.
- **Evidence/quote:** "Domestic securities constituted nearly 97 per cent by the early 1830s... to about 70 per cent by the 1860s... just over 50 per cent during and after World War I."
- **Source/loc:** B2-CGT-BeforeCult-2019, §2 ~p.6 · **Period:** 1830s–1929 · **Geo:** GB vs foreign · **Unit:** % of securities that are domestic (by count) · **Conf:** high

### C-112
- **Branch:** QT3.4 · **Hyp:** — · **Class:** quantitative estimate · **Status:** supported
- **Claim:** Campbell's (2013) weekly par-adjusted "All Railway" price index (0%-loss-on-delisting scenario) peaked at 1,984 (Aug 1845), troughed at 673 — a 66.1% decline.
- **Evidence/quote:** "The first scenario shows the All Railway index peaking at 1,984, and reaching a trough at 673, which represents a 66.1 per cent decline."
- **Source/loc:** A2-Campbell-Deriving-2013, §II ~p.8 + Fig.1 · **Period:** Aug 1845 – ~1850 · **Geo:** GB (LSE) · **Unit:** par-adjusted price index; NOT total return · **Conf:** high
- **Counter/limits:** Greatest Bubble (daily) reports 2,017/672 (C-120) — directionally consistent, not identical; excludes provincial-only railways.

### C-113
- **Branch:** QT3.4 · **Hyp:** — · **Class:** quantitative estimate · **Status:** supported
- **Claim:** Under the 100%-loss-on-delisting scenario the same index peaked 1,935, troughed 583 (69.9% decline); the paper frames 0%-loss as the upper and 100%-loss as the lower bound of investor experience (winding-up usually returned a positive sum).
- **Evidence/quote:** "The second scenario shows a peak at 1,935 and a trough at 583, which represents a 69.9 per cent decline."
- **Source/loc:** A2-Campbell-Deriving-2013, §II ~p.8 · **Period:** 1843–1850 · **Geo:** LSE · **Unit:** price index delisting-sensitivity bound · **Conf:** high
- **Counter/limits:** Greatest Bubble's 3-way scenarios give a narrower band (C-120/C-121); "positive sum" based on a small reported sample.

### C-114
- **Branch:** QT3.5 · **Hyp:** — · **Class:** quantitative estimate · **Status:** supported
- **Claim:** 1843→Aug 1845: Established Railways rose 71.7%, All Railways 93.5–98.4% (delisting-dependent), vs Non-Railways +18.8% — established and new cohorts appreciated very differently.
- **Evidence/quote:** "The index of Established Railways rose by 71.7 per cent... All Railways... between 93.5 per cent and 98.4 per cent... Non-Railways index of just 18.8 per cent."
- **Source/loc:** A2-Campbell-Deriving-2013, §II ~p.6–7 · **Period:** 1843–Aug 1845 · **Geo:** LSE · **Unit:** price index · **Conf:** high
- **Counter/limits:** New-cohort figure already delisting-sensitive during run-up (some failing pre-peak).

### C-115
- **Branch:** QT3.5 · **Hyp:** — · **Class:** quantitative estimate · **Status:** supported
- **Claim:** Peak price/par ratio (leveraged return proxy) varied sharply by authorization cohort: 2.16 (1844), 4.36 (1845), 3.05 (1846), 1.09 (1847), 3.03 (never authorized) — dispersion tied to timing, not eventual success.
- **Evidence/quote:** "The peak price/par ratio of those railways authorised in 1844 was 2.16... 1845 was 4.36... 1846 was 3.05... 1847 was 1.09... not authorised was 3.03."
- **Source/loc:** A2-Campbell-Deriving-2013, §V ~p.17 · **Period:** 1844–1850 cohorts · **Geo:** LSE · **Unit:** price/par ratio (leveraged) · **Conf:** high
- **Counter/limits:** Pricing "had more to do with market expectations... than the authorisation status"; excludes preference/guaranteed stock.

### C-116
- **Branch:** QT3.5 · **Hyp:** — · **Class:** scholarly interpretation · **Status:** supported
- **Claim:** Stripping out partial-payment leverage, peak implied fully-paid price/par ratios collapse to near-parity (1.29/1.24/1.13/1.09/1.12 by cohort) — the dramatic headline gains were overwhelmingly a leverage artifact, not large fundamental mispricing.
- **Evidence/quote:** "due to the leveraged nature of the partially-paid shares the returns which they actually experienced were substantial."
- **Source/loc:** A2-Campbell-Deriving-2013, §V ~p.20 · **Period:** 1844–1850 · **Geo:** LSE · **Unit:** implied fully-paid price/par ratio (~3% discount rate) · **Conf:** high
- **Counter/limits:** Relies on assumed discount/dividend scenario (robustness-checked). **Central H5 (timing/leverage) evidence.**

### C-117
- **Branch:** QT3.5 · **Hyp:** — · **Class:** quantitative estimate · **Status:** supported
- **Claim:** Mean realized (partially-paid) returns by cohort: +57.5% (1844), +36.0% (1845), +21.8% (1846), −19.6% (1847), avg +33.7% — vs fully-paid-equivalent +16.6/+8.7/+6.6/−2.7%, avg +9.1%. Boom entrants captured leveraged gains; the 1847 cohort took a leveraged loss.
- **Evidence/quote:** "The mean return on companies authorised in 1844 was 57.5 per cent... 1847 was −19.6 per cent... if only fully-paid shares... 1844 was 16.6 per cent... 1847 was −2.7 per cent."
- **Source/loc:** A2-Campbell-Deriving-2013, §V Table 2 ~p.21 · **Period:** 1844–47 cohorts, subscription→first post-Assent call · **Geo:** LSE · **Unit:** % return, leveraged vs unleveraged · **Conf:** high
- **Counter/limits:** Method "tends to underestimate" leverage effects (measured from first call, post-peak for later cohorts); restricted to authorized companies. **Direct H5 evidence: timing dominated outcome within the same sector.**

### C-118
- **Branch:** QT3.5 · **Hyp:** — · **Class:** quantitative estimate · **Status:** supported
- **Claim:** Established railways >doubled aggregate par value 1843→1850, while Mania-era new railways reached 39.5% of the industry's par value by 1850.
- **Evidence/quote:** "more than doubling their par value between 1843 and 1850... represented 39.5 per cent of the railway industry's par value in 1850."
- **Source/loc:** A2-Campbell-Deriving-2013, §II ~p.9 · **Period:** 1843–1850 · **Geo:** LSE · **Unit:** aggregate par value · **Conf:** high · **Counter/limits:** Par value (capital committed), not investor wealth/return.

### C-119
- **Branch:** QT3.4 · **Hyp:** — · **Class:** historical fact · **Status:** supported
- **Claim:** Campbell's (2013) dataset = weekly Railway Times LSE ordinary railway shares 1843–1850, averaging 179.6 listed securities/week (peak 295 in 1846), excluding preference/guaranteed stock.
- **Evidence/quote:** "averaged 179.6 across the period, peaking at 295 in 1846."
- **Source/loc:** A2-Campbell-Deriving-2013, §III ~p.9–10 · **Period:** 1843–1850 · **Geo:** LSE · **Unit:** count of listed ordinary securities · **Conf:** high
- **Counter/limits:** London-only; "underestimates the extent of promotion... others chose to only list on regional exchanges."

### C-120
- **Branch:** QT3.6 · **Hyp:** — · **Class:** quantitative estimate · **Status:** supported
- **Claim:** Campbell & Turner's (2010) daily index (base 1,000 = Jan 1843) peaked 2,017 (9 Aug 1845), troughed 672 (16 Apr 1850) — a 66.7% peak-to-trough fall, but only 14.3% Jan1843→Dec1850; framing choice materially changes the "loss."
- **Evidence/quote:** "The index peaked at 2,017 on 9th August 1845... reaching a low of 672 on 16th April 1850. Overall, the index fell by 14.3 per cent between January 1843 and December 1850, and from peak to trough, prices fell by 66.7 per cent."
- **Source/loc:** A2-CampbellTurner-GreatestBubble-2010, ~p.11–12 · **Period:** Jan 1843–Dec 1850 · **Geo:** LSE · **Unit:** daily par-adjusted price index; NOT total return · **Conf:** high
- **Counter/limits:** Campbell 2013 weekly gives 1,984/673 (C-112); includes first-day returns of new listings (C-122).

### C-121
- **Branch:** QT3.6 · **Hyp:** — · **Class:** quantitative estimate · **Status:** supported
- **Claim:** Under 100%/50%/0%-of-market-price delisting scenarios, the index peaked (same day) 2,017/1,992/1,967 and ended 1850 at 857/793/733 — i.e. 57.5%/60.2%/62.7% below peak; delisting choice shifts the end-1850 fall by ~5 pp.
- **Evidence/quote:** "By the end of 1850, the indices stood at 857, 793, and 733 respectively. Under the various scenarios, prices ended 1850 at 57.5 per cent, 60.2 per cent, and 62.7 per cent below their peak level."
- **Source/loc:** A2-CampbellTurner-GreatestBubble-2010, ~p.13–15 · **Period:** 1843–1850 · **Geo:** LSE · **Unit:** price index delisting sensitivity · **Conf:** high
- **Counter/limits:** Applies to 155 unknown-outcome securities; 100 known-amalgamation delistings treated uniformly.

### C-122
- **Branch:** QT3.7 · **Hyp:** — · **Class:** scholarly interpretation · **Status:** supported
- **Claim:** New-listing first-day returns inflated the boom: peak 2,017 incl. vs 1,722 excl. first-day returns; an established-only index peaked separately at 1,670 — the bubble pattern persists even among established railways.
- **Evidence/quote:** "the new railways made a substantial contribution to the positive returns... most of this impact was derived from the first day they traded... although the new railways accentuated the bubble-like pattern, it is still there when we just consider the railways constructed prior to 1843."
- **Source/loc:** A2-CampbellTurner-GreatestBubble-2010, ~p.16–17 · **Period:** 1843–1850 · **Geo:** LSE · **Unit:** price index variants · **Conf:** high · **Counter/limits:** First-day return assumes par subscription (sample-limited).

### C-123
- **Branch:** QT3.7 · **Hyp:** — · **Class:** quantitative estimate · **Status:** supported
- **Claim:** Median price/par diverged by cohort: established 0.72(1843)→1.63(1845)→0.60(1849); new 1.22(1845)→0.54(1850); new-railway median paid-up rose 6.0%(1844–45)→92.4%(1850) as calls accumulated — direct evidence of the calls→deleveraging→price-decline mechanism.
- **Evidence/quote:** "The median new railway in 1845 was trading at a price/par ratio of 1.22... reaching 0.54 by the end of 1850... 6.0 per cent paid up in 1844 and 1845... 92.4 per cent in 1850."
- **Source/loc:** A2-CampbellTurner-GreatestBubble-2010, Table 2 ~p.15–16 · **Period:** 1843–1850 · **Geo:** LSE · **Unit:** median price/par; % paid-up by cohort-year · **Conf:** high · **Counter/limits:** Median (unweighted); "established" composition shifts via amalgamation.

### C-124
- **Branch:** QT3.6 · **Hyp:** — · **Class:** historical fact · **Status:** supported
- **Claim:** Greatest Bubble's dataset = weekly Railway Times LSE ordinary GB/Ireland railway equity: after excluding 88 non-ordinary, 84 foreign, 150 incomplete → 591 shares / 332 companies / 449,165 obs (108,444 daily price obs).
- **Evidence/quote:** "we were left with 591 ordinary shares belonging to 332 companies... 449,165 observations... only 108,444 daily price observations."
- **Source/loc:** A2-CampbellTurner-GreatestBubble-2010, ~p.8–9 · **Period:** 1843–1850 · **Geo:** LSE (GB/Ireland railways) · **Unit:** sample construction · **Conf:** high · **Counter/limits:** Excludes provincial-only-listed railways by construction.

### C-125
- **Branch:** QT3.6 · **Hyp:** — · **Class:** research inference · **Status:** partially-supported
- **Claim:** Greatest Bubble treats dividends only narratively (established railways cut dividends in the downturn), NOT in the index — confirming it is a price-only index and dividend cuts are a candidate cause of the fall, not a return component.
- **Evidence/quote:** "the rapid decline in the dividends paid by railway firms during the downturn suggests that changes in cash flows may have been influential in the price falls." (no dividend term in the index formula)
- **Source/loc:** A2-CampbellTurner-GreatestBubble-2010, ~p.22–24 + p.9 · **Period:** 1843–1850 · **Geo:** LSE · **Unit:** price-only index; dividends as narrative factor · **Conf:** medium
- **Counter/limits:** Realized investor total return was somewhat less negative than the price fall implies; offset magnitude unquantified.

### C-126
- **Branch:** QT3.8 · **Hyp:** — · **Class:** historical fact · **Status:** supported
- **Claim:** Rule Britannia builds monthly capital-appreciation, dividend-yield, and total-return indices for 1825–1870 (three weighting schemes) from the Course of the Exchange, explicitly restricted to the London market.
- **Evidence/quote:** "constructing monthly returns for stocks traded on the London market for the period 1825 to 1870... unweighted indices as well as indices weighted by paid-up capital and market capitalization."
- **Source/loc:** B2-Acheson-RuleBritannia-2009, p.1108–09 · **Period:** 1825–1870 · **Geo:** London only · **Unit:** CG + DY + TR, 3 weightings, monthly · **Conf:** high
- **Counter/limits:** Clearest explicit London-only statement — anchors any RB-based claim as strictly non-provincial.

### C-127
- **Branch:** QT3.8 · **Hyp:** — · **Class:** scholarly interpretation · **Status:** supported
- **Claim:** Rule Britannia critiques the three prior era indices (Gayer et al.; Hayek; Rousseaux) for excluding dividends, small survivorship-biased samples, and flawed weighting, and positions itself as correcting all three incl. explicit survivorship adjustment.
- **Evidence/quote:** "The three existing indices mainly include stocks which survived and were frequently quoted... causing a sample selection bias. We avoid such a bias by collecting all available stock-price data... our estimates are adjusted for survivorship bias."
- **Source/loc:** B2-Acheson-RuleBritannia-2009, p.1108–09 · **Period:** 1825–1870 · **Geo:** London · **Unit:** methodological positioning · **Conf:** high

### C-128
- **Branch:** QT3.8 · **Hyp:** — · **Class:** quantitative estimate · **Status:** supported
- **Claim:** Unadjusted (pre-survivorship) 1825–1870 total returns: arithmetic 9.28% (mkt-cap wtd), 7.40% (paid-up wtd), 10.16% (unweighted); geometric 8.94/6.93/9.70%.
- **Evidence/quote:** Table 4 Panel A "Total return": WPC 7.40/6.93; WMC 9.28/8.94; UN 10.16/9.70.
- **Source/loc:** B2-Acheson-RuleBritannia-2009, Table 4 p.1126 · **Period:** 1825–1870 · **Geo:** London · **Unit:** annual total return, pre-survivorship-adjustment · **Conf:** high
- **Counter/limits:** Falls to 4.62% under the most severe attrition (C-133) — unadjusted overstates realized return.

### C-129
- **Branch:** QT3.8 · **Hyp:** — · **Class:** quantitative estimate · **Status:** supported
- **Claim:** Rule Britannia provides a Consols + real-return comparison: mean 3% Consols yield 3.32%; mean inflation 0.03%; mkt-cap-wtd arithmetic real return 9.44% pre-1850, 10.49% post-1850 — so a Consols benchmark AND real decomposition are present (not a gap).
- **Evidence/quote:** "Yield on 3% consols 3.32... Inflation 0.03... nominal and real returns... pre-1850 period are 8.09 percent and 9.44 percent... post-1850 period are 10.83 percent (nominal) and 10.49 percent (real)."
- **Source/loc:** B2-Acheson-RuleBritannia-2009, Table 4 p.1126 + p.1127 · **Period:** 1825–1870 (split 1850) · **Geo:** London · **Unit:** Consols running yield; real return · **Conf:** high
- **Counter/limits:** "Yield on Consols" is a running yield, NOT a total return like C-108 — the two papers' Consols benchmarks are not directly comparable.

### C-130
- **Branch:** QT3.8 · **Hyp:** — · **Class:** quantitative estimate · **Status:** supported
- **Claim:** Railways dominated the RB sample but contributed only modestly at index level: mkt-cap-wtd total return 9.28% (incl.) vs 9.07% (excl. railways); railways paid lower dividends but slightly higher capital appreciation.
- **Evidence/quote:** "railways, the dominant sector in our sample, paid lower dividends than other industries, although the return railroad investors received through capital appreciation was slightly higher."
- **Source/loc:** B2-Acheson-RuleBritannia-2009, Table 4 Panels A&B p.1126 · **Period:** 1825–1870 · **Geo:** London · **Unit:** total return, incl/excl railways · **Conf:** high · **Counter/limits:** Coarse sector split; no established/new railway sub-split.

### C-131
- **Branch:** QT3.9 · **Hyp:** — · **Class:** historical fact · **Status:** supported
- **Claim:** Rule Britannia's survivorship correction = 3 attrition strategies × 2 bounds (lower: −100% at delisting, security stays [buy-and-hold]; upper: −100% and removed). **This machinery belongs to Rule Britannia, not Before the Cult of Equity (C-102).**
- **Evidence/quote:** "The lower bound adjustment viewed shareholders as suffering a –100 percent return at delisting... a buy-and-hold survivorship bias adjustment. The upper bound adjustment... with the stock disappearing from their portfolio at this date."
- **Source/loc:** B2-Acheson-RuleBritannia-2009, "Survivorship Bias" p.1129–30 · **Period:** 1825–1870 · **Geo:** London · **Unit:** methodology · **Conf:** high · **Counter/limits:** See C-134 (sub-12-month delistings omitted).

### C-132
- **Branch:** QT3.9 · **Hyp:** — · **Class:** historical fact · **Status:** supported
- **Claim:** Checking the Dec 1870 IMM, the authors found 77 firms that had left their London sample were still alive (many had moved to a regional exchange) and are NOT counted as attrition — direct evidence a London-only sample can mistake exchange-migration for failure.
- **Evidence/quote:** "There were 77 firms which had disappeared from our data set but nonetheless appeared in the December 1870 edition... many of these equities had simply moved their listing to a regional stock exchange. Consequently, these 77 companies are not counted as victims attrition."
- **Source/loc:** B2-Acheson-RuleBritannia-2009, p.1129–30 · **Period:** through Dec 1870 · **Geo:** London vs national IMM · **Unit:** attrition correction · **Conf:** high
- **Counter/limits:** IMM comprehensive only from mid-1860s — this check couldn't cover the 1840s Mania cohort.

### C-133
- **Branch:** QT3.9 · **Hyp:** — · **Class:** quantitative estimate · **Status:** supported
- **Claim:** Delisting treatment materially changes returns: mkt-cap-wtd total return falls from 9.28% (unadjusted) to 4.62%–7.34% by strategy/bound; even the most severe gives 4.62%/yr (index still +741% over 1825–1870).
- **Evidence/quote:** "the total return index grows 741 percent by 1870, with the annual rate of return being 4.62 percent." Table 6: unadjusted 9.28; strategy 1 lower bound 4.62.
- **Source/loc:** B2-Acheson-RuleBritannia-2009, Table 6 p.1131 · **Period:** 1825–1870 · **Geo:** London · **Unit:** returns by attrition strategy × bound · **Conf:** high
- **Counter/limits:** Attrition hits unweighted more → delisting firms were mostly small; weighting interacts with survivorship treatment.

### C-134
- **Branch:** QT3.9 · **Hyp:** — · **Class:** scholarly interpretation · **Status:** partially-supported
- **Claim:** The authors acknowledge their correction ignores losses from companies listed <12 months (esp. fraudulent Mania promotions) but argue this barely biases results because such firms were small and investors had paid only a small deposit.
- **Evidence/quote:** "it ignores the losses produced by companies (particularly fraudulent ones) that briefly entered but were listed for less than 12 months... investors in short-lived companies typically lost very little."
- **Source/loc:** B2-Acheson-RuleBritannia-2009, p.1130 · **Period:** 1825–1870 (esp. 1840s Mania) · **Geo:** London · **Unit:** qualitative limitation · **Conf:** medium
- **Counter/limits:** Campbell's Mania papers (C-113, C-117 1847 cohort −19.6%) show losses were NOT confined to sub-12-month promotions — RB may understate Mania risk; magnitude unquantified.

### C-135
- **Branch:** QT3.8 · **Hyp:** — · **Class:** scholarly interpretation · **Status:** supported
- **Claim:** RB's indices don't reproduce Gayer et al.'s sharp 1836 railway-mania cycle because railways were only 17% of RB's weighted index vs 44% of Gayer's in 1836/37 — sample composition determines whether a "mania" shows up.
- **Evidence/quote:** "railways only constitute 17 percent of our weighted indices... whereas they constitute 44 percent of Gayer et al.'s."
- **Source/loc:** B2-Acheson-RuleBritannia-2009, p.1121–22 · **Period:** 1836–1841 · **Geo:** London · **Unit:** sector weight across index constructions · **Conf:** high
- **Counter/limits:** For 1841–49 (the 1840s Mania proper) RB and Gayer converge — this concern is much milder for this ledger's focal period.

### C-136
- **Branch:** QT3.10 · **Hyp:** — · **Class:** historical fact · **Status:** supported
- **Claim:** Campbell, Rogers & Turner classify every IMM security (1869–1929) by "chiefly traded" into London Only / London and Provincial / Multiple Provincial / Single Provincial — the apparatus for assessing how "London-only" an index is.
- **Evidence/quote:** "'London Only'... only on the London Stock Exchange. 'London and Provincial'... both... 'Multiple Provincial'... multiple regional exchanges, but not... London. 'Single Provincial'... only one regional exchange."
- **Source/loc:** WP16-03-CampbellRogersTurner, §3 ~p.9–10 · **Period:** 1869–1929 · **Geo:** GB+Ireland · **Unit:** listing-strategy classification · **Conf:** high
- **Counter/limits:** IMM "may not have reported every market"; thin provincial listings undercount → results "understate the number of firms."

### C-137
- **Branch:** QT3.10 · **Hyp:** — · **Class:** quantitative estimate · **Status:** partially-supported
- **Claim:** In 1870 (earliest year; ~a generation after the Mania), 85% of London-and-provincial cross-listed securities and 61% of multiple-provincial (non-London) securities were railways — directional (not contemporaneous) evidence that Mania-era listings skewed provincial/cross-listed.
- **Evidence/quote:** "85 per cent of securities in 1870 which were chiefly traded on both London and provincial markets were railway securities. Also, 61 per cent... on multiple provincial exchanges (but not London) were railways."
- **Source/loc:** WP16-03-CampbellRogersTurner, §4 Table 3 ~p.12 · **Period:** 1870 · **Geo:** GB+Ireland · **Unit:** % of securities that are railways, by category · **Conf:** medium
- **Counter/limits:** 1870, not 1843–50; railway/provincial concentration declined over time (C-141) → don't extrapolate backward.

### C-138
- **Branch:** QT3.10 · **Hyp:** — · **Class:** quantitative estimate · **Status:** supported
- **Claim:** For 1869–1929, average monthly total returns were statistically indistinguishable between London (0.38%) and provincial (0.35%) exchanges (diff 0.03 pp, p=0.59) — for this later period a London-only sample wouldn't materially bias the aggregate return level (though it can bias composition, C-137).
- **Evidence/quote:** Table 6: "London Stock Exchange 0.38%... Provincial stock exchanges 0.35%... Difference 0.03% (p value of 0.59)."
- **Source/loc:** WP16-03-CampbellRogersTurner, §5 Table 6 ~p.15 · **Period:** 1869–1929 · **Geo:** London vs provincial · **Unit:** avg monthly total return · **Conf:** high
- **Counter/limits:** NOT the 1843–50 Mania; pools all sectors; London had higher SD (1.00 vs 0.80).

### C-139
- **Branch:** QT3.10 · **Hyp:** — · **Class:** scholarly interpretation · **Status:** supported
- **Claim:** Provincial and London returns correlated highly 1869–1929 (adj R²=0.80 incl. cross-listed, 0.59 excl.) — a reasonably integrated national market that tempers, without eliminating, the London-only concern.
- **Evidence/quote:** Table 7: "Provincial markets 0.80*** / 0.59***"; "London & Provincial 0.74***."
- **Source/loc:** WP16-03-CampbellRogersTurner, §5 Table 7 ~p.16 · **Period:** 1869–1929 · **Geo:** London vs provincial · **Unit:** adj R² on London returns · **Conf:** high
- **Counter/limits:** Correlation drops to 0.59 excluding cross-listed; individual exchanges vary widely (Manchester 0.75 vs Cardiff 0.19); correlation ≠ equal crash magnitude for a specific episode.

### C-140
- **Branch:** QT3.10 · **Hyp:** — · **Class:** historical fact · **Status:** supported
- **Claim:** Provincial exchanges were founded in response to railway booms: Liverpool & Manchester in 1836 (first promotion boom), more in the 1840s boom; railway (and bank) shares were "the main forms of securities traded on the provincial stock exchanges in their early decades."
- **Evidence/quote:** "In 1836, stock exchanges were established in Liverpool and Manchester during the first railway promotion boom... railway shares... were the main forms of securities traded on the provincial stock exchanges in their early decades."
- **Source/loc:** WP16-03-CampbellRogersTurner, §2 ~p.4–5 · **Period:** 1830s–1840s · **Geo:** GB provincial exchanges · **Unit:** institutional narrative · **Conf:** high
- **Counter/limits:** Establishes WHY provincial representation is a first-order Mania-era concern, but doesn't quantify the 1843–50 magnitude.

### C-141
- **Branch:** QT3.10 · **Hyp:** — · **Class:** research inference · **Status:** gap
- **Claim:** The railway/bank share of provincial listings declined over time via consolidation; the earliest usable cross-section is 1870, so the 1843–50-specific magnitude of provincial railway listing is NOT quantified in any available source.
- **Evidence/quote:** "both the banking and railway industries underwent consolidation... national giants being created" + data only "for the period between 1869 and 1929."
- **Source/loc:** WP16-03-CampbellRogersTurner, §3–4 ~p.9, ~p.12 · **Period:** data from 1870; Mania out of scope · **Geo:** GB+Ireland · **Unit:** gap-flag · **Conf:** high (as a gap identification)
- **Counter/limits:** The clearest statement of the carried Stage B provincial-magnitude gap.

### C-142
- **Branch:** QT3.11 · **Hyp:** — · **Class:** research inference · **Status:** partially-supported
- **Claim:** The two Campbell railway indices are broadly but not exactly consistent: 2013 (weekly) 1,984→673 (66.1%) / 1,935→583 (69.9%); 2010 (daily) 2,017→672 (66.7%) with 60.2%/62.7% variants. Both agree on Aug-1845 peak, ~Apr-1850 trough, ~66–70% fall; exact levels differ by frequency/sample.
- **Evidence/quote:** Cross-reference of C-112/C-113 vs C-120/C-121.
- **Source/loc:** A2-Campbell-Deriving-2013 §II; A2-CampbellTurner-GreatestBubble-2010 · **Period:** 1843–1850 · **Geo:** LSE · **Unit:** price index, weekly vs daily · **Conf:** medium
- **Counter/limits:** A claim citing "the" Mania peak/trough must specify which paper; my cross-comparison, not the authors'.

### C-143
- **Branch:** QT3.2 · **Hyp:** — · **Class:** quantitative estimate · **Status:** supported
- **Claim:** Before the Cult of Equity reports 1830–1929 average inflation "just under 0.4% per year," implying ~5.0% real total return (vs 5.4% nominal all-equities) — a second real-return anchor distinct from Rule Britannia's.
- **Evidence/quote:** "Inflation during this period averaged just under 0.4 per cent per year, so real returns would have been about 5.0 per cent."
- **Source/loc:** B2-CGT-BeforeCult-2019, §5 ~p.17 · **Period:** 1830–1929 · **Geo:** GB · **Unit:** real total return (Clark deflator) · **Conf:** high
- **Counter/limits:** 100-yr average masks sub-period swings (cf. RB's pre/post-1850 split, C-129).

**C3 closing flags:** (a) Consols/real-return comparison is **present, not a gap** (C-108, C-129, C-143) — but the two papers' Consols measures (total return vs running yield) are not interchangeable. (b) Provincial-underrepresentation magnitude for **1843–50 is an unquantified carried gap** (C-141). (c) "Before the Cult of Equity" main index: pre-1869 (COE) is London-only by source construction; post-1869 (IMM) is a mixed London+provincial universe (C-103) whose exact provincial share is undetermined — the inclusion question is resolved (mixed), the magnitude is `undecidable`.

---

## Section C4 — Cash-flow-aware reconstruction (York and North Midland Railway)

Sources: `A4-Tuck-1845`, `A4-Tuck-1847`, `A4-Tuck-1848` (newly located 9th ed., archive.org `railwaysharehol01tuckgoog`), `B1-CampbellTurner-Dispelling-2012`, `A5-Odlyzko-Collapse-2011`. **Outcome: reconstruction is `undecidable` (C-166) — no dated call schedule exists; nothing was fabricated.** Several figures rest on OCR-scrambled tables and are flagged `partially-supported`/low confidence.

### C-150
- **Branch:** QT3.4 · **Hyp:** H2 · **Class:** historical fact · **Status:** supported
- **Claim:** YNM paid-up capital by class (Tuck 1845, ~mid-1845): 6,700 Whole Shares (£50/£50 paid); 6,700 Half Shares (£25/£25); 10,400 Scarborough Branch (£25/£20); 10,400 Selby Scrip (£50/£20).
- **Evidence/quote:** "6,700 Shares, 50l. each ; 50l. Paid. Whole Shares... 10,400 Shares, 50l. each ; 20l. Paid. Selby Scrip."
- **Source/loc:** A4-Tuck-1845, lines 3295–3300 (p. ~37) · **Period:** ~mid-1845 · **Geo:** GB · **Unit:** £ nominal vs £ paid per share, by class · **Conf:** high · **Counter/limits:** Publication snapshot; class totals don't reconcile with the printed authorized total (C-151).

### C-151
- **Branch:** QT3.4 · **Hyp:** — · **Class:** quantitative estimate · **Status:** contested
- **Claim:** Tuck 1845 prints YNM "Total sum authorised to be raised by Shares" as £1,062,500, not reconciling with the four share-class nominal totals (£1,282,500 by multiplication).
- **Evidence/quote:** "Total sum authorised to be raised by Shares 1,062,500l."
- **Source/loc:** A4-Tuck-1845, line 3300 · **Period:** ~mid-1845 · **Geo:** GB · **Unit:** £ authorized vs issued · **Conf:** low · **Counter/limits:** 1847/1848 eds. print a clean £4,721,250; surrounding table OCR-scrambled — digit errors can't be ruled out.

### C-152
- **Branch:** QT3.4 · **Hyp:** H2 · **Class:** historical fact · **Status:** supported
- **Claim:** YNM last half-yearly dividend (Tuck 1845): £2 10s/share = 10% p.a.
- **Evidence/quote:** "Last half-yearly dividend, per share, 2l. 10s. ; (per cent., per annum, 10l.)"
- **Source/loc:** A4-Tuck-1845, lines 3310–12 · **Period:** ~early-mid 1845 · **Geo:** GB · **Unit:** £/share/half-year; annualized % · **Conf:** high · **Counter/limits:** No exact declaration/payment date.

### C-153
- **Branch:** QT3.4 · **Hyp:** H2 · **Class:** research inference · **Status:** partially-supported
- **Claim:** Reconstructing the OCR-scrambled table: YNM H1-1845 total earnings ≈£77,791, cost of working ≈£28,484, total expended to June 1845 ≈£1,279,950 → implied operating ratio ≈36.6%.
- **Evidence/quote:** Labels "Total earnings for the six months, ending June 5, 1845..." / "Cost of working..." followed by "77,791; / 28,484l." matched by position.
- **Source/loc:** A4-Tuck-1845, lines 3300–3320 · **Period:** H1 ending ~5 Jun 1845 · **Geo:** GB · **Unit:** £; ratio = cost/revenue · **Conf:** low-medium · **Counter/limits:** Plausibility-based label-matching from scrambled OCR, NOT a direct transcription — must carry this caveat if cited.

### C-154
- **Branch:** QT3.4 · **Hyp:** H2 · **Class:** quantitative estimate · **Status:** partially-supported
- **Claim:** Tuck 1845 uniquely has a semi-annual YNM price/premium table for Jan/Jul 1839–1845, but column structure is OCR-scrambled so cell-level values can't be attributed to dates; only a qualitative rise (low-20s in 1839 → ~90–120 in 1843–44, partial pull-back by Jan 1845) is discernible.
- **Evidence/quote:** "Shewing the Price of York and North Midland Railway Shares, with the Premium or Discount thereon, on the 1st January and 1st July in each of the following Years."
- **Source/loc:** A4-Tuck-1845, lines 3328–3491 · **Period:** Jan 1839–Jul 1845 · **Geo:** GB · **Unit:** £ price/premium per share, semi-annual · **Conf:** low · **Counter/limits:** Only edition with this table; cell values unrecoverable from the text layer.

### C-155
- **Branch:** QT3.4 · **Hyp:** H2 · **Class:** historical fact · **Status:** partially-supported
- **Claim:** Tuck 1847 lists eight YNM share classes; total share capital £4,721,250. (One cell — 17,400 Scarborough shares — is arithmetically inconsistent with its own £260,000 subtotal implying 10,400, matching 1845/1848; likely OCR error.)
- **Evidence/quote:** "6,700 Shares, 50Z. each ; 50Z. paid ; Original Shares .... £335,000 ... Total Amount of Share Capital £4,721,250"
- **Source/loc:** A4-Tuck-1847, lines 6760–77 (p.111) · **Period:** 1847 · **Geo:** GB · **Unit:** £ nominal/paid by class · **Conf:** medium · **Counter/limits:** One OCR-corrupted share count.

### C-156
- **Branch:** QT3.4 · **Hyp:** H2 · **Class:** historical fact · **Status:** supported
- **Claim:** Tuck 1847 gives YNM "Amount raised by calls on shares to 30th June, 1846" = £1,397,022 10s — a cumulative total, NOT a dated call schedule.
- **Evidence/quote:** "Amount raised by calls on shares to 30th June, 1846.. 1,397,022 10"
- **Source/loc:** A4-Tuck-1847, line 6785 (p.111) · **Period:** cumulative to 30 Jun 1846 · **Geo:** GB · **Unit:** £ cumulative called/received · **Conf:** high · **Counter/limits:** The exact figure Stage B flagged; cannot support a money-weighted return (needs per-call timing).

### C-157
- **Branch:** QT3.4 · **Hyp:** H2 · **Class:** historical fact · **Status:** supported
- **Claim:** Tuck 1847: YNM debentures/loans £376,040 to 30 Jun 1846; total received £1,772,062 10s; total expended £1,957,979 8s.
- **Evidence/quote:** "on debentures or loan notes to ditio 376,040 / Total actually received to ditto 1,772,062 10 / Ditto expended to June, 1846 1,957,979 8"
- **Source/loc:** A4-Tuck-1847, lines 6787–91 (p.111) · **Period:** cumulative to 30 Jun 1846 · **Geo:** GB · **Unit:** £ cumulative receipts (shares+debt), capex · **Conf:** high · **Counter/limits:** Cumulative only.

### C-158
- **Branch:** QT3.4 · **Hyp:** H2 · **Class:** historical fact · **Status:** supported
- **Claim:** YNM last half-yearly dividend (Tuck 1847): £2 10s/share (10% p.a.) — identical to 1845.
- **Evidence/quote:** "Last half-yearly dividend, per share, 2l. 10s. / Per cent, per annum, 10l."
- **Source/loc:** A4-Tuck-1847, lines 6804–05 (p.111) · **Period:** H1 ending 30 Jun 1846 · **Geo:** GB · **Unit:** £/share/half-year · **Conf:** high

### C-159
- **Branch:** QT3.4 · **Hyp:** — · **Class:** research inference · **Status:** gap
- **Claim:** YNM total-earnings/cost figures for H1 ending 30 Jun 1846 are OCR-illegible in the 1847 edition (balance-from-last-half £18,281 3s 4d is legible).
- **Source/loc:** A4-Tuck-1847, lines 6795–6802 (p.111) · **Period:** H1 ending 30 Jun 1846 · **Geo:** GB · **Unit:** £ (unrecoverable) · **Conf:** N/A · **Counter/limits:** Genuine OCR failure; needs page-image re-scan.

### C-160
- **Branch:** QT3.4 · **Hyp:** H2 · **Class:** historical fact · **Status:** supported (authorization-date table, NOT call dates)
- **Claim:** A previously-unlocated Tuck 9th ed. (1848) contains a dated table "ACTS EMPOWERING THE YORK AND NORTH MIDLAND RAILWAY COMPANY TO RAISE CAPITAL" listing each Act 3 Jun 1836 → 27 Jul 1846 with date, object, capital & loan ceilings.
- **Evidence/quote:** "3 June, 1836 / Act of Incorporation / £370,000 / 183,333 ... 27 July, 1846 / ... 2,000,000 / nil."
- **Source/loc:** A4-Tuck-1848, lines 6666–6820 (pp.175–76) · **Period:** 1836–1847 · **Geo:** GB · **Unit:** £ Parliamentary capital/loan authorization ceilings, by dated Act · **Conf:** medium-high
- **Counter/limits:** **Critical: these are authorization dates, NOT dates the company called cash from shareholders.** Must not be treated as call dates. Some £ cells OCR-garbled.

### C-161
- **Branch:** QT3.4 · **Hyp:** H2 · **Class:** historical fact · **Status:** supported
- **Claim:** Tuck 1848 has a "Statement... Upon the Consolidation of the Shares into Stock, August, 1847" showing East & West Riding at £15 paid (of £25) and Hull & Selby purchase shares at £5 paid (of £25).
- **Evidence/quote:** "STATEMENT Of the Shares Account, Upon the Consolidation... August, 1847... 50,000 ... 25l. each ; 15l. paid ; East and West Biding [Riding]"
- **Source/loc:** A4-Tuck-1848, lines 6828–50 (p.176) · **Period:** Aug 1847 · **Geo:** GB · **Unit:** £ paid-up per share by class, at a named date · **Conf:** high · **Counter/limits:** Single snapshot; no intra-period call dates.

### C-162
- **Branch:** QT3.4 · **Hyp:** H2 · **Class:** research inference · **Status:** undecidable (date); partially-supported (amount)
- **Claim:** LABELLED PARTIAL/INFERRED: comparing the Aug-1847 consolidation snapshot (C-161) with the same edition's Capital Account (East & West Riding now £20 paid, Hull & Selby now £10) brackets a ~£5/share call to sometime Aug–Dec 1847 — NOT an exact date, and NOT a substitute for a dated call schedule.
- **Evidence/quote:** "50,000 Shares of 25l. each ; 20l. paid. East & West Riding... 62,950 Shares of 25l. each ; 10l. pd. Hull & Selby purchase... Amount received to 30th June, 1847 £2,891,654 5 6"
- **Source/loc:** A4-Tuck-1848, lines 6852–66 (p.176) · **Period:** bracketed Aug–Dec 1847 · **Geo:** GB · **Unit:** £/share paid-up increment, inferred window · **Conf:** low-medium (timing); medium (amount)
- **Counter/limits:** The "received to 30 Jun 1847" figure predates the Aug-1847 snapshot showing LOWER paid-up — an internal sequencing anomaly showing cross-snapshot inference is fragile even here.

### C-163
- **Branch:** QT3.4 · **Hyp:** H2 · **Class:** historical fact · **Status:** supported
- **Claim:** YNM last half-yearly dividend (Tuck 1848): £2 10s/share (10% p.a.) — unchanged across 1845, 1847, 1848 editions.
- **Evidence/quote:** "Last half-yearly dividend, per share, 2l. 10s. / Per cent, per annum, 10l."
- **Source/loc:** A4-Tuck-1848, lines 6880–81 (p.177) · **Period:** H1 ending 30 Jun 1847 · **Geo:** GB · **Unit:** £/share/half-year · **Conf:** high

### C-164
- **Branch:** QT3.4 · **Hyp:** — · **Class:** research inference · **Status:** partially-supported
- **Claim:** For H1 ending 30 Jun 1847, Tuck 1848 gives legible cost of working (£61,189 11s) and balance-from-last-half (£15,615 10s 4d), but total earnings is OCR-illegible → no verified operating ratio for this half-year.
- **Evidence/quote:** "Cost of working for the same period including rent\ 61 189 11 0 of Hull and Selby"
- **Source/loc:** A4-Tuck-1848, lines 6868–78 (p.177) · **Period:** H1 ending 30 Jun 1847 · **Geo:** GB · **Unit:** £ cost (legible); revenue (illegible) · **Conf:** high (cost only)

### C-165
- **Branch:** QT3.4 · **Hyp:** — · **Class:** scholarly interpretation · **Status:** supported (general context; not YNM-specific)
- **Claim:** 1840s railway allotment required only a 10% deposit, with subsequent calls made by the board "from time to time" and not systematically tabulated by compilers like Tuck — structurally why dated call schedules are hard to source.
- **Evidence/quote:** "they had to pay the 10 per cent deposit... The original allottees were liable for all future calls should the company be successfully incorporated..."
- **Source/loc:** B1-CampbellTurner-Dispelling-2012, lines 144–164 · **Period:** 1845/46 mechanics · **Geo:** GB · **Unit:** % deposit; qualitative · **Conf:** medium · **Counter/limits:** Describes NEW-company Mania subscription; YNM was incorporated 1836, so context not a YNM data point.

### C-166 — MASTER DECISION
- **Branch:** QT3.4 · **Hyp:** H2 · **Class:** research inference · **Status:** undecidable
- **Claim:** A full dated money-weighted investor cash-flow reconstruction for a representative YNM shareholder **cannot be built from available sources** and is marked **undecidable**. Tuck's editions give only cumulative paid-up/calls-received totals at isolated dates, dividend-per-share at those dates, and an authorization-date table (explicitly not call dates). No board call notice/due dates or per-call amounts were located.
- **Evidence/quote:** Synthesis of C-150–C-165.
- **Source/loc:** A4-Tuck-1845/1847/1848 (aggregate) · **Period:** 1836–1847 available window · **Geo:** GB · **Unit:** feasibility determination · **Conf:** high (in the negative determination)
- **Counter/limits / reasoning:** (1) Missing = dated calls (the load-bearing input for a money-weighted return). (2) Available = cumulative totals + dividends + authorization dates. (3) Inferring calls from paid-up changes is a labelled partial approximation only (C-162), bounding to months, and even that has an internal inconsistency. (4) **No IRR/money-weighted number is produced — doing so would require fabricating call dates, which the decision rule forbids.** (5) Alternative substrate flagged (Mitchell/Chambers/Crafts's 15-company PRO archive, e.g. Taff Vale) but NOT switched, per instructions. (6) archive.org has only 3 Tuck eds. (1845/1847/1848); no 1846/1849/1850 there — the Stage B gap is **bounded, not closed** (may exist in HathiTrust / physical libraries).

---

## Section C5 — Operating profit vs shareholder return

Sources: `A4-Tuck-1845/1847/1848`, `B5-MitchellChambersCrafts-2011`, `B5-CampbellTurner-ManagerialFailure-2015` (**re-keyed** — see C-197), `A5-Odlyzko-Collapse-2011`. Hard rule applied throughout: **reported dividend alone is never treated as proof of economic profitability.**

### C-180 to C-184 (YNM operating figures — OCR-reconstructed, low confidence)
- **C-180** (QT4.4·H2·research inference·partially-supported): YNM H1-1845 total revenue ≈£77,791 (reconstructed, see C-153). A4-Tuck-1845 lines 3306–18.
- **C-181** (QT4.4·H2·research inference·partially-supported): YNM H1-1845 operating cost ≈£28,484 (reconstructed). A4-Tuck-1845 lines 3308–19.
- **C-182** (QT4.4·H2·research inference·partially-supported): Implied YNM H1-1845 operating ratio ≈36.6% (28,484/77,791). Derived; low confidence — fully dependent on the OCR reconstruction (C-153).
- **C-183** (QT4.4·H2·research inference·partially-supported): Implied YNM H1-1845 net revenue ≈£49,307 (77,791−28,484). Derived; low confidence.
- **C-184** (QT4.4·research inference·gap): For H1 ending 30 Jun 1847, YNM cost of working £61,189 11s is legible but total earnings OCR-illegible → no operating ratio computable. A4-Tuck-1848 lines 6868–78.

### C-185
- **Branch:** QT4.4 · **Hyp:** — · **Class:** scholarly interpretation · **Status:** supported
- **Claim:** Mitchell/Chambers/Crafts define railway ROCE as net traffic revenue (from Railway Returns / half-yearly accounts) ÷ paid-up capital (equity+debentures, excluding nominal additions).
- **Evidence/quote:** "the return on capital employed (ROCE)... 'net traffic revenue'... The two together constituted paid-up capital... exclusive of nominal additions or deductions..."
- **Source/loc:** B5-MitchellChambersCrafts-2011, lines 246–267, 332–34 · **Period:** applied 1870–1912 · **Geo:** GB · **Unit:** ROCE = net traffic revenue ÷ adjusted paid-up capital · **Conf:** high
- **Counter/limits:** Differs from Arnold & McCartney (who didn't adjust for nominal additions — C-189); net traffic revenue excludes head-office/finance items.

### C-186
- **Branch:** QT4.4 · **Hyp:** — · **Class:** historical fact · **Status:** supported
- **Claim:** ROCE is built for 15 major companies (~¾ of route mileage): CR, GER, GNR, GWR, LYR, LNWR, LSWR, LBSCR, LCDR, MSLR/GCR, MR, NBR, NER, SER, TVR.
- **Evidence/quote:** "These railways comprise about three quarters of the route miles in operation at the end of the period."
- **Source/loc:** B5-MitchellChambersCrafts-2011, lines 1470–77 (Table 1 notes) · **Period:** 1870–1912 · **Geo:** GB · **Unit:** company sample · **Conf:** high · **Counter/limits:** Skewed to largest/best-documented.

### C-187
- **Branch:** QT4.4 · **Hyp:** H2 · **Class:** quantitative estimate · **Status:** supported
- **Claim:** 15-company 5-yr-MA ROCE fell 5.11% (1872) → 4.29% (1893) → 4.46% (1910) on paid-up-capital basis; 5.63% (1872) → 4.51% (1903) → 4.62% (1910) on capex basis.
- **Evidence/quote:** "the 5-year moving average of ROCE fell from 5.11 per cent in 1872 to a low of 4.29 per cent in 1893 but had recovered to 4.46 per cent in 1910..."
- **Source/loc:** B5-MitchellChambersCrafts-2011, lines 454–59 + Table 1 · **Period:** 1870–1912 · **Geo:** GB · **Unit:** ROCE %, two capital bases · **Conf:** high
- **Counter/limits:** **Entirely AFTER the Mania — must not be conflated with 1840s figures.** ROCE is a total-capital (debt+equity) return, not pure equity.

### C-188
- **Branch:** QT4.4 · **Hyp:** — · **Class:** scholarly interpretation · **Status:** supported
- **Claim:** British railways of this era used no separate depreciation charge; maintenance/renewal via the revenue account substituted for it, on the assumption of indefinite asset life.
- **Evidence/quote:** "railway assets, or at any rate the majority of them, had an indefinite life."
- **Source/loc:** B5-MitchellChambersCrafts-2011, lines 400–403 · **Period:** 19th-c. convention · **Geo:** GB · **Unit:** accounting convention · **Conf:** high
- **Counter/limits:** Makes any reported "net revenue"/"profit" (incl. the YNM figures) non-comparable to a modern depreciation-adjusted profit.

### C-189
- **Branch:** QT4.4 · **Hyp:** — · **Class:** scholarly interpretation · **Status:** contested
- **Claim:** Failing to exclude "nominal additions" to paid-up capital exaggerates the apparent ROCE decline; MCC's adjusted estimates decline "considerably less" than Arnold & McCartney's unadjusted figures.
- **Evidence/quote:** "The ROCE estimates in Table 1 decline by considerably less than those recently reported by Arnold and McCartney who appear not to have adjusted for nominal additions..."
- **Source/loc:** B5-MitchellChambersCrafts-2011, lines 310–316, 447–52 · **Period:** 1870–1912 · **Geo:** GB · **Unit:** method dispute · **Conf:** high
- **Counter/limits:** An explicit scholarly disagreement (MCC vs Arnold & McCartney), not settled fact. Same caution applies to reading YNM's raw paid-up-capital figures.

### C-190
- **Branch:** QT4.4 · **Hyp:** H2 · **Class:** historical fact · **Status:** supported
- **Claim:** YNM's reported half-yearly dividend held flat at £2 10s/share (10% p.a.) across three editions (mid-1845, H1-1846, H1-1847).
- **Evidence/quote:** Synthesis of C-152/C-158/C-163.
- **Source/loc:** A4-Tuck-1845/1847/1848 · **Period:** mid-1845 – H1-1847 · **Geo:** GB · **Unit:** £/share/half-year · **Conf:** high
- **Counter/limits:** A flat 10% dividend during rapid capital expansion is exactly the pattern contemporaries/scholars flagged as symptomatic of dividend-smoothing via capital-account manipulation (C-192/C-193). States only the reported fact.

### C-191
- **Branch:** QT4.4 · **Hyp:** H2 · **Class:** scholarly interpretation · **Status:** partially-supported
- **Claim:** Arnold & McCartney estimate YNM's 1850 return on equity was 10.1% for the pre-Mania network vs −0.3% for the Mania-era-constructed part.
- **Evidence/quote:** "Arnold and McCartney estimate that in 1850, the return on equity of the York and North Midland's pre-Mania network was 10.1 per cent, whereas the return on the Mania part of its network -0.3 per cent." (cited in fn 45)
- **Source/loc:** B5-CampbellTurner-ManagerialFailure-2015, lines 469–71, fn 45 line 864 · **Period:** 1850 · **Geo:** GB (YNM) · **Unit:** ROE %, by network vintage · **Conf:** medium
- **Counter/limits:** **Secondary citation** to McCartney & Arnold (2001), primary NOT read (C-194); 1850 dating doesn't align exactly with the 1845–47 Tuck dividend data.

### C-192 — HARD-RULE SYNTHESIS
- **Branch:** QT4.4 · **Hyp:** H2 · **Class:** research inference · **Status:** partially-supported
- **Claim:** YNM's flat 10% reported dividend (C-190) must NOT be read as proof of profitability: the only located segment-level ROE estimate (C-191) shows 10.1% (pre-Mania) vs −0.3% (Mania construction) — a single stable blended dividend coexisted with value-destroying investment in the same company.
- **Evidence/quote:** Juxtaposition of C-190 and C-191.
- **Source/loc:** A4-Tuck (dividend) + B5-CampbellTurner-ManagerialFailure-2015 citing McCartney & Arnold 2001 · **Period:** 1845–47 (div) / 1850 (ROE) · **Geo:** GB · **Unit:** qualitative synthesis · **Conf:** medium
- **Counter/limits:** An inference across two separately-sourced facts, limited by the period mismatch and by lacking YNM segment-level dividend data. **Directly serves H2 (social value / operating profit ≠ investor return separation).**

### C-193
- **Branch:** QT4.4 · **Hyp:** H2 · **Class:** scholarly interpretation · **Status:** supported (general mechanism; not YNM-specific)
- **Claim:** Industry-wide, "closing the capital account" (charging maintenance/renewal revenue expenditure to capital) inflated reported net revenue/dividend capacity. Concrete non-YNM instance: the South Eastern Railway's May-1849 investigation found £150,000 "charged to capital instead of against revenue" over three years, ≈30% of dividends paid.
- **Evidence/quote:** "over the previous three years £150,000 had been 'charged to capital instead of against revenue.' This was about 30% of the dividends paid out during that period."
- **Source/loc:** A5-Odlyzko-Collapse-2011, lines 1998–2002 + 209–212 · **Period:** 1840s (SER: 3 yrs to ~May 1849) · **Geo:** GB · **Unit:** £ misclassified; ratio to dividends · **Conf:** high
- **Counter/limits:** Odlyzko argues critics overstated pervasiveness — even in 1849 railways paid ~1.9% dividends, so not "wholly delusive." SER, not YNM (see C-194 gap).

### C-194 — GAP
- **Branch:** QT4.4 · **Hyp:** H2 · **Class:** research inference · **Status:** gap
- **Claim:** The YNM-specific capital-to-revenue mechanism — the subject of McCartney & Arnold (2001), "Capital Clamours for Profitable Investment…" (J. Industrial History 4(2): 94–116) — is known only by title/citation; the primary was not available and no substantive claim is drawn from it.
- **Evidence/quote:** Identical reference in both Odlyzko's and Campbell & Turner's bibliographies.
- **Source/loc:** bibliographies of B5-CampbellTurner-ManagerialFailure-2015 & A5-Odlyzko-Collapse-2011 · **Period:** N/A · **Conf:** N/A · **Counter/limits:** The paper whose title implies it directly addresses the target mechanism, but per the read-the-passage rule no claim is made. Fetch this 2001 article in a future stage.

### C-195
- **Branch:** QT4.4 · **Hyp:** H2 · **Class:** quantitative estimate · **Status:** supported
- **Claim:** Industry-wide (established companies), average profit per mile fell £1,811 (1843) → £1,231 (1850); dividend/par "nearly halves"; avg mileage 36→153 mi and route density 11,761→7,013 persons/mile (1843→1850).
- **Evidence/quote:** "profit per mile falls from £1,811 in 1843 to £1,231 in 1850. The average return on capital also falls in this period and the dividend/par ratio nearly halves."
- **Source/loc:** B5-CampbellTurner-ManagerialFailure-2015, lines 431–57 · **Period:** 1843 vs 1850 · **Geo:** GB · **Unit:** £ profit/mile; persons/mile; dividend/par · **Conf:** medium-high
- **Counter/limits:** Industry aggregate (prose summary of an unextracted Table 6); "return on capital also falls" stated without a number.

### C-196
- **Branch:** QT4.4 · **Hyp:** — · **Class:** quantitative estimate · **Status:** supported
- **Claim:** For 15 railway ordinary shares, nominal dividend yields fell from 3.7% (1877) to 2.8% (1897).
- **Evidence/quote:** "Nominal dividend yields fell steadily from an average of 3.7% in 1877 to 2.8% in 1897."
- **Source/loc:** B5-MitchellChambersCrafts-2011, line 731 · **Period:** 1877–1897 · **Geo:** GB · **Unit:** nominal dividend yield % · **Conf:** high · **Counter/limits:** Later period; backbone context only.

### C-197 — SOURCE-PROVENANCE / BYLINE CORRECTION
- **Branch:** QT4.4 · **Hyp:** — · **Class:** historical fact (byline) / research inference (reconciliation) · **Status:** supported (byline); gap (reconciliation)
- **Claim:** The file at `railwaymania_managerial.txt` (Stage B key `B5-McCartney-ManagerialFailure-2024`) is actually **Campbell & Turner (2015), "Managerial Failure in Mid-Victorian Britain?"** (Business History, DOI 10.1080/00076791.2015.1026260) — re-keyed `B5-CampbellTurner-ManagerialFailure-2015`. The YNM 10.1%/−0.3% figures it reports are a citation to a distinct paper, McCartney & Arnold (2001), which was not read.
- **Evidence/quote:** "Managerial Failure in Mid-Victorian Britain?... / Gareth Campbell and John D. Turner / Queen's University Belfast" + "doi: 10.1080/00076791.2015.1026260."
- **Source/loc:** railwaymania_managerial.txt, lines 8–16, 31–35 · **Conf:** high (byline) · **Counter/limits:** T&F DOI-year conventions mean it's *possible* this same 2015-DOI'd paper was later issue-assigned to Business History 66(5) 2024 (would reconcile the descriptor but not the author/title mismatch) — not resolved here. Claims resting on the YNM figure are two-hop citations.

---

## Section C6 — Failure and investor impairment (UK-focused)

Sources: `A5-Odlyzko-Collapse-2011`, `A2-Campbell-Deriving-2013`, `B5-MitchellChambersCrafts-2011`. (US receivership evidence is in C8, not duplicated here.) This section carries the plan's mandatory **failure quota**.

### C-220
- **Branch:** QT4.1 · **Hyp:** H4 · **Class:** scholarly interpretation · **Status:** supported
- **Claim:** Of the "well-known" Mania fraud cases, only George Hudson's fraud on three of the four major lines he controlled was solidly established by later scholarship (Arnold & McCartney), despite popular impressions of pervasive fraud.
- **Evidence/quote:** "only the well-known cases of Hudson's fraud on three of the four major lines he controlled had been solidly established."
- **Source/loc:** A5-Odlyzko-Collapse-2011, p.6 · **Period:** 1849 · **Geo:** GB (Hudson's 4 lines) · **Unit:** count of lines (3 of 4) · **Conf:** high
- **Counter/limits:** Non-Hudson cases exist too (SER £150,000, C-193); fraud/aggressive-accounting boundary "extremely nebulous."

### C-221
- **Branch:** QT4.1 · **Hyp:** H4 · **Class:** historical fact · **Status:** supported
- **Claim:** North British Railway failure case: early 1849, 99 miles in service paying 4% on £1.7m capital, but 53.5 miles under construction projected at £4m for the full 152.5-mile line (per-mile cost ~2.5× higher for the unfinished part); within ~2 years no common dividend, only partial preference.
- **Evidence/quote:** "99 miles in service, and was paying out... 4% dividends on £1.7 million of capital. But there were 53.5 miles under construction, and the eventual cost of the entire 152.5 miles... £4 million"; "no dividend on the common shares, and only partial on the preference shares."
- **Source/loc:** A5-Odlyzko-Collapse-2011, p.6 · **Period:** 1849–c.1851 · **Geo:** Scotland (NBR) · **Unit:** £ capital in service vs projected; dividend % · **Conf:** medium
- **Counter/limits:** Company's own committee gave a "clean bill of health" — contemporary dispute; collapse date/% not exact.

### C-222
- **Branch:** QT4.2 · **Hyp:** H4 · **Class:** quantitative estimate · **Status:** supported
- **Claim:** Leeds and Thirsk Railway (>£2m capital): expected ~£20,000/mile cost & ~£3,000/mile revenue; actual >£30,000/mile cost & only ~£1,000/mile revenue by 1852 — ~50% cost overrun, ~67% revenue shortfall.
- **Evidence/quote:** "costs were over £30,000 per mile, while revenues in 1852 came only to about £1,000 per mile."
- **Source/loc:** A5-Odlyzko-Collapse-2011, p.44 · **Period:** plan (1845–46) vs 1852 · **Geo:** England (Yorkshire) · **Unit:** £/mile cost & revenue, planned vs realized · **Conf:** medium
- **Counter/limits:** Single case chosen for tractability, not representativeness.

### C-223
- **Branch:** QT4.2 · **Hyp:** H4 · **Class:** historical fact · **Status:** supported
- **Claim:** By the final £5/share call (Aug 1848, bringing Leeds & Thirsk to full £50 paid), the market discounted the investment by half — yet shareholders kept paying calls because they were legally obliged (sue/forfeit), showing calls could compel continued injection into an already-marked-down asset.
- **Evidence/quote:** "By the time the last call of £5 per share was paid in August 1848, the market was discounting the investments by half"; "shareholders were obliged to pay the calls, and if they did not, they could be sued, or forfeit their shares."
- **Source/loc:** A5-Odlyzko-Collapse-2011, p.45–46 · **Period:** Mar 1846–Aug 1848 · **Geo:** England · **Unit:** market/paid-up ratio; £5 call per £50 nominal · **Conf:** medium
- **Counter/limits:** Compulsion not absolute — collective shareholder action could halt projects; no national aggregate of suits/forfeitures.

### C-224
- **Branch:** QT4.3 · **Hyp:** H4 · **Class:** quantitative estimate · **Status:** supported
- **Claim:** Common-share dividends collapsed to an average 1.9% of paid-up capital in 1849, recovering only to 2.8% over 1849–1858 — below the ~4% expected of a stable company and below the ~3% Consol yield.
- **Evidence/quote:** "Dividends on common shares in railways averaged just 1.9% on the paid-up capital in 1849, and only 2.8% over the decade 1849–1858, according to one estimate." (source: Parl. Papers 1859 [2560] XXVII.637 p.xi)
- **Source/loc:** A5-Odlyzko-Collapse-2011, p.7 + p.54 · **Period:** 1849; 1849–1858 · **Geo:** UK · **Unit:** % dividend on paid-up capital, common shares, industry average · **Conf:** medium-high
- **Counter/limits:** Industry average masks dispersion (cf. NBR/Leeds & Thirsk); Arnold & McCartney's modern-method re-estimate differs; primary not read.

### C-225
- **Branch:** QT4.3 · **Hyp:** H4 · **Class:** quantitative estimate · **Status:** supported
- **Claim:** A distinct measure from the same report — return on total capital invested (common+preferred+loans) — was 2.8% (1849) and 3.6% avg (1849–1858); a different base from C-224 and not to be conflated.
- **Evidence/quote:** "return on total capital invested (common and preferred shares, as well as loans) of 2.8% in 1849, with an average of 3.6% over 1849–1858."
- **Source/loc:** A5-Odlyzko-Collapse-2011, p.54 fn 6 · **Period:** 1849; 1849–1858 · **Geo:** UK · **Unit:** % return on total capital (broader base than C-224) · **Conf:** medium-high
- **Counter/limits:** Coincides with C-224 for 1849 (both 2.8%) but diverges for the decade (2.8% vs 3.6%) — genuinely non-identical statistics.

### C-226
- **Branch:** QT4.4 · **Hyp:** H4 · **Class:** quantitative estimate · **Status:** supported
- **Claim:** Depending on delisting treatment, Campbell's "All Railways" index fell 66.1% (1,984→673, zero additional loss) or 69.9% (1,935→583, total loss) peak-to-trough.
- **Evidence/quote:** "66.1 per cent decline... 69.9 per cent decline. Using either approach, the downward movement in prices was substantial."
- **Source/loc:** A2-Campbell-Deriving-2013, p.8 · **Period:** Aug 1845 – ~1849–50 · **Geo:** GB (LSE) · **Unit:** market-cap-wtd price index, two scenarios · **Conf:** medium
- **Counter/limits:** Portfolio-average, not a £ aggregate loss; winding-up usually returned a positive sum → likely closer to 66.1% (C-234).

### C-227
- **Branch:** QT4.4 · **Hyp:** H4 · **Class:** quantitative estimate · **Status:** supported
- **Claim:** The same "All Railways" index had risen 93.5–98.4% (1843→Aug 1845) vs Established +71.7% and Non-Railways +18.8% — the scale of prior gains against which the 66–70% collapse must be read (boom vs bust for the identical index).
- **Evidence/quote:** (as C-114).
- **Source/loc:** A2-Campbell-Deriving-2013, p.6 · **Period:** 1843–Aug 1845 · **Geo:** LSE · **Unit:** % index rise · **Conf:** medium

### C-228
- **Branch:** QT4.5 · **Hyp:** H4 · **Class:** quantitative estimate · **Status:** supported
- **Claim:** The 1847 authorization cohort (last/worst) had mean realized return −19.6% (partially-paid) and −2.7% (fully-paid) — vs +57.5/36.0/21.8% (partially-paid) for 1844/45/46 — a clear weak-return cohort defined by entry timing.
- **Evidence/quote:** (as C-117).
- **Source/loc:** A2-Campbell-Deriving-2013, p.21 · **Period:** 1844–47 cohorts · **Geo:** GB · **Unit:** % mean return by cohort, leveraged/unleveraged · **Conf:** medium-high
- **Counter/limits:** 1847-cohort window biased toward post-peak; authorized companies only. **Failure-quota weak-cohort evidence.**

### C-229
- **Branch:** QT4.5 · **Hyp:** H4 · **Class:** quantitative estimate · **Status:** partially-supported
- **Claim:** YNM's early (pre-1845) lines earned 14% on shareholders' funds but the Mania extensions earned only 2.3% — an intra-company weak-return cohort.
- **Evidence/quote:** "The early lines of the York and North Midland had been earning a return on shareholders' funds of 14 per cent, but the extensions earned only 2.3 per cent."
- **Source/loc:** A2-Campbell-Deriving-2013, p.8 · **Period:** pre-1845 vs extensions · **Geo:** England (YNM) · **Unit:** % return on shareholders' funds · **Conf:** low-medium
- **Counter/limits:** Secondary citation to McCartney & Arnold 2001 (not read directly) — parallels the 10.1%/−0.3% figure (C-191); note the two figure-pairs differ, both trace to the same unread 2001 paper.

### C-230
- **Branch:** QT4.6 · **Hyp:** — · **Class:** historical fact · **Status:** supported
- **Claim:** Calls were a legally compulsory extraction (sue/forfeit for non-payment), so shareholders who had lost confidence could be compelled to keep injecting capital.
- **Evidence/quote:** "shareholders were obliged to pay the calls, and if they did not, they could be sued, or forfeit their shares."
- **Source/loc:** A5-Odlyzko-Collapse-2011, p.46 · **Period:** 1840s · **Geo:** GB · **Unit:** legal/institutional · **Conf:** high
- **Counter/limits:** Collective action could halt calls — not unconditional; no aggregate enforcement figures.

### C-231
- **Branch:** QT4.6 · **Hyp:** — · **Class:** historical fact · **Status:** supported
- **Claim:** It was common (not universal) to pay ~4% interest on calls-received before a branch opened; this "interest" was accounted as capital expenditure though economically an early return of the shareholder's own capital — inflating recorded "capital invested."
- **Evidence/quote:** "by the time shareholders had paid the full £20 per share, they had received £2 per share back in 'interest.' This was of course just an early return of capital, yet in the accounting of the time this 'interest' was counted as part of the capital expenditure."
- **Source/loc:** A5-Odlyzko-Collapse-2011, p.50 · **Period:** 1840s (£20/£2 example) · **Geo:** GB · **Unit:** £/share; interest-on-calls as capex · **Conf:** high
- **Counter/limits:** Illustrative example, not a national aggregate; a non-fraudulent accounting inconsistency.

### C-232
- **Branch:** QT4.6 · **Hyp:** H4 · **Class:** scholarly interpretation · **Status:** supported
- **Claim:** Though contemporaries blamed "calls" for the price collapse, both Odlyzko's review and Campbell's regression agree calls had only a transitory/secondary effect — Campbell finds the change-in-par variable significant but with R² <1%, dividends and low profitability far more important.
- **Evidence/quote:** Campbell: "the explanatory power of the change in par value variable is very low, with an R2 value of less than 1 per cent... supports the argument of Odlyzko (2011) that calls had only a transitory influence..."
- **Source/loc:** A5-Odlyzko-Collapse-2011 p.13; A2-Campbell-Deriving-2013 p.26 · **Period:** 1847–49 / 1843–50 · **Geo:** GB · **Unit:** regression coefficient & R²; qualitative · **Conf:** medium-high
- **Counter/limits:** Calls still statistically significant (not zero); contemporaries (Spackman, The Times) disagreed; two different methods combined as corroboration.

### C-233
- **Branch:** QT4.7 · **Hyp:** H4 · **Class:** quantitative estimate · **Status:** partially-supported
- **Claim:** Established pre-Mania lines survived in better health: Fig. 3 lines paid ~8% dividends at the start of 1847, vs the 1.9–2.8% industry average by 1849 once new lines entered the reckoning.
- **Evidence/quote:** "the approximately 8% dividend rates for the lines shown in Fig. 3 at the start of 1847, although that figure may have been somewhat exaggerated by improper accounting."
- **Source/loc:** A5-Odlyzko-Collapse-2011, p.8 · **Period:** start 1847 vs 1849–58 · **Geo:** GB (10-line sample) · **Unit:** % dividend rate · **Conf:** medium
- **Counter/limits:** Odlyzko flags the 8% "may have been exaggerated by improper accounting"; small non-random sample; not same-sample vs C-224.

### C-234
- **Branch:** QT4.7 · **Hyp:** — · **Class:** research inference · **Status:** partially-supported
- **Claim:** For the few delisted companies where winding-up was reported (Railway Times 1846, pp.522/550/599), shareholders received a positive residual — evidence the "100% loss" scenario (C-226) is a lower bound, not a central estimate.
- **Evidence/quote:** "there was a positive sum returned to shareholders, so it is likely that the first scenario is the upper boundary, and the second scenario is the lower boundary..."
- **Source/loc:** A2-Campbell-Deriving-2013, p.8 · **Period:** 1846 · **Geo:** GB · **Unit:** qualitative (positive vs zero residual) · **Conf:** low-medium
- **Counter/limits:** Small sample; no aggregate residual figure; doesn't claim to generalize.

### C-235
- **Branch:** QT4.7 · **Hyp:** H4 · **Class:** historical fact · **Status:** supported
- **Claim:** LNWR's survival mechanism (1848): capped total capex at £26m and "indefinitely postponing"/effectively abandoning all lines for which it had Acts but not yet commenced.
- **Evidence/quote:** "indefinitely postponing–and which the public understand as altogether abandoning–all the lines for which it has obtained acts, and which are not yet commenced."
- **Source/loc:** A5-Odlyzko-Collapse-2011, p.38–39 · **Period:** Oct–Nov 1848 · **Geo:** England (LNWR) · **Unit:** £26m ceiling; qualitative abandonment · **Conf:** medium-high
- **Counter/limits:** Odlyzko skeptical it was decisive (the £4m liability cut was small vs total capital) — may be perception management.

### C-236
- **Branch:** QT4.8 · **Hyp:** H4 · **Class:** historical fact · **Status:** supported
- **Claim:** Many Mania-promoted railways never received Parliamentary authorization at all (failing procedural requirements, or beaten by a competing scheme) — a distinct "never-authorized" failure category from "authorized-but-abandoned" (C-056).
- **Evidence/quote:** "Many of the railways promoted at the height of the boom never received Parliamentary authorisation..."
- **Source/loc:** A2-Campbell-Deriving-2013, p.7 · **Period:** 1845 · **Geo:** GB · **Unit:** qualitative · **Conf:** medium
- **Counter/limits:** No count given; "not authorised" cohort still ran up (peak price/par 3.03) and fell hardest — investors lost money speculating pre-authorization.

### C-237
- **Branch:** QT4.5 · **Hyp:** H4 · **Class:** quantitative estimate · **Status:** contested
- **Claim:** In a distinct later episode, 15-company 5-yr-MA ROCE eroded from 5.11%/5.63% (1872) to 4.29%/4.51% lows, recovering to 4.46%/4.62% (1910) — a slow secular decline, contested against Arnold & McCartney's steeper 4.8%(1872)→3.85%(1892)→3.54%(1912).
- **Evidence/quote:** "a much better performance than suggested by Arnold and McCartney who found that the weighted-average ROCE fell from 4.8 per cent in 1872 to 3.85 per cent in 1892 and to 3.54 per cent in 1912."
- **Source/loc:** B5-MitchellChambersCrafts-2011, p.9 · **Period:** 1872–1912 · **Geo:** GB (15 companies) · **Unit:** % ROCE, 5-yr MA · **Conf:** high
- **Counter/limits:** **A distinct episode from the 1847–50 bust** — the one clearly-evidenced weak-return cohort in this file, explicitly period-flagged; magnitude disputed vs Arnold & McCartney.

**C6 gaps:** aggregate UK £-investor-capital-loss figure — **GAP** (see Carried Gaps). Comprehensive count/mileage of formally abandoned Railway Acts (vs never-authorized/unbuilt) — **GAP**. Regional (vs cohort/company) return breakdown — **GAP** (partially offset by company-level cases).

---

## Section C7 — Competing interpretations

Sources: `B1-Odlyzko-Hallucinations-2010`, `B1-Campbell-Myopic-2012`, `B3-DonaldsonHornbeck-2016`, `B3-Leunig-2006`, Fogel (via D&H). Interpretation disputes carry status `contested`.

### C-270
- **Branch:** QT4.1 · **Hyp:** — · **Class:** scholarly interpretation · **Status:** contested
- **Claim:** Odlyzko's position: the Mania demonstrates genuine ex-ante market inefficiency — contemporaries had "trustworthy quantitative measures" showing insufficient demand, yet sustained a "collective hallucination"; the bust was predictable in advance.
- **Evidence/quote:** "it provides a convincing demonstration of market inefficiency. There were trustworthy quantitative measures to show investors... that there would not be enough demand..."; fn 107 directly rebuts Campbell by name.
- **Source/loc:** B1-Odlyzko-Hallucinations-2010, Abstract p.1 + fn 107 pp.271–72 · **Period:** 1840s · **Geo:** GB · **Unit:** ex-ante predictability, not numeric · **Conf:** medium
- **Counter/limits:** Campbell (C-271); narrative/close-reading argument, not a re-estimation of Campbell's regressions.

### C-271
- **Branch:** QT4.1 · **Hyp:** — · **Class:** scholarly interpretation · **Status:** contested
- **Claim:** Campbell's position: prices were consistent with non-railways once short-term dividend growth is controlled for; investors were "myopic but rational," their failure being inability to forecast longer-term dividend declines — implying the bust was hard to predict/prevent ex ante.
- **Evidence/quote:** "investors may have been myopic... but they remained rational... When... two years of dividend growth are included this apparent overpricing is entirely eliminated."
- **Source/loc:** B1-Campbell-Myopic-2012, Abstract + §6/Table 5 pp.18–19 + Conclusion p.30 · **Period:** 1843–1850 · **Geo:** GB · **Unit:** weekly cross-sectional dividend-yield regressions (417 weeks) · **Conf:** medium
- **Counter/limits:** **Citation-fidelity flag:** the exact string Odlyzko's fn 107 quotes ("Dividends rose and fell...") is NOT in the published 2012 Campbell text on file — Odlyzko (Jan 2010) quoted an earlier working-paper draft abstract, later revised; the substantive claim is unchanged. Odlyzko (C-270) argues available demand estimates made the bust foreseeable.

**Discriminating evidence (Mania):** neither paper runs the joint test — whether the specific contemporary demand estimates Odlyzko cites actually had power to forecast the magnitude/timing of the dividend decline that Campbell's regressions show going unpriced, and whether the analysts who produced them traded on their own forecasts. The fn 107 exchange is citation-level assertion/rebuttal, not a resolved empirical contest. **Verdict: genuine substantive disagreement, citation-level.**

### C-272
- **Branch:** QT5 · **Hyp:** — · **Class:** quantitative estimate (via D&H) / scholarly interpretation · **Status:** contested
- **Claim:** Fogel's (1964) social-saving approach — reported via D&H, Fogel's own text not read — bounds US railroads' value to agriculture at ≤2.7% of 1890 GNP ($321m: 0.6% inter-regional + 2.1% intraregional), with an upper bound (total loss of all agricultural land) of 5.35% of GNP.
- **Evidence/quote:** "Fogel's total social saving estimate of $321 million, or 2.7% of GNP... although the total loss of all agricultural land could only generate annual losses of $642 million or 5.35% of GNP."
- **Source/loc:** B3-DonaldsonHornbeck-2016, §II pp.805–806 · **Period:** 1890 · **Geo:** US · **Unit:** % of 1890 GNP; assumes zero transport-demand elasticity (upper bound) · **Conf:** medium
- **Counter/limits:** **Reported via D&H, not primary Fogel** (CDL borrow-only); D&H's GE result (C-273) is the opposing pole.

### C-273
- **Branch:** QT5 · **Hyp:** — · **Class:** quantitative estimate · **Status:** contested
- **Claim:** D&H's GE "market access" approach: removing all 1890 railroads would cut US agricultural land value 60.2% (s.e. 4.2%) → annual loss 3.22% (s.e. 0.22%) of GNP — **"moderately larger" than Fogel's 2.7%, NOT "more than double"**; max possible 5.35%.
- **Evidence/quote:** "decrease the total value of U.S. agricultural land by 60.2%... 3.22% (0.22%) of GNP in 1890"; "our market access approach finds moderately larger economic impacts... than... Fogel."
- **Source/loc:** B3-DonaldsonHornbeck-2016, §VI.A pp.840–41 + p.854 · **Period:** 1890 · **Geo:** US · **Unit:** % change in ag land value; % of GNP · **Conf:** high (point estimate as stated)
- **Counter/limits:** Sensitive to trade elasticity and to extrapolating the 1870–1890-estimated log-linear relationship to full-removal counterfactuals; both approaches examine only agriculture. **Corrects the Stage B "more than double" error.**

**Discriminating evidence (social value):** D&H frame their method as a "natural extension of Fogel's intuition," not a refutation ("moderately larger"). The open empirical question is whether the log-linear land-value/market-access relationship (estimated from 1870–90 variation, avg decline 60%) holds out-of-sample at the larger declines (avg 80%) implied by removing all railroads — an extrapolation D&H cannot fully validate. **Verdict: genuine, citation-level methodological disagreement, but nested/extension in tone.**

### C-274
- **Branch:** QT5 · **Hyp:** — · **Class:** scholarly interpretation · **Status:** supported (refinement lineage; NOT a second competing pair)
- **Claim:** Leunig (2006) frames his UK passenger social-savings estimates as revising/extending Hawke's method (same framework, revised counterfactual, extended to 1843–1912), not as a rival theory.
- **Evidence/quote:** "This article revises and extends Hawke's social savings... Hawke's passenger methodology is simple and correct." (Leunig's headline: ~14% of GDP by 1912; Hawke's 1865: 2.1%/5.8%, Leunig flags 2.1% "should be 1.6 per cent.")
- **Source/loc:** B3-Leunig-2006, p.640 · **Period:** 1843–1912 · **Geo:** GB (England & Wales) · **Unit:** passenger social saving as % of GDP · **Conf:** high
- **Counter/limits:** Not a competing pair by design; prior critiques (Baker/Fishlow/Gourvish) are within-framework refinements. **Do not present Hawke vs Leunig as a second Gate-2 competing pair.**

---

## Section C8 — Bounded comparative modules: canals + US

Sources: `B1-Odlyzko-Hallucinations-2010` (canals), `A5-PoorsManual-1899`, `A5-Lubben-2004` (US). Bounded per Gate 1 (U3/U4).

### C-310
- **Branch:** QT2/QT4 (canals) · **Hyp:** — · **Class:** historical fact · **Status:** partially-supported
- **Claim:** Infrastructure speculation predated railways: a "Canal Mania" occurred in the early 1790s, decades before the 1840s Railway Mania, though far smaller.
- **Evidence/quote:** "There was even a Canal Mania in the early 1790s, although a far, far smaller one... than the Railway Mania."
- **Source/loc:** B1-Odlyzko-Hallucinations-2010, p.40 · **Period:** early 1790s vs 1840s · **Geo:** GB · **Unit:** qualitative comparison · **Conf:** medium
- **Counter/limits:** Odlyzko notes "no comprehensive study of canal industry finances" — impressionistic.

### C-311
- **Branch:** QT2/QT4 (canals) · **Hyp:** — · **Class:** research inference · **Status:** partially-supported
- **Claim:** Financing/accounting excess was not railway-specific: a study of five British canals (Arnold & McCartney, via Odlyzko) found dividend rates significantly overstated true profitability on capital employed — analogous to the later railway distortion.
- **Evidence/quote:** "a careful study of the finances of five British canals just how serious a distortion this produced, in that dividend rates significantly overstated true profitability of capital that was employed."
- **Source/loc:** B1-Odlyzko-Hallucinations-2010, p.50 (+ p.40 on Jacob 1825's 5.75% avg dividend) · **Period:** late-18th–19th c. · **Geo:** GB canals · **Unit:** reported-dividend vs true-return gap · **Conf:** low-medium
- **Counter/limits:** Secondhand (Arnold & McCartney canal papers not read); some canals were "veritable gold mines" — heterogeneous. **NOTE:** correcting my Stage-C brief — the source says "five British canals," not "seven"; located in the Hallucinations paper, not `odlyzko_full.txt`.

### C-312
- **Branch:** QT4-QT5 (US) · **Hyp:** — · **Class:** historical fact / quantitative estimate · **Status:** supported
- **Claim:** Jan 1884–Jan 1900: 521 US railroad corporations (78,582 miles owned) went into receivership, total capitalization $5,353,869,099 (~$2.46bn share capital + $2,891,876,942 funded debt).
- **Evidence/quote:** "there were placed in the hands of receivers the... number of 521 railroad corporations... 78,582 miles, and a capitalization of $5,353,869,099..."
- **Source/loc:** A5-PoorsManual-1899, front-matter "A Study in Railway Statistics," pp. lxxi–lxxii · **Period:** 1884–1900 (16-yr cumulative) · **Geo:** US · **Unit:** count; miles owned; $ capitalization · **Conf:** medium-high
- **Counter/limits:** OCR imperfect (mileage renders 78,582 vs 78,562 in different passages); share-capital final digits uncertain (cross-checked by subtraction).

### C-313
- **Branch:** QT4-QT5 (US) · **Hyp:** — · **Class:** historical fact / quantitative estimate · **Status:** supported
- **Claim:** 1893 was the worst single year 1884–99: 119 companies, 27,883 miles, $835,768,845 share capital, $1,160,426,166 funded debt into receivership.
- **Evidence/quote:** "in that year no less than 119 companies, representing 27,883 miles of road, $835,768,845 share capital, and $1,160,426,166 [funded] debt, were forced under the protection of the Courts."
- **Source/loc:** A5-PoorsManual-1899, "A Study in Railway Statistics," p. lxxi · **Period:** 1893 · **Geo:** US · **Unit:** companies; miles; $ share capital & funded debt · **Conf:** medium-high
- **Counter/limits:** Lubben (C-316) reports 126 railroads by June 1894 / $2.5bn — related but not identical (different window/source).

### C-314
- **Branch:** QT4-QT5 (US) · **Hyp:** — · **Class:** quantitative estimate · **Status:** supported
- **Claim:** ~Half of the largest US railroads went through receivership 1890–WWI; a pre-WWI receivership made a railroad "more than two-and-a-half times (or 150%)" more likely to fail again, and reorganized railroads later failed at >2× the never-receivership rate.
- **Evidence/quote:** "approximately half of which went through a receivership between 1890 and this country's entry into World War I... more than two-and-a-half times (or 150%) more likely to undergo another receivership or bankruptcy after the War."
- **Source/loc:** A5-Lubben-2004, Abstract p.1421 + pp.1427–28 · **Period:** 1890–1917; post-WWI · **Geo:** US · **Unit:** receivership incidence & recurrence · **Conf:** medium-high
- **Counter/limits:** Sample = "largest railroads" (size not in the passage read); regression not independently reviewed.

### C-315
- **Branch:** QT4-QT5 (US) · **Hyp:** — · **Class:** historical fact · **Status:** supported
- **Claim:** The 1873 panic (optional second episode) began with the failure of Northern Pacific's financing bank, a 10-day NYSE closure, and 89 railroads defaulting on their bonds.
- **Evidence/quote:** "89 railroads defaulted on their bonds, which led to a general economic collapse lasting until the end of the decade."
- **Source/loc:** A5-Lubben-2004, p.1428 · **Period:** Sep 1873 – late 1870s · **Geo:** US · **Unit:** count of bond-defaulting railroads · **Conf:** medium
- **Counter/limits:** Lubben cites Cashman (1993), not primary railroad statistics; only bond defaults (no receivership count for 1873).

### C-316
- **Branch:** QT4-QT5 (US) · **Hyp:** — · **Class:** quantitative estimate · **Status:** supported
- **Claim:** The 1893 depression led to 126 railroads collapsing by June 1894, ≈$2.5bn (25% of total US railroad capital).
- **Evidence/quote:** "the collapse of 126 railroads by June of 1894, representing $2.5 billion (25%) of the total railroad capital at the time."
- **Source/loc:** A5-Lubben-2004, pp.1428–29 (citing Ripley 1915, Cashman 1993) · **Period:** 1893–Jun 1894 · **Geo:** US · **Unit:** count; $ / % of total railroad capital · **Conf:** medium
- **Counter/limits:** Twice-removed (Lubben citing Ripley/Cashman); not reconcilable with Poor's calendar-1893 tally (119 / ≈$2.0bn, C-313) due to window/source differences.

---

## Quantitative Backbone

Core series that will anchor `REV-HIST-001`. Each: variable · unit · frequency · period · geography · source key · original/reconstructed · caveats.

**Technology & diffusion (C1)**
1. Steam/water/wind horsepower mix — installed hp by prime-mover · benchmark years 1760–1907 · GB · `B4-Crafts-2004` (Table 3, Kanefsky) · reconstructed · 1800–38 gap; contested by Bottomley post-1838.
2. Capital & annual cost per steam hp — £ current · benchmark years 1760–1910 · GB (Manchester mill proxy) · `B4-Crafts-2004` (Table 4) · reconstructed · single-sector, non-representative; input to TFP estimates.
3. Coal per installed hp per year — lb/hp/yr · 4 points pre-1769→early-20th-c · GB · `B4-Crafts-2004` · reconstructed points · per-year not per-hour; stationary context.
4. Steam growth-accounting contribution — pp/yr · sub-periods 1760–1910 · GB · `B4-Crafts-2004` (Tables 5–7) · fully derived · model-dependent; substitutability assumption contested (C-021).
5. Bottomley revised national steam capacity 1870 — ihp by sector · 1870 · UK · `B4-Bottomley-2025` (Table 3) · reconstructed extrapolation (Suffolk) · single-county base; lower bound; **unreconciled with #1**.

**Capital formation & overbuild (C2)**
6. Mileage of new railway lines authorized by Parliament — miles/yr · 1822–1852 (& 1847–79 companion) · GB · `A1-NBER-FRED-Mileage` · original (Lewin / Parl. Papers) · two non-identical series for overlap years; 1840 negative = net abandonments.
7. Actual railway construction investment — £m/yr · 1845–1850 · GB · `A5-Odlyzko-Collapse-2011` · secondary compilation · GDP share (~8% 1847) contested by Mitchell 1964 (5.7/6.7/4.7%) — series #8.
8. Railway investment as % of GDP — % · 1846–48 · GB · `A2-Campbell-Deriving-2013` (Mitchell 1964) · secondary · unreconciled with #7.
9. Mileage in service & cost/revenue per mile — miles; £/mile · 1844–1851 · GB · `A5-Odlyzko-Collapse-2011` (Tooke & Newmarch) · secondary · industry aggregate.
10. Per-security nominal/par/uncalled capital — £/share · 1843–1850 · GB (LSE) · `A2-Campbell-Deriving-2013` · original (Railway Times, Tuck's, Scrivenor) · imputation for missing obs.
11. Adjusted paid-up capital & cumulated capex, 15 companies — £000 · 1870–1912 · GB · `B5-MitchellChambersCrafts-2011` (Table 1) · original archival (B.R. Mitchell/Deane project) · **post-Mania; excludes nominal additions.**

**Prices & investor returns (C3)**
12. Broad UK equity indices (all/UK/blue-chip; capital-gain, dividend-yield, total-return) — index/% · monthly · 1829–1929 · GB (London→+provincial) · `B2-CGT-BeforeCult-2019` · original · **no survivorship adjustment.** [U1 primary benchmark]
13. Broad British total-return indices, survivorship-adjusted — % · monthly · 1825–1870 · London only · `B2-Acheson-RuleBritannia-2009` · original · 3 attrition strategies × 2 bounds; London-only.
14. Railway Mania price indices (All/Established/Non-Railway; weekly & daily) — index · weekly/daily · 1843–1850 · GB (LSE) · `A2-Campbell-Deriving-2013` & `A2-CampbellTurner-GreatestBubble-2010` · original (Railway Times) · price-only; London-only; delisting-scenario-sensitive (peak/trough 1,984→673 / 2,017→672).
15. Return-by-authorization-cohort (price/par; realized returns) — % / ratio · cohorts 1844–1847 · GB · `A2-Campbell-Deriving-2013` (Table 2) · reconstructed · measurement-window timing biases later cohorts.
16. Consols benchmark — total return (BCE ~2.8%, 1830–1929) / running yield (RB 3.32%, 1825–70) — % · GB · `B2-CGT-BeforeCult-2019` & `B2-Acheson-RuleBritannia-2009` · original · the two are NOT interchangeable in construction. [U1 secondary]
17. London vs provincial return/correlation — % monthly return; R² · 1869–1929 · GB · `WP16-03-CampbellRogersTurner` · original · does not cover 1843–50.

**Operating & failure (C4/C5/C6)**
18. YNM paid-up capital / dividend / cumulative calls — £/share; £ · report dates 1845/1846/1847 · GB · `A4-Tuck-1845/1847/1848` · original (contemporary manual) · cumulative only, no dated call schedule; some OCR-scrambled.
19. Railway ROCE, 15 companies — % (5-yr MA) · 1870–1912 · GB · `B5-MitchellChambersCrafts-2011` (Table 1) · original · **post-Mania**; contested vs Arnold & McCartney.
20. Railway dividend collapse — % on paid-up / on total capital · 1849; 1849–1858 · UK · `A5-Odlyzko-Collapse-2011` (Parl. Papers 1859) · secondary · industry average, masks dispersion.

**US comparative (C8)**
21. US railroads in receivership — count / miles / $ · 1884–1899 (& 1893 peak) · US · `A5-PoorsManual-1899` · near-primary · OCR-scrambled annual detail (only prose aggregates usable); complemented by `A5-Lubben-2004`.

No charts created (per instruction — none needed to clarify a disputed series; the Crafts-vs-Bottomley and Odlyzko-vs-Mitchell disputes are documented in text as `contested`).

---

## Carried Stage B gaps — disposition

| # | Gap | Disposition | Basis |
|---|---|---|---|
| 1 | Aggregate UK investor-capital-loss figure | **Non-critical for Gate 2, but remains an open gap** | Confirmed absent from Odlyzko's full text (C-224/C-226 give index-level declines & dividend collapse, not a £ realized-loss aggregate); no called-vs-paid national series exists to derive it (C2 gaps). Failure quota is met via cohort/company evidence without it. |
| 2 | YNM dated call schedule | **Makes the cash-flow reconstruction `undecidable`; bounded, not closed** | C-166. A new Tuck 1848 ed. was found but has no dated schedule; only 3 Tuck eds. on archive.org. Alternative substrate (MCC 15-company PRO archive) flagged, not switched. |
| 3 | "Before the Cult of Equity" main-index provincial inclusion | **Resolved (qualitatively): post-1869 index is mixed London+provincial** | C-103 (fn 31). The inclusion question is settled; only the exact provincial *share* is undetermined (→ gap #4). |
| 4 | Provincial-underrepresentation magnitude for 1843–50 | **Bounded limitation; magnitude `undecidable`** | C-137/C-140/C-141: direction documented (railways foundational to provincial exchanges; 1870 shows 61–85% railway concentration), but no source covers 1843–50 quantitatively. Carry into `REV-HIST-001` as a stated limitation. |
| 5 | Arnold & McCartney (2004) full text | **Bounded limitation** | `verified-paywalled`, no open copy; the pre-1870 return question is partially covered by MCC 2011 (later period) and Odlyzko; the specific 1830–55 ROCE numbers remain uncited. |
| 6 | "Managerial Failure" authorship | **Resolved (with a new correction)** | C-197: the file is Campbell & Turner (2015) "Mid-Victorian," re-keyed. The YNM 10.1%/−0.3% figure is a two-hop citation to McCartney & Arnold (2001), primary unread (C-194 gap). |

New gap surfaced this stage: **Odlyzko ~8% vs Mitchell 5.7–6.7% railway-investment/GDP share (C-053/C-064)** — `undecidable` from available files (different denominators/definitions).

---

## Gate 2 Readiness Matrix

Self-assessment only — Gate 2 is not declared passed here.

| Gate 2 requirement | Status | Basis |
|---|---|---|
| Investor return evidence | **ready** | Cohort realized returns (C-117/C-228), broad-equity total returns & benchmark (C-107/C-108/C-128/C-133), railway sector returns (C-109), price-index falls with delisting sensitivity (C-112/C-113/C-120/C-121). |
| Failure cases | **ready** | NBR (C-221), Leeds & Thirsk (C-222/C-223), 1847 weak cohort (C-228), YNM extensions (C-229), never-authorized & abandoned schemes (C-056/C-236), dividend collapse (C-224/C-225). Failure quota met. |
| Competing interpretations | **ready** | Both pairs genuine & citation-level: Mania (C-270/C-271), social value (C-272/C-273); Hawke/Leunig correctly classed as refinement (C-274). |
| Operating profit separated from shareholder return | **ready** (Mania era partial) | ROCE method & series (C-185/C-187, 1870–1912); depreciation convention & dividends-from-capital (C-188/C-193); the hard-rule synthesis for YNM (C-190/C-191/C-192). Mania-era operating figures are OCR-limited (C-180–C-184) but the *separation principle* is evidenced. |
| Primary / near-primary quantitative sources | **ready** | Authorized-mileage series (C-063), Poor's Manual receivership (C-312/C-313), Tuck's manuals (C-150–C-164), contemporary Railway Times / Nash tabulations via Odlyzko, Railway Returns via MCC. |
| Post-bubble economic impact | **partial** | Long-run productivity/timing (C-006–C-011), post-Mania ROCE erosion (C-237), consolidation context. Weaker on a clean 1850s–70s "what productive infrastructure remained & who exploited it" quantification. |
| Explicit gaps and counter-evidence | **ready** | Every claim carries counter-evidence/limitations; the six carried gaps + new GDP-share gap are dispositioned above; contested items (C-015/C-064/C-189/C-237, both interpretation pairs) are labelled. |

**Two requirements not fully "ready": post-bubble economic impact (partial)** and the **Mania-era operating-profit figures (OCR-limited, partial)**. No requirement is `blocked`.

---

*Stage C deliverable complete. No `REV-HIST-001`, Pattern, Mapping, or Thesis created; no AI-era analogy. Next: Gate 2 Evidence Sufficiency Review.*
