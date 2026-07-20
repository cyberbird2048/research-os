---
id: HIS-002-SOURCE-REGISTER
type: source-register
title: HIS-002 Source Register — Electricity, Grid Infrastructure, and Industrial Electrification
status: draft
created: 2026-07-16
updated: 2026-07-20
owner: cyberbird
research_lead: codex
stage_b_verification_lead: claude-code
research_architect: chatgpt
review_date: 2026-08-04
confidence: low
sources: []
related:
  - HIS-002
  - HIS-002-BRIEF
  - HIS-002-PLAN
  - PAT-001
  - PAT-002
  - PAT-003
---

# HIS-002 Source Register

## Stage A status and limits

This is a **candidate-source landscape**, not an Evidence Ledger and not a set of historical findings. Bibliographic existence and a first-pass access path were checked on 2026-07-16. `verified-open` means the actual page, PDF, or downloadable dataset endpoint was opened; it does **not** mean that every relevant table, security, or methodology has already been extracted and audited. That work belongs to Stage B.

The register is bounded to the United States, c. 1900–1935, and to the three approved Pattern tests. It deliberately excludes consumer appliances, streetcars, rural electrification after 1935, non-US comparison cases, AI mapping, and investment conclusions.

## Access taxonomy

- `verified-open` — actual full text, PDF, primary document, or downloadable dataset endpoint opened.
- `verified-partial` — landing page or meaningful excerpt opened, but the full evidentiary object remains incomplete.
- `verified-paywalled` — bibliographic and relevance metadata checked; full text requires paid/institutional access.
- `access-failed` — direct access attempted and failed.
- `not-yet-checked` — candidate identified but direct access not yet tested.

## Candidate register

