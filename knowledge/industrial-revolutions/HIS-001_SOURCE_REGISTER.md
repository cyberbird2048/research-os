---
id: HIS-001-SOURCE-REGISTER
type: source-register
title: HIS-001 Source Register
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
---

# HIS-001 Source Register

Stage A ("Orientation") deliverable per `knowledge/industrial-revolutions/HIS-001_RESEARCH_EXECUTION_PLAN.md` §5 and `governance/HIS-001_GATE_1_REVIEW.md`. This is bibliographic reconnaissance only: it catalogs candidate sources, their expected role, reliability, and accessibility. **No claims are extracted here, no historical narrative is written, and no Evidence Ledger rows exist yet** — the Evidence Ledger is built in Stage C. Every source cited in the future Evidence Ledger or `REV-HIST-001` must have an entry here first (per `templates/SOURCE_REGISTER_TEMPLATE.md`).

Sourcing follows the open-access-first rule and paid-access trigger established at Gate 1 (decision U5; see `governance/HIS-001_GATE_1_REVIEW.md` and plan §5, §12).

## Access Verification Constraint — read before using this register

Both Stage A research passes hit the same environment limitation: **outbound `WebFetch`/direct-page-retrieval was rejected by this session's network egress policy for every external domain tested** (confirmed via the agent-proxy status endpoint: explicit `connect_rejected` / policy-denial entries for hosts including `www.nber.org` and `www.bankofengland.co.uk`; other hosts almost certainly failed the same way even where not individually logged). Per this environment's own proxy guidance, this is an organizational policy denial to be reported, not worked around.

Consequence: every "Access" judgment below is based on **web-search result metadata** (titles, snippets, hosting-domain patterns such as `.ac.uk` institutional repositories, SSRN, MPRA, EconStor, archive.org) and cross-confirmation across multiple independent search hits — **not** a confirmed `200 OK` fetch of the actual file. No URL, title, author, or date was fabricated; where a detail could not be verified, the researching agent flagged it explicitly rather than guessing.

**Action needed before Stage B relies on any single source as load-bearing:** re-verify that source's access path in an environment/session with working outbound fetch access (or via manual download by the user), particularly for anything marked "open" below on a working-paper mirror (SSRN, MPRA, EconStor, institutional repository) rather than a `.gov`/`archive.org` public-domain scan. This is a genuine infrastructure constraint on this session, not a defect in the source landscape itself — recommend escalating to the User per the Gate 1 escalation conditions if it persists into Stage B.

### How to read the columns

- **Access** — `open` (believed freely accessible by hosting pattern), `partial` (abstract-only, or borrow-only e.g. Internet Archive lending), `paywalled` (no open substitute found after a genuine search)
- **Expected Claims/Questions Supported** — references question-tree branches (QT1–QT6) and hypotheses (H1–H5) from the execution plan, since no Evidence Ledger claim IDs (`C-###`) exist yet. This column will be updated to reference actual `C-###` rows once the Evidence Ledger is built in Stage C.
- **Reliability** — a judgment on the source itself (methodology, peer-review status, distance from primary data), never on whether it supports a desired conclusion, per `governance/OPERATING_PRINCIPLES.md`.

---

## Part A — Primary / Near-Primary Sources (plan §3)

### A1. UK Parliamentary and Regulatory Records — serves QT1, QT4

