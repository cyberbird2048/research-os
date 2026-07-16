---
id: HIS-002-SOURCE-REGISTER
type: source-register
title: HIS-002 Source Register — Electricity, Grid Infrastructure, and Industrial Electrification
status: draft
created: 2026-07-16
updated: 2026-07-16
owner: cyberbird
research_lead: codex
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