| Key | Source | Author / institution | Date | Type | Pattern / outcome lanes | Expected evidentiary role | Access | Reliability / Stage B caution |
|---|---|---|---:|---|---|---|---|---|
| S-001 | *Historical Statistics of the United States, 1789–1945* | U.S. Bureau of the Census | 1949 | official statistical compendium | PAT-002: Supports / Weakens / Rejects / Undecidable; QT-A | Generating plants, installed capacity, production per kW, industrial electric-energy use, utility output; backbone for capacity-versus-generation/load-factor tests | `verified-open` | High. Stage B must identify exact series, units, ownership coverage, and discontinuities; a PDF endpoint opened but one browser parse failed. |
| S-002 | *Census of Electrical Industries: Central Electric Light and Power Stations* (1902–1927 census sequence) | U.S. Bureau of the Census | 1902–1934 | primary official census | PAT-002 all lanes; PAT-001 contextual | Plant/equipment investment, capacity, output, customers, revenues, expenses, and ownership structure at census dates | `verified-partial` | High. Full-view bibliographic object located; Stage B must secure machine-readable scans or PDFs and reconcile changing census definitions. |
| S-003 | *Control of Power Companies* / FTC 1927 Annual Report summary | Federal Trade Commission | 1927 | primary regulatory investigation | PAT-001: Weakens / Supports; PAT-002: Weakens; PAT-003: Supports / Weakens | Holding-company control shares, installed capacity and generation by group, operating-versus-holding-company structure | `verified-open` | High for investigated facts; potentially adversarial/regulatory framing. Exact underlying Senate Document 213 remains preferable to the annual-report summary. |
| S-004 | FTC 1928 Annual Report, electric-power inquiry | Federal Trade Commission | 1928 | primary regulatory investigation | PAT-001 all lanes; PAT-002 Supports / Weakens; PAT-003 Supports | Pyramiding, service fees, property turnover, capitalized charges, duplicated distribution lines, rate-base regulation | `verified-open` | High for contemporaneous institutional evidence; Stage B must distinguish general observations from company-specific findings. |
| S-005 | FTC Utility Corporations investigation / 1929 Annual Report | Federal Trade Commission / U.S. Senate | 1928–1935 | primary hearings and investigation | PAT-001 all lanes; PAT-002 all lanes; PAT-003 all lanes | Capital assets/liabilities, security issuance, fees, affiliate relations, operating earnings/expenses, and public detriment across holding-company systems | `verified-open` | Potentially the most load-bearing primary source family. Ninety-plus volumes require a bounded index-first acquisition plan; do not treat the annual-report description as the final evidence. |
| S-006 | FTC 1933 Annual Report and operating-group energy schedules | Federal Trade Commission | 1933 | primary regulatory report | PAT-001 Supports / Weakens; PAT-002 Supports / Weakens / Rejects | Generated, disposed, and interstate-transmitted energy by operating-company group; fee-ledger investigation of Electric Bond & Share | `verified-open` | High. Stage B should locate the referenced group reports and map them to financial entities without mixing gas and electric operations. |
| S-007 | *Interstate Movement of Electric Energy* (S. Doc. 238) | Federal Trade Commission / U.S. Senate | 1930 | primary official report | PAT-002 all lanes; QT-A | Energy flows across state lines and development of interconnected systems | `verified-partial` | High. Existence and scope confirmed through FTC records; exact report PDF/table access still needs verification. |
| S-008 | *Common-Stock Indexes* / Cowles Commission historical data | Alfred Cowles 3rd / Cowles Commission; Yale ICF data host | 1938–1939 / current data host | reconstructed market dataset | PAT-001 all lanes; PAT-003 all lanes | Utility price, cash-dividend, income, and all-stock benchmark indexes through 1940; principal open benchmark candidate | `verified-open` | High but methodology-sensitive. Stage B must inspect the workbook universe, dividends, rebalancing, survivorship, utility classification, and whether holding/operating tiers can be separated. |
| S-009 | CRSP monthly U.S. stock database, 1926 onward | Center for Research in Security Prices | 1960s–present | security-level market dataset | PAT-001 all lanes; PAT-003 all lanes | Security-level returns, delistings, cohorts/vintages, broad-market controls from 1926–1935 | `verified-paywalled` | Highest-quality candidate for PAT-003, but access is not assumed. Paid-access escalation is premature until Cowles/FRASER/Moody's substitutes are tested. |
| S-010 | *Commercial and Financial Chronicle* issues and security tables | William B. Dana Co.; FRASER archive | 1900–1935 | contemporary financial press / primary market record | PAT-001 all lanes; PAT-003 all lanes | New issues, yields, prices, dividends, offerings, company capital structures, and contemporaneous investor framing | `verified-open` | High for quoted market facts, moderate for commentary. Stage B needs a bounded security/cohort sampling design rather than indiscriminate issue collection. |
| S-011 | *Losses to the Public in the Insull Collapse: 1932–1946* | Arthur R. Taylor | 1962 | academic security-loss reconstruction | PAT-001 Supports / Weakens; PAT-003 Supports / Weakens | Security-by-security disposition and investor losses in the Insull complex; timing and financing-tier comparison candidate | `verified-partial` | High relevance. Substantive notes/excerpts opened, but full article access must be rechecked. Its hold-to-liquidation method is not a general total-return index. |
| S-012 | *Moody's Manual of Investments: Public Utility Securities* | Moody's Investors Service | annual, especially 1920s–1935 | contemporary company/security manual | PAT-001 all lanes; PAT-003 all lanes | Operating-company versus holding-company capital structure, dividends, prices, issuance dates, subsidiaries, failures | `not-yet-checked` | Potentially load-bearing for tier/vintage reconstruction. Large-volume/manual access and OCR quality are likely constraints. |
| S-013 | *The Origin and Development of the Public Utility Holding Company in the United States* | Junko Nishikawa | 1968 | academic business history | PAT-001 Weakens / Supports; PAT-003 Supports / Weakens | Development and institutional logic of major utility holding companies before the late-1920s boom | `verified-open` | Moderate-high; useful orientation and source chain, not sufficient alone for returns or impairment. |
| S-014 | *Financial Economies, Consolidation Constraints, and the Early Organization of the Electricity Business* | academic working/conference paper | n.d. | academic interpretation | PAT-001 Weakens / Rejects; PAT-003 Supports / Weakens | Competing interpretation in which holding companies delivered financing/consolidation efficiencies and high returns | `verified-partial` | Important anti-confirmation candidate. Stage B must verify authorship, final venue, calculations, and whether the cited return is operating-company or holding-company equity. |
| S-015 | *Selling Power: Economics, Policy, and Electric Utilities Before 1940* | John L. Neufeld | 2016 | academic monograph | PAT-001 all lanes; PAT-002 Weakens / Rejects; PAT-003 all lanes | Industry economics, regulation, holding-company profitability, investment and policy context | `verified-partial` | High synthesis value, but chapter access is partial/paywalled. Use as source map; do not let a narrative claim substitute for return reconstruction. |
| S-016 | *Early Twentieth Century American Productivity Growth Dynamics* | Paul A. David and Gavin Wright | 2001 | academic economic history | PAT-001 Supports / Weakens / Undecidable | Electrification diffusion, manufacturing TFP acceleration, capital productivity, complementary labor-market change | `verified-open` | High. Full-text page opened. Stage B must separate electrification contribution from labor-market and other complementary causes. |
| S-017 | *The Dynamo and the Computer* | Paul A. David | 1990 | academic historical interpretation | PAT-001 Weakens / Undecidable; QT-A | Diffusion lag and complementary organizational capital; cautions against immediate productivity attribution | `verified-open` | High conceptual value, lower direct causal identification. Useful counterweight, not a standalone social-value estimate. |
| S-018 | *Powering Up Productivity: The Effects of Electrification on U.S. Manufacturing* | academic authors, NBER Working Paper 28076 | 2020 | modern causal economic history | PAT-001 Supports / Weakens / Rejects | County-industry causal estimates of productivity, output, employment, and heterogeneity from electrification, 1890–1940 | `verified-open` | High. Stage B must verify authors, full PDF, specifications, and timing overlap with security-return evidence. |
| S-019 | *Does Electricity Drive Structural Transformation? Evidence from the United States* | academic authors, NBER Working Paper 26477 | 2019 | modern causal economic history | PAT-001 Supports / Weakens | Employment reallocation and manufacturing structural transformation, 1910–1940 | `verified-partial` | High but partly outside 1935 and measures structural change rather than investor value. Use only where the pre-1935 window can be isolated. |
| S-020 | *The Most Technologically Progressive Decade of the Century* | Alexander J. Field | 2003 | academic macroeconomic history | PAT-001 Supports / Weakens; PAT-002 Weakens | Peak-to-peak productivity growth during 1929–1941 despite depressed output and investment | `verified-open` | High as competing macro interpretation; period extends beyond 1935 and electrification is not the sole mechanism. Boundary discipline required. |