| Source | Author/Compiler | Date | Source Type | Primary/Secondary | Claims/Questions Supported | Reliability | Access | Notes |
|---|---|---|---|---|---|---|---|---|
| NBER Macrohistory series: "Mileage of New Railway Lines Authorized by Parliament for Great Britain" | NBER Macrohistory Database, ultimate source H.G. Lewin, *Early British Railways* / *The Railway Mania and Its Aftermath, 1845–1852* (1936) | annual data ~1822–52, 1847–79 | reconstructed statistical series | Near-primary | QT1, QT4 (authorized-vs-built gap) | Medium-high | open | https://fred.stlouisfed.org/series/A0284DGBA374NNBR ; chain of custody is thin (one 1936 historian's compilation, not raw Board of Trade returns) |
| The Railways Archive (railwaysarchive.co.uk) — Board of Trade / Ministry of Transport document collection | independent volunteer digitization project | documents from 1841 | primary-document repository | Primary (for scanned items) | QT1, QT4 | Medium | open (for what's scanned) | https://www.railwaysarchive.co.uk/browse.php ; **unconfirmed** whether the specific annual statistical Railway Returns (vs. accident/legislative documents) are actually digitized here — needs manual confirmation before Gate 2 reliance |
| Digitized UK Parliamentary Papers (scattered volumes) | UK Parliament / archive.org scans | 1801–1852 (partial) | parliamentary record | Primary | QT1 | Low-medium | open (scattered), comprehensive corpus paywalled | Comprehensive indexed corpus is via ProQuest UK Parliamentary Papers (institutional subscription only); archive.org has only scattered individual volumes — **structural gap** |

**Category flag:** weakest-confirmed category for open access. Treat as most likely to require institutional ProQuest access or manual verification of railwaysarchive.co.uk's actual holdings.

### A2. Contemporary Security Price Records — serves QT2, QT3, QT4

| Source | Author/Compiler | Date | Source Type | Primary/Secondary | Claims/Questions Supported | Reliability | Access | Notes |
|---|---|---|---|---|---|---|---|---|
| *The Course of the Exchange, and Other Things* | John Castaing (from 1698), successors | 1698–19th c. | periodical | Primary | QT2, QT3 | High (contemporaneous) | paywalled/restricted, no open copy found | Foundational primary source but not independently accessible; project will rely on scholarly reconstructions below — a dependency worth flagging |
| Campbell, Grossman & Turner, "New Monthly Indices of the British Share Market, 1829–1929" (QUCEH WP 19-01 / CEPR DP13717) | Gareth Campbell, Richard Grossman, John D. Turner | 2019 (index covers 1829–1929) | reconstructed index (working paper) | Near-primary | QT2, QT3, QT4; **primary candidate for the Gate 1 U1 broad-equity-index benchmark** | High | open (QUCEH/SSRN working paper; published version status unconfirmed) | Built from Course of the Exchange + Investor's Monthly Manual — both **London-centric periodicals**; see provincial-bias flag below |
| Campbell & Turner, "Deriving the Railway Mania" (2013, *Financial History Review* 20(1)) and "'The Greatest Bubble in History'" (2010) | Gareth Campbell, John D. Turner | 2010–2013 | reconstructed daily index (peer-reviewed + preprint) | Near-primary | QT2, QT3, QT4 (Mania/bust window specifically) | High | open via MPRA/SSRN preprints; journal version paywalled | Most precisely scoped index to the 1843–1850 Mania/bust window |

**Flags:**
- No open substitute found for the commercial vendor "Global Financial Data" — not needed; Campbell/Turner outputs above are the credible open functional substitute.
- **Provincial-exchange digitization bias (structural, unresolved):** Manchester/Liverpool investors reportedly held ~37% of nominal railway share value vs. London's ~17%, and dedicated provincial exchanges (Manchester, Liverpool, Glasgow, Edinburgh, others) operated from 1836/1844. A QUCEH working paper on "The Rise and Decline of the UK's Provincial Stock Markets" exists but could not be fetch-verified. **It is not confirmed whether provincial-only-listed companies are incorporated into the Campbell/Turner indices** above, as opposed to only London/dual-listed shares — treat as an open, unresolved digitization-bias question, not as solved. This is directly relevant to the project's survivorship-bias concern.

### A3. Company Records — serves QT2, QT3, QT4, QT5

| Source | Author/Compiler | Date | Source Type | Primary/Secondary | Claims/Questions Supported | Reliability | Access | Notes |
|---|---|---|---|---|---|---|---|---|
| TNA (Kew) railway company records, RAIL series | The National Archives, UK | 19th–20th c. | primary company records | Primary | QT2, QT3, QT4, QT5 | High | mostly paywalled-per-item or in-person only | Catalogue/finding-aid free to browse; documents generally require a Kew visit or paid per-item download — genuine structural access gap at scale |
| "Railway Returns and Railway Audit" (House of Lords debate, 5 Feb 1850), Historic Hansard | UK Parliament | 1850 | primary parliamentary debate transcript | Primary | QT3 (contemporaneous evidence of dividend-from-capital/audit-quality controversy) | High (for what it documents; speaker bias present) | open | https://api.parliament.uk/historic-hansard/lords/1850/feb/05/railway-returns-and-railway-audit |
| "Development of British Railway Accounting: 1800–1911" | (hosted via University of Mississippi eGrove repository) | — | scholarly/secondary, documents primary accounting practice | Secondary (documents primary practice) | QT3 | High | open | https://egrove.olemiss.edu — confirms the 1868 Regulation of Railways Act first mandated standardized accounts/the "double account system," implying pre-1868 accounts genuinely lacked a depreciation standard |

### A4. Contemporary Press and Reference Works — serves QT2, QT3, QT4, QT5

| Source | Author/Compiler | Date | Source Type | Primary/Secondary | Claims/Questions Supported | Reliability | Access | Notes |
|---|---|---|---|---|---|---|---|---|
| *The Economist*, Historical Archive | The Economist / digitized by Gale | from 1843 | periodical | Primary | QT2, QT3, QT4 | High | **paywalled, no open substitute found** | Gale commercial database, institutional-subscription only; NYPL free-library-card access is a quasi-open individual path, not bulk/open data |
| *The Railway Times* | London periodical | 1837/1839–1863 (partial run digitized) | periodical | Primary | QT2, QT3, QT4 | High | open (partial run) | https://archive.org/details/railwaytimes100londuoft ; comprehensive searchable run exists via paywalled British Newspaper Archive |
| Bradshaw's Railway Manual, Shareholders' Guide and Official Directory | W.J. Adams / George Bradshaw's office | annual, 1848–1923 | reference work | Primary (company self-reported) | QT2, QT3, QT5 | Medium-high | open | https://archive.org/details/bradshawsrailwa00unkngoog ; subject to same dividend/depreciation caveats as A3 |
| The Railway Shareholder's Manual | Henry Tuck | 19th c. | reference work | Primary | QT2, QT3, QT4 | Medium-high | open | https://archive.org/details/railwaysharehol02tuckgoog ; independent cross-check source vs. Bradshaw's |

### A5. Failure Records — serves QT4, QT5 (US comparative capped to ≤2 panics per Gate 1 U3)

| Source | Author/Compiler | Date | Source Type | Primary/Secondary | Claims/Questions Supported | Reliability | Access | Notes |
|---|---|---|---|---|---|---|---|---|
| Poor's Manual of the Railroads of the United States | Henry Varnum Poor | annual, 1868–1917 (23 vols.) | statistical compendium | Near-primary | QT5, US comparative (financing fragility/receivership, per U3 cap) | High | open (public-domain pre-1929 volumes) | Multiple free volumes on archive.org/HathiTrust; **strongest confirmed open source for the project's US failure-quota requirement** |
| Odlyzko, "The Collapse of the Railway Mania... Robert Lucas Nash, a Forgotten Pioneer..." | Andrew Odlyzko | 2011 | secondary, recovers a primary contemporary analyst's work | Secondary/near-primary | QT4 (bust mechanics, shareholders ruined by calls) | High | open (author's page, SSRN) | Re-derives from Robert Lucas Nash, a genuine contemporary financial analyst |
| US receivership figures for 1873 and 1893 (via Federal Reserve History essay; cross-checked against tertiary summaries) | various (ultimately traceable to Poor's Manual / ICC annual reports) | 1873–74, 1893–94 | secondary/tertiary restatement | Secondary (points to near-primary) | QT4, QT5 (US comparative, 2-of-3 cap applied to 1873 & 1893) | Medium (as found) — **primary backbone is Poor's Manual (above), not yet extracted** | open (secondary essays), primary backbone open but unextracted | ~55–89 of 364 US railroads failed by 1873–74; ~125–150+ into receivership in 1893, ~¼ of US rail mileage in receivership 1893–94; figures need re-derivation from Poor's Manual annual volumes in Stage C, not taken as final from secondary summaries |

**UK abandonment scale (cross-referenced, multiple independent sources):** of ~12,000 miles authorized by Parliament 1844–48, only ~7,200 miles (~60%) were completed by 1852; share prices fell ~53–66% 1845–1850. Sourced from the NBER/Lewin series (A1) and Odlyzko's work above — flagged here as a figure needing formal C-### sourcing in Stage C, not yet a ledger claim.

### A6. US Quantitative Compendia — serves QT5, QT6 (US comparative, capped per U3)

| Source | Author/Compiler | Date | Source Type | Primary/Secondary | Claims/Questions Supported | Reliability | Access | Notes |
|---|---|---|---|---|---|---|---|---|
| Poor's Manual of Railroads | (see A5) | — | — | — | — | — | — | cross-listed with A5 |
| ICPSR Study 2896, "Historical, Demographic, Economic, and Social Data: The United States, 1790–2002" | Michael R. Haines, building on ICPSR Study 0003 | — | statistical compendium | Near-primary | QT5 | High | **partial** — institutional-membership gated | NHGIS (nhgis.org) offers free-registration access to related Census series, but not specifically railroad financial/receivership data |
| ICPSR 36353 / Jeremy Atack, "Historical Transportation of Navigable Rivers, Canals, and Railroads in the United States" | Jeremy Atack (Vanderbilt/NBER) | network-extent snapshots: 1840, 1845, 1850, 1861, 1870+ | GIS geographic dataset | Near-primary | QT1, QT5 | High | open | https://my.vanderbilt.edu/jeremyatack/data-downloads/ — freely downloadable directly from author, no institutional login; also mirrored at LOC |
| Historical Statistics of the United States — 1949/1960 editions (free) vs. 2006 Millennial Edition (paywalled) | US Census Bureau (1949/1960); Carter, Gartner, Haines, Olmstead, Sutch, Wright eds., Cambridge UP (2006) | 1949, 1960, 2006 | official statistical compendium | Primary/near-primary | QT5, QT6 | High (Millennial Edition more reliable/corrected) | **mixed**: 1949/1960 open; 2006 Millennial Edition paywalled, no free full text found | Free older editions at census.gov are real substitutes but less comprehensive/not reconciled with modern corrections |

---

## Part B — Academic / Institutional Sources (plan §4)

### B1. Railway Mania Financial Economics — serves QT4, H3, H5 — **required competing-interpretation pair present**

| Source | Author | Date | Source Type | Primary/Secondary | Claims/Questions Supported | Reliability | Access | Notes |
|---|---|---|---|---|---|---|---|---|
| "Dispelling the Myth of the Naive Investor during the British Railway Mania, 1845–1846" | Gareth Campbell & John D. Turner | 2012, *Business History Review* 86(1) | peer-reviewed article | Secondary | QT4, H3, H5 | High | open (QUB repository); publisher version paywalled | Position: prices tracked short-run fundamentals ("not naive") |
| "Myopic rationality in a Mania" | Gareth Campbell | 2012, *Explorations in Economic History* 49(1) | peer-reviewed article | Secondary | QT4, H5 | High | open (MPRA); publisher paywalled | Coins "myopic rationality" — the near-rational pole of the debate |
| "'The Greatest Bubble in History'" / "Cross-Section of a 'Bubble'" | Gareth Campbell & John D. Turner | ~2010, MPRA WPs 21820/21821 | working paper (final venue unconfirmed) | Secondary | QT2, QT3, QT4 | Medium-high | open (MPRA/RePEc) | Micro cross-section of share prices/dividends during the Mania |
| "Deriving the railway mania" | Gareth Campbell & John D. Turner | 2013, *Financial History Review* 20(1) | peer-reviewed article | Secondary | QT4 | High | open (QUB repository); publisher paywalled | Models price-expectation formation, LSE railway-securities dataset 1843–1850 |
| "The role of the media in a bubble" | Campbell, Turner & Walker | 2012, *Explorations in Economic History* 49(4) | peer-reviewed article | Secondary | QT4 | High | open (authors' project site); publisher paywalled | Finds media transmitted facts rather than independently inflating the bubble |
| "Collective Hallucinations and Inefficient Markets: The British Railway Mania of the 1840s" | Andrew Odlyzko | 2010 (working paper) | working paper | Secondary | QT4, H3, H5 | Medium-high | open (author's page, SSRN) | **Opposing position** to Campbell/Turner: argues oversupply warning signs were available and ignored — genuine market inefficiency, not myopic rationality |
| "Bubbles, Gullibility, and Other Challenges..." | Andrew Odlyzko | 2010, *First Monday* 15(9) | peer-reviewed (open-access journal) | Secondary | QT4 | High (for an interdisciplinary venue) | open | Broadens the "gullibility" thesis beyond railways |
| "The Collapse of the Railway Mania... Robert Lucas Nash..." | Andrew Odlyzko | 2011, *Accounting History Review* 21(3) | peer-reviewed article | Secondary (recovers primary source) | QT4 | High | open (author's page); publisher paywalled | Cross-listed at A5 |

**Required competing-interpretation pair #1 (Gate 2):** Campbell & Turner ("myopic rationality" — prices broadly tracked short-run fundamentals, investors not naive) **vs.** Odlyzko ("collective hallucination" — quantitative warning signs of oversupply were ignored, genuine inefficiency). Both sides are openly accessible.

### B2. Long-Run UK Asset Returns — serves the Gate 1 U1/U6 excess-return benchmark

| Source | Author | Date | Source Type | Primary/Secondary | Claims/Questions Supported | Reliability | Access | Notes |
|---|---|---|---|---|---|---|---|---|
| "Rule Britannia! British Stock Market Returns, 1825–1870" | Acheson, Hickson, Turner & Ye | 2009, *Journal of Economic History* 69(4) | peer-reviewed article | Primary-adjacent (built from primary price/dividend records) | QT2, QT3, U1 benchmark (pre-1870 segment) | High | open (Stirling repository); publisher paywalled | Addresses survivorship bias explicitly; dividends dominate returns |
| "New Indices of British Equity Prices, 1870–1913" | Richard S. Grossman | 2002, *Journal of Economic History* 62(1) | peer-reviewed article | Secondary/index-construction | U1 benchmark (post-1870 segment) | High | **paywalled, no free copy found** | Load-bearing gap — see summary below; may be substitutable by B2's next entry |
| "Before the Cult of Equity: New Monthly Indices of the British Share Market, 1829–1929" | Campbell, Grossman & Turner | 2019, QUCEH WP19-01 / CEPR DP13717 | working paper (final venue unconfirmed) | Secondary | **Primary candidate for the U1 benchmark — spans the entire Mania window and beyond in one continuous series** | High-ish | open (QUCEH, SSRN) | Cross-listed at A2 |
| "What Moved Share Prices in the Nineteenth-Century London Stock Market?" | Campbell, Quinn, Turner & Ye | 2018, *Economic History Review* | peer-reviewed article | Secondary | QT2, QT3 | High | open (QUB repository); publisher paywalled | Same underlying database as the two entries above |
| "Stocks for the Long Run: New Monthly Indices of British Equities, 1869–1929" | Richard S. Grossman | Wesleyan WP 2017-004 / CEPR DP12121 (final venue unconfirmed) | working paper | Secondary | U1 benchmark (alternative splice) | Medium-high | open claimed (RePEc/SSRN), full-text access not independently confirmed | Alternative to the Campbell/Grossman/Turner (2019) splice for the same purpose |

**Note:** the UK consol/gilt-yield series (secondary benchmark per Gate 1 U1) is expected to come from the Bank of England Millennium dataset (B6), not a dedicated paper.

### B3. Social Savings / Counterfactual Literature — serves QT5, H2 — **required competing-interpretation pair present**

| Source | Author | Date | Source Type | Primary/Secondary | Claims/Questions Supported | Reliability | Access | Notes |
|---|---|---|---|---|---|---|---|---|
| *Railroads and American Economic Growth: Essays in Econometric History* | Robert W. Fogel | 1964, Johns Hopkins UP | book | Secondary | QT5, H2 | High (methodologically contested, not weak) | open | https://archive.org/details/railroadsamerica00foge — classic "social saving <5% of GNP, railroads not indispensable" position |
| *American Railroads and the Transformation of the Ante-bellum Economy* | Albert Fishlow | 1965, Harvard UP | book | Secondary | QT5, H2 | High | **paywalled, no open copy found** | Foundational US antebellum text; found ~4% of GNP social saving for 1859, via forward-linkage extensions Fogel didn't use — load-bearing gap |
| *Railways and Economic Growth in England and Wales, 1840–1870* | G.R. Hawke | 1970, Clarendon Press | book | Secondary | QT5, H2 (UK) | High (canonical UK study) | **partial** (Internet Archive borrow-only) | Found UK social savings 7–11% of national income by 1865 — materially larger than Fogel's US figure |
| "Time is Money: A Re-Assessment of the Passenger Social Savings from Victorian British Railways" | Tim Leunig | 2006, *Journal of Economic History* 66(3) | peer-reviewed article | Secondary | QT5, H2 | High | open (LSE Research Online) | Revises Hawke's passenger estimates upward using 1843–1912 timetable data |
| "Social savings" (survey) | Tim Leunig | 2010, *Journal of Economic Surveys* 24(5) | peer-reviewed survey | Secondary | QT5, H2 | High | open (LSE Research Online); publisher paywalled | Best single map of the social-savings methodological debate — efficient source for Gate 2 |
| "Railroads and American Economic Growth: A 'Market Access' Approach" | Dave Donaldson & Richard Hornbeck | 2016, *QJE* 131(2) (NBER WP 19213, 2013) | peer-reviewed article (top journal) | Secondary | QT5, H2 | High | open (author's site, SSRN); NBER/publisher paywalled | **Opposing position** to Fogel: GE "market access" approach finds substantially larger true US railroad impact |
| "The Transport Revolution in Industrializing Britain: A Survey" | Dan Bogart | working paper, ~2013 draft | working paper (final venue unconfirmed) | Secondary | QT1, QT5 | Medium-high | open (author's site) | UK freight-cost decline survey (~95% real decline 1700–1870); contextual, not a head-to-head estimate |

**Required competing-interpretation pair #2 (Gate 2):** Fogel/Fishlow ("modest social savings, railroads not strictly indispensable," partial-equilibrium counterfactual) **vs.** Donaldson & Hornbeck ("general-equilibrium market-access approach shows much larger true impact," directly contesting Fogel on methodological grounds). Bonus internal dispute: Hawke vs. Leunig (UK passenger-estimate refinement, same method, different assumptions).

### B4. Steam Power / GPT Diffusion Economics — serves QT1, QT5.3

| Source | Author | Date | Source Type | Primary/Secondary | Claims/Questions Supported | Reliability | Access | Notes |
|---|---|---|---|---|---|---|---|---|
| *Steam Power and British Industrialization to 1860* | G.N. von Tunzelmann | 1978, Oxford UP | book | Secondary | QT1, QT5.3 | High (benchmark quantitative treatment) | **paywalled, no open copy found** | Foundational text; partially substitutable by the two entries below |
| "Steam as a General Purpose Technology: A Growth Accounting Perspective" | Nicholas Crafts | 2004, *Economic Journal* 114(495) | peer-reviewed article | Secondary | QT1, QT5.3, H5 | High | open (LSE working-paper version); publisher paywalled | Growth-accounting: near-zero steam productivity contribution pre-1830, rising to ~0.4pp/yr and two-fifths of productivity growth 1850–70 — central H5 (timing) evidence |
| "The early diffusion of the steam engine in Britain, 1700–1800: A reappraisal" | Nuvolari, Verspagen & von Tunzelmann | 2011, *Cliometrica* 5(3) | peer-reviewed article | Secondary (reappraises a primary engine census) | QT1 | High | open (Maastricht/EconStor repositories) | Reappraises the Kanefsky & Robey steam-engine census with S-curve diffusion modeling |

### B5. Business/Financial History of Railway Companies, incl. Accounting — serves QT3, QT4.4 — **secondary dispute present**

| Source | Author | Date | Source Type | Primary/Secondary | Claims/Questions Supported | Reliability | Access | Notes |
|---|---|---|---|---|---|---|---|---|
| "The Beginnings of Accounting for Capital Consumption: Disclosure Practices in the British Railway Industry, 1830–55" | A.J. Arnold & S. McCartney | 2002, *Accounting and Business Research* 32(4) | peer-reviewed article | Primary-adjacent (close reading of company accounts) | QT3, QT4.4 | High | **paywalled, no open copy found** | Core source for the depreciation-manipulation question — load-bearing gap |
| "Financial Reporting in the Context of Crisis: Reconsidering the Impact of the 'Mania' on Early Railway Accounting" | S. McCartney & A.J. Arnold | 2002, *European Accounting Review* 11(2) | peer-reviewed article | Secondary | QT3, QT4.4 | High | **paywalled, no open copy found** | Argues railways improved disclosure post-Mania |
| "Accounting for the 'railway mania' of 1845 — A great railway swindle?" | Rob Bryer | 1991, *Accounting, Organizations and Society* 16(5-6) | peer-reviewed article | Secondary | QT3, QT4.4 | Medium-high (influential but contested) | open (Warwick WRAP) | Marxian "manipulation/swindle" framing — opposing pole to Arnold & McCartney's more measured account |
| "Revisiting the British railway 'mania' of 1845–1846 with Marx's theory of crises..." | Rob Bryer | 2024/2025, *Accounting History Review* 35(1) | peer-reviewed article | Secondary | QT3, QT4.4 | Medium | paywalled, no open copy found | Confirms the accounting-manipulation debate remains active |
| "Managerial Failure in early Victorian Britain: Network and capital expansion during the Railway Mania" | Sean McCartney | 2024 (online 2022), *Business History* 66(5) | peer-reviewed article | Secondary | H3, H4 | High | open claimed (project site, unverified) | Finds most Mania-era expansion was by established railways, not new promotions — a managerial failure destroying shareholder value |
| "How Good Was the Profitability of British Railways, 1870–1912?" | Brian Mitchell, David Chambers & Nick Crafts | 2011, *Economic History Review* 64(3) | peer-reviewed article | Primary-adjacent (company-level ROCE reconstruction) | QT3, H4 | High | open (AgEconSearch, Warwick WRAP) | ROCE fell below cost of capital after the mid-1870s — direct H4 (profit-pool migration/decay) evidence. **Caution:** co-author "Brian Mitchell" is not confirmed to be the same person as "B.R. Mitchell" of *British Historical Statistics* (B6) — do not conflate |

**Secondary dispute (not one of the two required Gate 2 pairs, but relevant to QT3/QT4.4):** Bryer's "manipulation/swindle" framing vs. Arnold & McCartney's more measured archival account — currently asymmetric, since Bryer's 1991 piece is open but Arnold & McCartney's core papers are paywalled.

### B6. Official Statistics Compendia — serves all quantitative branches; benchmark deflator source

| Source | Author/Compiler | Date | Source Type | Primary/Secondary | Claims/Questions Supported | Reliability | Access | Notes |
|---|---|---|---|---|---|---|---|---|
| *Abstract of British Historical Statistics* / *British Historical Statistics* | B.R. Mitchell (with Phyllis Deane; later H.G. Jones) | 1962 (later editions to 1988) | official statistics compendium (book) | Secondary compendium of primary/official data | all quantitative UK branches | High | **partial** (Internet Archive borrow-only, not confirmed free download) | Standard reference for 19th-c. UK official series |
| "A Millennium of Macroeconomic Data for the UK" | Bank of England (dataset, v3.1, to 2016) | — | official statistics dataset (spreadsheet) | Secondary/tertiary compilation of primary series | Gate 1 U1/U6 benchmark (consol yields), deflators | High | **open, but the specific direct .xlsx download URL found via search is unverified — bankofengland.co.uk was an explicitly policy-blocked host in this session** | Mirrors on Kaggle and datahub.io are more likely fetchable if BoE's own site remains blocked; contains the long-run consol/gilt yield series needed for the secondary benchmark, plus GDP/price deflators for the whole 1760–1900 window |

### B7. Synthesis Works — orientation only, **explicitly NOT load-bearing evidence**

| Source | Author | Date | Source Type | Primary/Secondary | Claims/Questions Supported | Reliability | Access | Notes |
|---|---|---|---|---|---|---|---|---|
| *Technological Revolutions and Financial Capital: The Dynamics of Bubbles and Golden Ages* | Carlota Pérez | 2002, Edward Elgar | book (non-empirical synthesis) | N/A — framing only | none (orientation only) | Low-for-evidence | book paywalled; companion article open | May suggest framing/hypotheses; must never be cited as evidence for a historical claim (per plan §4 item 7, `governance/OPERATING_PRINCIPLES.md`) |
| *The Visible Hand: The Managerial Revolution in American Business* | Alfred D. Chandler Jr. | 1977, Belknap/Harvard UP | book (narrative/organizational history) | N/A — framing only | none (orientation only) | Low-for-evidence | open (archive.org) | Excellent on managerial-hierarchy history, not designed to answer QT2–QT4's quantitative questions — background framing only |

---

## Part C — Known Gap: Canal-Mania Sources Not Yet Researched

Gate 1 decision U4 requires one bounded Evidence Ledger section on canal-mania (1790s) returns, but no source category for canals was defined in the plan's §3/§4 lists, so Stage A did not task any research pass on canal-specific sources. **This must be filled before Stage C builds that ledger section** — flagging explicitly rather than leaving an implicit gap.

---

## Summary — Evidence Gaps and Access Flags

### Categories with the weakest confirmed access

- **A1 (UK Parliamentary/Regulatory Records)** is the weakest category overall: the comprehensive digitized Parliamentary Papers corpus is paywalled (ProQuest), TNA/Kew company records are mostly in-person/paid-per-item, and railwaysarchive.co.uk's coverage of the specific statistical Railway Returns (as opposed to accident/legislative documents) is unconfirmed.

### Sources confirmed or likely paywalled with no open substitute found (candidates for a Gate 1 U5 paid-access escalation if they prove load-bearing in Stage B/C)

1. *The Economist* Historical Archive (Gale) — no open full-archive substitute.
2. ProQuest UK Parliamentary Papers corpus (1715–2015) — only scattered archive.org volumes substitute.
3. *Historical Statistics of the United States*, Millennial Edition (Cambridge) — only older, less-comprehensive 1949/1960 free editions substitute.
4. TNA/Kew railway company records (RAIL series) — mostly paywalled-per-item or in-person only.
5. ICPSR Study 2896 — institutional-membership gated (Atack's GIS dataset at ICPSR 36353 is a genuine open exception).
6. *The Course of the Exchange* itself — accessible only indirectly through scholarly reconstructions (B2/A2).
7. Richard Grossman (2002), "New Indices of British Equity Prices, 1870–1913" — no open copy found; likely substitutable by the 2019 Campbell/Grossman/Turner splice (B2).
8. Albert Fishlow (1965) — foundational US social-savings text, no open copy found.
9. G.N. von Tunzelmann (1978) — foundational steam-diffusion text, no open copy found; partially substitutable by Crafts (2004) and Nuvolari et al. (2011).
10. A.J. Arnold & S. McCartney's two 2002 accounting-history papers — core sources for the depreciation-manipulation question, no open copies found; Bryer (1991, open) is a partial but asymmetric substitute.

### Does this threaten the project's hard requirements?

- **Failure quota:** largely protected — the single most important US failure source (Poor's Manual) is confirmed open across many public-domain volumes; UK failure evidence (abandoned lines, shareholders ruined by calls) is well-served by the open NBER/Lewin mileage series and Odlyzko's self-archived work. Residual risk: precise panic-year-indexed US receivership statistics were only found via secondary/tertiary restatement in this pass — the open primary backbone (Poor's Manual) exists but its receivership figures have not yet been extracted from specific annual volumes.
- **Required competing-interpretation pairs (Gate 2):** both are fully covered with openly accessible sources on both sides — Railway Mania (Campbell & Turner vs. Odlyzko) and social savings (Fogel/Fishlow vs. Donaldson & Hornbeck).
- **Excess-return benchmark (U1):** well-served — the Campbell/Grossman/Turner (2019) monthly index is an open, single-series candidate spanning the full window; the Bank of England Millennium dataset should supply the consol/gilt secondary benchmark, subject to the access-verification caveat above.
- **Provincial/digitization bias:** genuinely unresolved. The reconstructed British share indices likely skew toward larger, London/dual-listed companies; this should be carried into `REV-HIST-001` as an explicit, stated limitation rather than assumed solved.

### One identity-disambiguation flag for future stages

"Brian Mitchell" (co-author, Mitchell/Chambers/Crafts 2011 railway profitability study) is **not confirmed** to be the same person as "B.R. Mitchell" (compiler of *British Historical Statistics*, B6). Evidence Ledger entries citing either must not conflate them.