## Pattern × outcome source architecture

This table records candidate coverage, not a verdict.

| Pattern | Supports candidates | Weakens candidates | Rejects candidates | Undecidable risk / diagnostic sources | Stage A assessment |
|---|---|---|---|---|---|
| PAT-001 — two-ledger divergence | S-005, S-008–S-012, S-016, S-018–S-020 | S-003–S-006, S-014–S-017 | S-008–S-010, S-014–S-016, if overlapping evidence shows investor returns tracked measured value | S-009/S-012 access; timing overlap between productivity estimates and investor returns; holding-vs-operating separation | Candidate coverage is broad enough for Stage B. The decisive task is matched-period comparison, not adding more productivity papers. |
| PAT-002 — financing overcommitment + separately tested physical overbuild | S-001–S-007, S-010, S-015 | S-001–S-007, S-014–S-015 | S-001–S-002 and S-006–S-007 if capacity/output/utilization track demand and returns | Capacity definitions, load-factor comparability, municipal/private segmentation, later-vintage operating returns | Physical-capacity leg has plausible official series; later-vintage returns and ownership segmentation remain uncertain. |
| PAT-003 — timing and financing structure | S-005, S-008–S-014 | S-008–S-015 | S-008–S-010 and S-012 if controlled tier/vintage dispersion is weak | CRSP/Moody's access; identifiers linking securities to holding/operating tiers; delistings and liquidation distributions | Weakest architecture. Stage B should test feasibility early and permit `Undecidable` if a defensible cohort/tier return set cannot be built. |

## Stage B priority queue

### Tier 1 — verify before expanding the bibliography

1. **Cowles utility and all-stock workbooks (S-008):** confirm downloadable data, index methodology, dividends, security universe, and whether a utility-sector benchmark can be formed for 1900–1935.
2. **Census / Historical Statistics series (S-001, S-002):** identify exact capacity, production, investment, revenue, expense, and industrial-use tables and definition changes.
3. **FTC Utility Corporations index and selected volumes (S-005, S-006):** locate a bounded set covering Insull, Electric Bond & Share, United Corporation, and operating-company energy/financial schedules.
4. **Insull security-loss reconstruction (S-011) plus Moody's/CFC source chain (S-010, S-012):** determine whether issuance-vintage and financing-tier outcomes can be reconstructed without CRSP.
5. **Electrification productivity pair (S-016, S-018) plus counterweight (S-017/S-020):** verify methods and isolate estimates within the approved period.

### Tier 2 — add only if Tier 1 leaves a real gap

- Company annual reports and state-commission filings for a small, pre-specified operating-company/holding-company sample.
- Federal Power Commission reports providing capacity, generation, load factors, investment, and ownership segmentation.
- Bankruptcy/receivership records for at least two holding-company failures and one operating utility that survived or recovered.

## Candidate case architecture

The eventual failure/survival sample is not selected yet, but Stage B should test these bounded candidates:

- **Insull system:** load-bearing failure and financing-tier case; strong primary/secondary source chain already identified.
- **Electric Bond & Share:** holding-company/operating-company fee and control case with FTC ledger access.
- **United Corporation or North American:** alternative large system to avoid treating Insull as the whole industry.
- **One conservatively financed operating utility:** negative/control case needed to test whether divergence or impairment was confined to pyramided holding companies.

No candidate is a conclusion. Selection must preserve operating-versus-holding-company separation and avoid survivorship-only sampling.

## Genuine Stage A gaps

1. **PAT-003 return reconstruction:** no verified-open security-level dataset has yet been shown to support issuance-vintage and financing-tier total returns with delistings. Cowles is the best open first test; CRSP and Moody's remain possible constraints.
2. **Entity linkage:** a reproducible mapping from top holding companies to subholding and operating-company securities is not yet built.
3. **Physical overbuild:** capacity and generation series exist, but their definitions and ability to measure regional or ownership-segment utilization are not yet verified.
4. **Matched-window PAT-001 test:** productivity/social-value estimates and investor-return data must overlap materially; otherwise PAT-001 becomes `Undecidable`, not Rejected.
5. **Negative/control evidence:** one non-pyramided or conservatively financed operating-utility case is needed so Insull does not predetermine the answer.
6. **Paid access:** no request is triggered at Stage A. Escalate only if a Gate-2-load-bearing table or dataset lacks an adequate open substitute after Tier 1 verification.

## Search log and anti-confirmation check

| Lane | Search focus completed in Stage A | Balance note |
|---|---|---|
| Supports | Productivity effects; holding-company losses; capacity/commitment and failure records | Covered, but not treated as the default outcome. |
| Weakens | Holding-company efficiencies; regulation; narrower tier/region effects; complementary-cause productivity literature | Covered through S-014–S-017 and segmentation requirements. |
| Rejects | Cowles/CRSP benchmark possibility; capacity/utilization tracking; operating-utility control case | Candidate architecture exists; actual negative tests remain Stage B/C work. |
| Undecidable | Data-access, entity-linkage, timing-overlap, and physical-utilization granularity failures | Explicitly preserved as an admissible outcome for all three Patterns. |

## Stage A completion assessment

- **Candidate landscape:** sufficient and bounded for Stage B verification.
- **Primary/official coverage:** strong for utility structure and physical-system statistics.
- **Academic coverage:** sufficient for competing productivity interpretations.
- **Investor-return coverage:** promising but not yet sufficient; this is the first Stage B feasibility test.
- **Scope compliance:** no Evidence Ledger claims, historical synthesis, Pattern promotion, AI mapping, or Thesis work performed.

**Stop point:** Source Orientation complete; awaiting review before substantive Stage B acquisition/verification expands this register.

---

# Stage B — Source Acquisition & Verification (verified-source readiness package)

**Author of this section:** claude-code (Repository Operator), 2026-07-20. Stage A above (the candidate landscape) was authored by codex; this Stage B section is appended without altering Stage A content.
**Authorization:** Research Architect verdict "PASSED WITH STAGE B CONDITIONS" (Stage A Source Orientation Review). Stage B is source acquisition & verification only. **No Evidence Ledger, historical synthesis, Mapping, Thesis, or Pattern promotion was created.**
**Method:** each source below was fetched through the session HTTPS proxy and the actual object opened/parsed (PDF via pypdf, HTML via bs4, `.xls` via xlrd). `verified-open` means the object was actually opened. Nothing is inferred; where an object could not be reached, it is marked `access-failed`/`verified-paywalled`/`verified-partial` with the actual HTTP code.

## Environment access caveats (affect several sources)

- **HathiTrust** `babel`/`catalog` full-text and page download return **HTTP 403** (Cloudflare bot-block) through this proxy — a channel limitation, **not** proof of non-existence. Catalog metadata is reachable via the HathiTrust API. Affects S-002 (later years), S-005 full text, S-012.
- **ftc.gov** report PDFs return **403** at the proxy; the **FRASER** (fraser.stlouisfed.org) mirrors of the same FTC documents return 200 and were used instead.
- **JSTOR / ResearchGate / Cambridge Core** return **403 / paywall** (S-011, S-014, and the canonical copies of S-017/S-020). Bibliographic identity was confirmed via open mirrors, Crossref, and author CVs.
- **census.gov / www2.census.gov, archive.org, FRASER, Yale SOM ICF, NBER** are fully reachable.

## Priority-order verdicts (per the Stage B review instruction)

1. **PAT-003 return-data feasibility — FEASIBLE-BUT-BOUNDED (blanket escalation NOT triggered; a bounded security-level access escalation is recommended).**
   - **Achievable now, from open sources (no CRSP):** a monthly **total-return** dataset for US electric/gas utilities **split by operating vs holding tier**, 1900–1935, with a matched broad-market control — parsed directly from the open Cowles data at Yale SOM ICF. Cowles Series C (dividend-reinvested total return) contains **C-11 "Utilities—Electric, Gas, Etc.—Operating Companies"**, **C-16 "…Holding Companies"**, **C-4 Utilities**, and **C-1 All Stocks**, monthly, densely populated across 1900–1935; the price (Series P) and dividend (Series Da) companions exist too. **This refutes Stage A's concern that operating/holding tiers could not be separated** — at the index tier they can, on a total-return basis. Gate 1 escalation conditions #1 (no utility return benchmark) and #2 (op/holding inseparable) are therefore **NOT met** at the index tier.
   - **NOT achievable from confirmed-open sources:** a **population-scale, security-level** return dataset *by issuance vintage / financing tier / capital structure with individual delisting-or-liquidation outcomes*. That requires **Moody's Manual of Investments: Public Utility Securities** (the definitive security-level tier/capital-structure/failure source), which was **not openly reachable** here (HathiTrust Cloudflare-403; archive.org holds only the 1917 *Steam Railroads* volume; Google Books quota-429), plus the **Taylor 1962** Insull loss study (paywalled). A bounded, hand-built cohort is possible from the open *Commercial & Financial Chronicle* (S-010, programmatic `cfc_YYYYMMDD.pdf`) cross-referenced to the Insull losses, but not a full population.
   - **Disposition:** the index-level tier-divergence test is answerable now (do NOT escalate that leg). The security-level vintage/capital-structure/outcome test is currently **Undecidable from confirmed-open sources** → **recommend a bounded paid/institutional-access escalation** (see Escalation Recommendation below), rather than forcing the whole Pattern to Undecidable.

2. **PAT-002 physical data-compatibility — COMPATIBLE-BUT-BOUNDED.** Capacity (kW), demand/output (kWh), and a **native utilization series** (Historical Statistics **Series G 204, kWh produced per kW installed** = capacity factor when ÷8760) are all defined in consistent physical units in the fully-reached S-001 (Chapter G), ownership-segmentable (private vs public from 1902; municipal/federal/other from 1920), **without any recourse to equity-price decline**. Bounded because clean *annual* data begin ~1920 (quinquennial-only + a Census-admitted 20–25% definitional variance before that), and S-002's census scope shifts across years (1912 folds in street railways). The strong window (~1920–1935) is the period of interest.

3. **PAT-001 matched-window — MATCHED-WINDOW-EXISTS.** The utility-investor-return window (Cowles ~1900–1935) overlaps materially with the electrification-productivity evidence, anchored by **S-018** (effects explicitly dated from 1900 on 1890–1940 data) and **S-016** (1920s manufacturing-TFP surge), both wholly inside the Cowles window; S-019 (1910–1935) and S-020 (1929–1935) add edge overlap. PAT-001 is therefore **not** Undecidable on matched-window grounds (Gate 1 escalation condition #3 NOT met). **Honesty caveat carried forward:** the overlap is *temporal* between *different outcome constructs* — the productivity sources measure TFP/MFP/labor productivity (the social/productivity ledger), not utility-investor returns (which come only from Cowles); the two ledgers must not be conflated when the divergence is tested in Stage C.

4. **Source-identity resolution (S-014, S-018, S-019) — complete** (see readiness table and Bibliographic Corrections below). S-014 remains **NON-load-bearing** pending full-text verification.

5. **FTC investigation bounded — index-first acquisition map built** (see below); the 90+ volume S-005 is not to be read indiscriminately.

## Verified-source readiness table (Tier 1)

Fields: identity · access (HTTP) · exact object reached · relevant tables/data · method & units · Pattern/outcome use · opco/holdco classification · load-bearing? · unresolved gap.

### S-008 — Cowles "Common-Stock Indexes" (Alfred Cowles 3rd & Assoc., Cowles Commission Monograph 3, 1938/1939)
- **Access:** `verified-open` (200). **Object:** Yale SOM ICF data page + parsed `.xls` files (`Stock_Prices-Cowles.xls`, `Stock_PricesincDvds-Cowles.xls` = Series C total return, `Dvd_Payments-1.xls`). **Data:** monthly index levels 1871→1940 (groups through 1938); **C-1 All Stocks (control), C-4 Utilities, C-11 electric/gas operating, C-16 electric/gas holding**; Series P price cols 13/18. **Method/units:** value-weighted common-stock indexes on Standard Statistics data; index-number units; survivorship handled at index level by chaining. **Use:** PAT-003 (return + broad-market-control + tier separation) and PAT-001 (the investor-return ledger). **opco/holdco:** separable at index tier (C-11 vs C-16), incl. total return. **Load-bearing:** YES (spine of the return leg). **Gap:** "Electric, Gas, Etc." mixes electric+gas (no pure-electric); index-level only — no security-level identities/vintages/capital structure/individual delistings; monograph methodology text not re-read.

### S-001 — Historical Statistics of the United States, 1789–1945 (Census, 1949) [+1975 ed.]
- **Access:** `verified-open` (200). **Object:** Chapter G PDF (`…/hist_stats_1789-1945-chG.pdf`), full-extracted. **Data:** Series G 171–233 — production by prime mover & by ownership (kWh), industrial use, **G 204 production per kW (utilization)**, G 205–224 installed capacity by prime mover & by ownership (kW), G 225–233 sales/customers/revenues. **Method/units:** kW, kWh (thousands), plant counts. **Use:** PAT-002 all three legs (capacity/output/utilization). **opco/holdco:** N/A (physical, not securities); **ownership** separable — private vs public from 1902, municipal/federal/other from 1920. **Load-bearing:** YES (primary physical source). **Gap:** quinquennial pre-1920 then annual from 1920; source switches (Census→USGS→FPC); pre-1920 20–25% definitional variance.

### S-002 — Census of Electrical Industries: Central Electric Light and Power Stations (1902–1927 seq.)
- **Access:** `verified-open` 1902/1907/1912 (archive.org djvu.txt, 200); `verified-partial` 1917–1932 (HathiTrust 403-blocked here). **Data:** private vs municipal station counts, dynamo capacity (HP and kW), output kWh by state, income/expenses, construction cost, equipment, at each census. **Method/units:** capacity in HP and kW (inconsistent early); output kWh. **Use:** PAT-002 (capacity/output/ownership benchmarks; corroborates S-001's 1902–1917 points). **Ownership:** private vs municipal separately tabulated every census. **Load-bearing:** secondary/corroborating. **Gap:** census **scope changes** (1912 broadened to include street/electrical railways) → raw cross-census totals not like-for-like; HP↔kW drift.

### S-005 — FTC "Utility Corporations" investigation (S. Doc. 92, 70th Cong.; 1928–1935)
- **Access:** `verified-open` (structure/catalog via HathiTrust API record 003849155 — 107 items, all public-domain Full view); `verified-partial`/`access-failed` for automated full text (`babel` 403; not on archive.org). **Object:** catalog record + structure. **Data:** Reports No. 1–84 (sub-parts incl. **84-A = 1935 Final Summary**; general indexes **71-B / 81-A / 84-D**) + Exhibit series No. 1–4047. Topical volumes: capital-asset growth, security issues, income/expenses, marketing of securities, inter-affiliate service fees, physical properties, holding-company structure. **Method/units:** company financial schedules (dollars), energy (kWh). **Use:** PAT-001/002/003 at entity level. **opco/holdco:** separable (its core subject). **Load-bearing:** load-bearing-**candidate** (contingent on a working full-text channel + triangulation vs Moody's/CFC for the same companies, given the FTC's adversarial framing). **Gap:** automated full text unreachable here → needs a **browser/institutional HathiTrust session**; report↔system crosswalk must be read from the index volumes first.

### S-006 — FTC 1933 Annual Report + operating-group energy schedules
- **Access:** `verified-open` via FRASER (`ftc_ar_1933.pdf`, 200, 149 pp). **Data:** energy generated/disposed/interstate-transmitted by each operating-company group (1929 & 1930); nine groups ≈18% of US electric energy, >80% of privately-owned interstate energy. **Method/units:** electric kWh, gas cu ft (cleanly separable). **Use:** PAT-002 output/interstate-flow leg; holding-company structure. **opco/holdco:** operating-company groups under holding control; municipal essentially out of scope. **Load-bearing:** supporting (output/interstate, not capacity). **Gap:** granular per-group schedules point to S-005 (S. Doc. 92) parts, not reprinted in the annual report.

### S-011 — Taylor, "Losses to the Public in the Insull Collapse: 1932–1946" (1962)
- **Access:** `verified-paywalled` (Cambridge Core landing 200 = paywall; JSTOR 403). **Identity (Crossref):** Arthur R. Taylor, *Business History Review* 36(2), Summer 1962, pp. 188–204, DOI 10.2307/3111455. **Method:** hold-to-liquidation security-loss reconstruction (dollar losses), NOT a total-return index. **Use:** PAT-003 (delisting/liquidation-outcome anchor) + PAT-001 (holding-company impairment). **opco/holdco:** holding-company case (Insull). **Load-bearing:** moderate (outcome-validation anchor). **Gap:** full text paywalled; one complex only.

### S-010 — Commercial and Financial Chronicle (William B. Dana Co.), via FRASER
- **Access:** `verified-open` (200). **Object:** FRASER title + parsed issue `cfc_19290105.pdf` (104 MB, 144 pp); pattern `cfc_YYYYMMDD.pdf` → whole 1900–1935 run enumerable. **Data:** weekly NYSE quotations (bid/ask, high-low), declared dividends, new-security offerings; Public Utility / Railway & Industrial / Bank & Quotation records. **Method/units:** primary contemporaneous quotations & dividends (raw, not an index). **Use:** PAT-003 (bounded hand-built cohort). **opco/holdco:** only via issuer identity (classify each security yourself vs Moody's/FTC). **Load-bearing:** yes for a bounded cohort. **Gap:** OCR-table extraction is the bottleneck (rough OCR on 100+ MB scans) → bounded sample only.

### S-012 — Moody's Manual of Investments: Public Utility Securities (1920s–1935)
- **Access:** `access-failed` (open reachability unverified). HathiTrust holds it but is Cloudflare-403 here; archive.org has only the 1917 *Steam Railroads* volume (used as a format/feasibility proxy — OCR'd, ~89 MB); Google Books API 429. **Data (as it would be used):** security-level issuer pages — capital structure, dividend/interest records, issuance dates, earnings, receiverships. **Use:** PAT-003 security-level legs (vintage, capital-structure tier, op-vs-holding classification, failures) — the definitive source. **opco/holdco:** yes at security level (if reachable). **Load-bearing:** YES, critically — **its inaccessibility is the single biggest open risk** for the security-level PAT-003 test. **Gap:** need a working HathiTrust/Google-Books/library route.

### S-016 — David & Wright, "Early Twentieth Century Productivity Growth Dynamics" (Oxford ESH WP _033, 1999; rev. 2005)
- **Access:** `verified-partial` (RePEc landing 200; direct PDF not reached — core.ac.uk 522, Oxford paths 404). **Method/window:** growth-accounting/TFP, US manufacturing ~1900–1929 (1920s surge); electrification as a capital-saving GPT. **Use:** PAT-001 productivity/social-value (interpretive). **Load-bearing:** yes (strongest interpretive social-value source in-window). **Gap:** electrification **not cleanly separable** (co-cause with a labor-market regime change); full-text PDF not fetched; register's "2001 / American" title is a variant (see corrections).

### S-017 — David, "The Dynamo and the Computer" (AER 80(2):355–361, 1990)
- **Access:** `verified-open` object (almendron.com PDF 200, image-scanned) / `verified-paywalled` canonical (JSTOR 403); bibliographic 200 via RePEc. **Method/window:** qualitative diffusion-lag interpretation, ~1880s–1920s; no dated numeric estimate. **Use:** PAT-001 framing only. **Load-bearing:** partial (framing; carries no value estimate alone). **Gap:** open PDF is an image scan (not machine-extractable here).

### S-018 — Fiszbein, Lafortune, Lewis & Tessada, "Powering Up Productivity" (NBER WP 28076)
- **Access:** `verified-open` (full PDF 200, 87 pp). **Identity CONFIRMED:** DOI 10.3386/w28076; Nov 2020, rev. Apr 2024; 1890–1940 sector-county. **Method/window:** energy-intensity × hydro-proximity IV; labor-productivity effects from 1900, ~10% faster growth by 1920. **Use:** PAT-001 productivity/social-value (primary, most rigorously identified). **Load-bearing:** YES (primary). **Gap:** working paper (not peer-reviewed); no material gap.

### S-019 — Gaggl, Gray, Marinescu & Morin, "Does Electricity Drive Structural Transformation?" (NBER WP 26477)
- **Access:** `verified-open` (landing/abstract 200). **Identity RESOLVED:** DOI 10.3386/w26477; Nov 2019; published *Labour Economics*, 2020. **Method/window:** transmission-line length instrumented by hydro potential; 1910–1940; measures **structural transformation (employment reallocation)**, not investor value or TFP. **Use:** PAT-001 social-transformation adjacency only. **Load-bearing:** NO / supporting only (wrong outcome construct; headline overshoots 1935). **Gap:** no clean 1910–1935 cut.

### S-020 — Field, "The Most Technologically Progressive Decade of the Century" (AER 93(4):1399–1413, 2003)
- **Access:** `verified-open` (SCU repository 200; AER landing 200; JSTOR 403). **Identity:** correct DOI **10.1257/000282803769206377**. **Method/window:** growth-accounting; 1929–1941 peak-to-peak MFP; straddles 1935; electrification not sole mechanism. **Use:** PAT-001 productivity/social-value (broad MFP). **Load-bearing:** partial. **Gap:** no 1929–1935-only figure; electrification's share not separable.

*(Also verified during Stage B: **S-003** FTC *Control of Power Companies* / S. Doc. 213, 69th Cong. — `verified-open` at the FTC-1927-summary level via FRASER; standalone S. Doc. 213 full text a gap. **S-004** FTC 1928 AR electric-power inquiry — `verified-open` via FRASER. **S-007** — `access-failed` and its citation corrected, see below. **S-014** — identity resolved, see below.)*

## FTC S-005 — bounded index-first acquisition map (do NOT read the 90+ volumes indiscriminately)

- **Step 0 (gate):** in a browser/institutional HathiTrust session, open the **general indexes — Reports 71-B, 81-A, 84-D — and the 1935 Summary Report 84-A** first, and read off the exact report-number and exhibit-number ranges for each target system. The report↔system crosswalk lives in these index volumes; do not guess it. This bounds acquisition to ~4 index/summary volumes + ~2 volumes per system.
- **Step 1 — cap at four systems:** Insull (Middle West Utilities, Commonwealth Edison, Insull Utility Investments, Corporation Securities Co. of Chicago); **Electric Bond & Share / EBASCO** (American & Foreign Power, American Power & Light, Electric Power & Light, National Power & Light) — also the direct test of S-014's cost-of-capital claim; United Corporation (United Gas Improvement, Public Service of NJ, Niagara Hudson); North American Co. (Union Electric, Washington Ry & Electric) as a comparatively-less-abusive candidate.
- **Step 2 — pull only these schedules, mapped to Pattern → lane:** Growth of Capital Assets / property write-ups → PAT-002 (financing leg); Security Issues & Marketing of Securities (issue dates/prices/tiers) → PAT-002 + PAT-003 (supplies the entity-linkage gap); **Public Utility Servicing — inter-affiliate fees → PAT-001** (Supports divergence if holdco "returns" were fee extraction; this is the direct rebuttal test of S-014); Income & Expenses (opco) → PAT-001; Physical Properties & the nine-group energy schedules → PAT-002 physical-overbuild leg. Keep gas/electric and holding/operating separated throughout.

## Bibliographic corrections log (Stage B)

1. **S-007 — citation corrected.** No support found for "S. Doc. 238, 1930." The corroborated FTC interstate-movement interim reports (under S. Res. 151, 71st Cong.) were **printed as S. Doc. 91 (Feb 28 1930, 4 pp) and S. Doc. 146 (May 12 1930, 6 pp)**. Treat "S. Doc. 238" as unverified/conflated; S-007's physical content is thin (4–6 pp summaries) and subsumed by S-006 + S-001. **S-007 is non-essential.**
2. **S-014 — identity resolved and paraphrase corrected.** Authors **W. Schrade & W. David Walls**; original = 28th IAEE conference paper (Taipei, June 2005); probable published descendant = "Holding companies, market liquidity, and the development of the electric power industry," *Journal of Energy and Development* 32(1):1–14 (2006). Its thesis is a **cost-of-capital / market-liquidity (financing-efficiency) argument for why the holding-company form emerged — NOT a measured "high equity return" series.** Whether it computes any realized return, at which tier, and by what method is **unverified** (full text 403/paywalled). **Do not enter a "high returns" claim on this source's authority.** It remains **NON-load-bearing** — it can *Weaken* a naïve "holding companies were purely value-destroying" reading of PAT-001, but cannot *Reject* PAT-001/PAT-003.
3. **S-016 — title/date variant.** Canonical: David & Wright, "Early Twentieth Century Productivity Growth Dynamics: An Inquiry into the Economic History of 'Our Ignorance'," Oxford ESH WP _033 (1999; rev. 2005). The register's "…American… (2001)" is a variant; the "2001" date is not confirmed.
4. **S-019 — authorship resolved:** Gaggl, Gray, Marinescu & Morin (was unattributed); published *Labour Economics* 2020.
5. **S-020 — DOI corrected** to 10.1257/000282803769206377 (a "…206488" variant is wrong / 404).

## Paid/institutional-access escalation recommendation (for the Source Verification Review to decide — NOT triggered unilaterally)

Per the Stage A paid-access rule (escalate only when a Gate-2-load-bearing object lacks an adequate open substitute after Tier 1 verification), Stage B has now established that two objects are load-bearing for the **security-level** PAT-003 test and have **no open substitute reachable from this environment**:

- **Moody's Manual of Investments: Public Utility Securities** (1920s–1935) — the definitive security-level tier / capital-structure / issuance-vintage / failure source. Open route blocked here (HathiTrust Cloudflare-403; not on archive.org; Google Books quota). **Recommended:** a browser/institutional HathiTrust session or a partner-library download.
- **Taylor (1962), "Losses to the Public in the Insull Collapse"** — the quantified holding-company outcome anchor. Paywalled (Cambridge/JSTOR). **Recommended:** institutional access to the *Business History Review* article.
- **FTC S. Doc. 92 full text (S-005)** — public-domain but `babel` is bot-blocked here; needs a **browser HathiTrust session** for the index volumes and the ~2-volumes-per-system extraction.

Note: the **index-level** PAT-003 test and the entire PAT-002 test require **no** paid access — they run on the open Cowles data and the open Census/Historical Statistics series. The escalation is scoped strictly to the security-level PAT-003 extension and the FTC entity-level extraction.

## Load-bearing gaps carried to the Source Verification Review

1. **Security-level PAT-003 data** (Moody's PU manuals + Taylor) — open route unproven; escalation recommended (above). The **index-level** tier-divergence test is unaffected and ready.
2. **FTC S-005 full-text channel** — HathiTrust browser/institutional session needed for the index-first extraction.
3. **Entity linkage** (top holding companies → subholding → operating-company securities) — to be built from the S-005 Security-Issues schedules + Moody's, once a full-text channel exists.
4. **S-002 cross-census definitional bridging** (1912 scope change) and **pre-1920 physical-data weakness** — must be handled explicitly in Stage C.
5. **PAT-001 construct caveat** — the matched window is temporal across *different* outcome constructs (productivity vs investor return); Stage C must not conflate the two ledgers.

## Stage B stop point

Source acquisition & verification complete for the Tier 1 set. **Stopping for the Source Verification Review.** No Evidence Ledger, historical synthesis, Mapping, Thesis, or Pattern promotion has been created. Stage C (Evidence Ledger) is not authorized and has not begun.
