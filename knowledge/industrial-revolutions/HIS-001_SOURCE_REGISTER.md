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

Stage A ("Orientation") built the candidate source landscape. Stage B ("Source Acquisition and Verification") ran in two passes: a first WebSearch-only pass (while the network was blocked) that tightened bibliographic metadata, and — after the environment network allowlist was opened — a second pass that **fetched and read the actual full text** of the Tier 1 load-bearing sources via a local `curl` + `pypdf`/`bs4` toolchain. This file records source metadata, methodology, coverage, page/table locations, and verified access status. **No Evidence Ledger claim rows exist yet, no historical narrative is written, and no Pattern/Mapping/Thesis file has been created** — those are Stage C and beyond.

Sourcing follows the open-access-first rule and paid-access trigger from Gate 1 (decision U5).

## Network-Access Status (updated — proxy now open)

The Stage-B network constraint was **resolved on 2026-07-12**: the User widened the environment's egress allowlist. Current state, confirmed by direct testing:

- **`curl` over HTTPS (via the session proxy): WORKS.** All Tier 1 hosts that previously returned 403 (archive.org, fred.stlouisfed.org, mpra.ub.uni-muenchen.de, www.bankofengland.co.uk, QUB/LSE/Stirling/Warwick/Cornell repositories, api.parliament.uk) now return 200/301.
- **The `WebFetch` tool: STILL 403.** WebFetch routes through a separate (Anthropic-hosted) fetch path that the environment allowlist change did not affect. Verification therefore uses `curl` + local text extraction (`pypdf` for PDFs, `beautifulsoup4` for HTML), not WebFetch. A reusable helper is at `scratchpad/fetch.py`.
- **Two hosts remain blocked by their own anti-bot layer (not the proxy):** `papers.ssrn.com` and `babel.hathitrust.org` (Cloudflare 403). Both have working open substitutes (MPRA/QUB/author-site preprints for SSRN; archive.org public-domain scans for HathiTrust), so neither is a real gap. `orca.cardiff.ac.uk` also Cloudflare-blocks direct hits but was recovered via a Wayback Machine mirror.

### Access-status taxonomy

- **verified-open** — actual full text/dataset (or, for a data page, the page itself) successfully opened and read this stage.
- **verified-partial** — item identity and access tier confirmed, but full text not readable (e.g. Controlled Digital Lending / borrow-only).
- **verified-paywalled** — a real paywall/landing page was reached; no open full text found after a genuine search.
- **access-failed** — a fetch was attempted and failed (server-side anti-bot block); note whether a working substitute exists.
- **not-yet-checked** — no fetch attempted this round (Tier 2, and Stage-A sources not re-tested after the network opened).

Roughly **20 Tier 1 sources are now verified-open by direct full-text read.** Remaining Stage-A sources not re-tested this round are relabeled `not-yet-checked` (their earlier `access-failed` reflected the old block and is now stale).

### How to read the other columns

- **Expected Claims/Questions Supported** references question-tree branches (QT1–QT6) and hypotheses (H1–H5); no Evidence Ledger claim IDs (`C-###`) exist yet.
- **Reliability** is a judgment on the source (methodology, peer review, distance from primary data), never on whether it supports a desired conclusion (per `governance/OPERATING_PRINCIPLES.md`).

---

## Part A — Primary / Near-Primary Sources (plan §3)

### A1. UK Parliamentary and Regulatory Records — serves QT1, QT4

| Source | Author/Compiler | Date | Type | P/S | Supports | Reliability | Access | Notes |
|---|---|---|---|---|---|---|---|---|
| NBER Macrohistory: "Mileage of New Railway Lines Authorized by Parliament for GB" | H.G. Lewin (1936), via NBER/FRED | ~1822–79 | reconstructed series | Near-primary | QT1, QT4 | Medium-high | verified-open (page reachable) | https://fred.stlouisfed.org/series/A0284DGBA374NNBR — **authorized-mileage only**; authorized-vs-built is a derived cross-source comparison |
| The Railways Archive | volunteer project | from 1841 | document repository | Primary | QT1, QT4 | Medium | not-yet-checked | Whether the annual statistical Railway Returns (vs. accident/legislative docs) are digitized here still unconfirmed |
| Digitized UK Parliamentary Papers (scattered) | UK Parliament / archive.org | 1801–1852 | parliamentary record | Primary | QT1 | Low-medium | not-yet-checked | Comprehensive corpus is ProQuest (subscription); archive.org has only scattered volumes |
| Historic Hansard, "Railway Returns and Railway Audit" (HL, 5 Feb 1850) | UK Parliament | 1850 | debate transcript | Primary | QT3 | High | verified-open (page reachable) | https://api.parliament.uk/historic-hansard/... — contemporaneous evidence of the dividend-from-capital/audit controversy |

### A2. Contemporary Security Price Records — serves QT2, QT3, QT4

| Source | Author/Compiler | Date | Type | P/S | Supports | Reliability | Access | Notes |
|---|---|---|---|---|---|---|---|---|
| *The Course of the Exchange* | John Castaing & successors | 1698–19th c. | periodical | Primary | QT2, QT3 | High | not-yet-checked | Not independently accessible; reached only through the reconstructions below |
| Campbell, Grossman & Turner, "Before the Cult of Equity: New Monthly Indices of the British Share Market, 1829–1929" | Campbell (QUB), Grossman (Wesleyan), Turner (QUB) | QUCEH WP19-01, May 2019 (published *European Review of Economic History* 25(4), 2021) | reconstructed index | Near-primary | **Primary U1 benchmark candidate** | High | **verified-open** | See Part C-A. 5,800 securities / 4,500 companies; builds capital-gains, dividend-yield, AND total-return indices; does NOT itself do a survivorship adjustment |
| Campbell, "Deriving the Railway Mania" | **Gareth Campbell (sole)** | 2013, *Financial History Review* 20(1) | reconstructed index | Near-primary | QT2, QT3, QT4 | High | **verified-open** | Sole authorship confirmed from the PDF cover. ~179.6 avg (peak 295) railway securities, Railway Times/LSE, 1843–50; price index; delisting handled as a sensitivity (93.5–98.4%) |
| Campbell & Turner, "'The Greatest Bubble in History'" | Gareth Campbell & John D. Turner | MPRA 21820, 2010 | reconstructed daily index | Near-primary | QT2, QT3, QT4 | Medium-high (WP) | **verified-open** | 591 ordinary shares / 332 companies, daily, LSE, 1843–50; price index; explicit "Delisting scenarios" section (100%/50%/0% of market price) |

### A3. Company Records — serves QT2, QT3, QT4, QT5

| Source | Author/Compiler | Date | Type | P/S | Supports | Reliability | Access | Notes |
|---|---|---|---|---|---|---|---|---|
| TNA (Kew) RAIL series | The National Archives, UK | 19th–20th c. | primary company records | Primary | QT2–QT5 | High | not-yet-checked | Catalogue-only access; in-person/paid-per-item |
| "Development of British Railway Accounting: 1800–1911" | eGrove repository (U. Mississippi) | — | secondary, documents primary practice | Secondary | QT3 | High | not-yet-checked | Confirms 1868 Act first mandated standardized accounts |

### A4. Contemporary Press and Reference Works — serves QT2, QT3, QT4, QT5

| Source | Author/Compiler | Date | Type | P/S | Supports | Reliability | Access | Notes |
|---|---|---|---|---|---|---|---|---|
| *The Economist* Historical Archive | Gale | from 1843 | periodical | Primary | QT2–QT4 | High | verified-paywalled | Gale subscription; no open substitute |
| *The Railway Times* | London periodical | 1837–1863 | periodical | Primary | QT2–QT4 | High | not-yet-checked | Partial run on archive.org; underlying data source for Campbell's indices |
| Bradshaw's Railway Manual, Shareholders' Guide | Bradshaw's office | annual, 1848–1923 | reference work | Primary | QT2, QT3, QT5 | Medium-high | verified-open (later eds.) | archive.org has a ~1869 reprint scan + 1890s–1910s eds. (YNM absent post-1854 merger); **1846/1848–1850 eds. not located** — see Part D |
| Henry Tuck, *The Railway Shareholder's Manual* | Henry Tuck | 1845 & 1847 eds. | reference work | Primary | QT2, QT3, QT4; **Part D cash-flow input** | Medium-high | **verified-open** | Both eds. read on archive.org (`railwaysharehol02tuckgoog` 1845; `railwaysharehol00tuckgoog` 1847). Contain paid-up-capital snapshots, half-yearly dividend rates, and (1845 ed.) an 1839–44 YNM price series — but **no dated call schedule** (Part D) |

### A5. Failure Records — serves QT4, QT5 (US comparative capped to ≤2 panics per Gate 1 U3)

| Source | Author/Compiler | Date | Type | P/S | Supports | Reliability | Access | Notes |
|---|---|---|---|---|---|---|---|---|
| Poor's Manual of the Railroads of the United States | Henry Varnum Poor | annual, 1868–1917 | statistical compendium | Near-primary | QT5, US comparative | High | **verified-open** | Read `poorsmanualrail00poorgoog` (~1899/1900) and `poorsmanualofrai18newyuoft` (~1885). The ~1899/1900 vol. has a receivership table (see Part C-F); per-company receivership status also in individual entries |
| Odlyzko, "The Collapse of the Railway Mania … Robert Lucas Nash …" | Andrew Odlyzko | 2011, *Accounting History Review* 21(3) | secondary, recovers primary analyst | Secondary/near-primary | QT4 (bust, calls) | High | **verified-open** | Read (umn.edu `mania02.pdf`). Contains capital-invested/authorized totals and a "~10%" early-1848 price-decline figure, but **NO aggregate investor-capital-loss statistic** (Part C-F) |
| Albro Martin, "Railroads and the Equity Receivership" | Albro Martin | 1974, *Journal of Economic History* 34(3), 685–709 | peer-reviewed | Secondary | QT4, QT5 (US) | High | verified-paywalled | Exists (Cambridge Core/JSTOR/RePEc); no open full text found |
| Peter Tufano, "Business Failure, Judicial Intervention … U.S. Railroads …" | Peter Tufano | 1997, *Business History Review* 71(1), 1–40 | peer-reviewed | Secondary | QT4, QT5 (US) | High | verified-paywalled | Exists (Cambridge Core); no open full text found |
| Stephen J. Lubben, "Railroad Receiverships and Modern Bankruptcy Theory" | Stephen J. Lubben | 2004, *Cornell Law Review* 89(6) | peer-reviewed | Secondary | QT4, QT5 (US) | High | **verified-open** | Read full text at `scholarship.law.cornell.edu`. ~half of railroads went through a receivership 1890–WWI; prior-receivership firms >2.5× more likely to fail again |

**UK abandonment scale (still not a sourced ledger claim; corroborated but needs formal C-### sourcing in Stage C):** ~60% of 1844–48 authorized mileage completed by 1852. **The aggregate UK investor-capital-loss figure remains a genuine gap** — not found in Odlyzko's full text (Part C-F).

### A6. US Quantitative Compendia — serves QT5, QT6 (US comparative, capped per U3)

| Source | Author/Compiler | Date | Type | P/S | Supports | Reliability | Access | Notes |
|---|---|---|---|---|---|---|---|---|
| ICPSR Study 2896 | Michael R. Haines | — | statistical compendium | Near-primary | QT5 | High | not-yet-checked | Institutional-membership gated |
| Cambridge Group GB railway GIS (from M. Cobb atlas); GBHGIS (Portsmouth) | Cambridge Group / GBHGIS | 1831 census years+ | GIS dataset | Near-primary | QT1, QT5 | High | not-yet-checked | **Corrected**: replaces the Stage-A "Atack" entry (Atack's GIS is US-Midwest, not GB) |
| Historical Statistics of the US — 1949/1960 (free) vs. 2006 Millennial (paywalled) | Census; Carter et al. (2006) | 1949/1960/2006 | official compendium | Primary/near-primary | QT5, QT6 | High | not-yet-checked | Free older eds. substitute for the paywalled Millennial |

---

## Part B — Academic / Institutional Sources (plan §4)

### B1. Railway Mania Financial Economics — QT4, H3, H5 — **Gate 2 pair confirmed genuine, citation-level (Part C-G)**

| Source | Author | Date | Type | Supports | Reliability | Access | Notes |
|---|---|---|---|---|---|---|---|
| "Dispelling the Myth of the Naive Investor …" | Campbell & Turner | 2012, *Business History Review* 86(1) | peer-reviewed | QT4, H3, H5; Part D | High | **verified-open** | Investor-level subscription data (1845/46 Parliamentary lists), **not** company-level call schedules (Part D) |
| "Myopic Rationality in a Mania" | **Gareth Campbell (sole)** | 2012, *Explorations in Economic History* 49(1) | peer-reviewed | QT4, H5 | High | **verified-open** | Sole authorship confirmed. "Rational but myopic" pole of the dispute |
| "'The Greatest Bubble in History'" | Campbell & Turner | MPRA 21820, 2010 | working paper | QT2–QT4 | Medium-high | **verified-open** | Cross-listed A2 |
| "Cross-Section of a 'Bubble'" | **Gareth Campbell (sole)** | MPRA 23580, 2010 | working paper | QT2–QT4 | Medium-high | verified-open (landing) | Sole authorship confirmed; predecessor draft of "Myopic Rationality" |
| "Deriving the Railway Mania" | **Gareth Campbell (sole)** | 2013, *Financial History Review* 20(1) | peer-reviewed | QT4 | High | **verified-open** | Cross-listed A2 |
| "The role of the media in a bubble" | Campbell, Turner & Walker | 2012, *Explorations in Economic History* 49(4) | peer-reviewed | QT4 | High | not-yet-checked | Not re-tested this round |
| "Collective Hallucinations and Inefficient Markets …" | Andrew Odlyzko | 2010, *B.E. J. Econ. Analysis & Policy* 10(1) | peer-reviewed | QT4, H3, H5 | Medium-high | **verified-open** | **Opposing pole**; directly rebuts Campbell by name (fn 107) — Part C-G |
| "Bubbles, Gullibility …" | Andrew Odlyzko | 2010, *First Monday* 15(9) | peer-reviewed (OA) | QT4 | High | not-yet-checked | Not re-tested this round |
| "The Collapse of the Railway Mania … Nash …" | Andrew Odlyzko | 2011, *Accounting History Review* 21(3) | peer-reviewed | QT4 | High | **verified-open** | Cross-listed A5 |

### B2. Long-Run UK Asset Returns — Gate 1 U1/U6 benchmark

| Source | Author | Date | Type | Supports | Reliability | Access | Notes |
|---|---|---|---|---|---|---|---|
| "Rule Britannia! British Stock Market Returns, 1825–1870" | Acheson, Hickson, Turner & Ye | 2009, *JEH* 69(4) | peer-reviewed | QT2, QT3, U1 (pre-1870) | High | **verified-open** | **LSE-only** (240 securities, ~£285m mkt cap in 1870). **This is where the Dec-1870-IMM survivorship check + buy-and-hold/−100% bounds actually live** (Part G correction) |
| "New Indices of British Equity Prices, 1870–1913" | Richard S. Grossman | 2002, *JEH* 62(1) | peer-reviewed | U1 (post-1870) | High | verified-paywalled | No open copy; substitutable by the 2019 CGT splice below |
| "Before the Cult of Equity … 1829–1929" | Campbell, Grossman & Turner | QUCEH WP19-01, 2019 / EREH 2021 | peer-reviewed | **Primary U1 benchmark** | High | **verified-open** | Cross-listed A2; see Part C-A for methodology + the open London-vs-provincial ambiguity |
| "What Moved Share Prices in the 19th-C London Stock Market?" | Campbell, Quinn, Turner & Ye | 2018, *Economic History Review* | peer-reviewed | QT2, QT3 | High | not-yet-checked | Not re-tested this round |
| "Stocks for the Long Run … 1869–1929" | Richard S. Grossman | Wesleyan WP 2017-004 | working paper | U1 (alt. splice) | Medium-high | not-yet-checked | Not re-tested this round |

### B3. Social Savings / Counterfactual — QT5, H2 — **Gate 2 pair confirmed genuine (Part C-H)**

| Source | Author | Date | Type | Supports | Reliability | Access | Notes |
|---|---|---|---|---|---|---|---|
| *Railroads and American Economic Growth* | Robert W. Fogel | 1964, Johns Hopkins UP | book | QT5, H2 | High | **verified-partial** | archive.org = Controlled Digital Lending (borrow-only). "<5% GNP" claim confirmed only via Donaldson & Hornbeck's reproduction (2.7% actual / 5.35% upper bound), not primary text |
| *American Railroads … Ante-bellum Economy* | Albert Fishlow | 1965, Harvard UP | book | QT5, H2 | High | verified-paywalled | No open copy; not strictly load-bearing (Fogel already anchors this camp) |
| *Railways and Economic Growth in England and Wales, 1840–70* | G.R. Hawke | 1970, Clarendon | book | QT5, H2 (UK) | High | not-yet-checked | Hawke vs. Leunig = refinement, not a 2nd pair (Part C-H) |
| "Time is Money … Victorian British Railways" | Tim Leunig | 2006, *JEH* 66(3) | peer-reviewed | QT5, H2 | High | **verified-open** | Self-describes as "revises and extends Hawke" — successive refinement |
| "Social savings" (survey) | Tim Leunig | 2010, *J. Econ. Surveys* 24(5) | peer-reviewed survey | QT5, H2 | High | not-yet-checked | Not re-tested this round |
| "Railroads and American Economic Growth: A 'Market Access' Approach" | Donaldson & Hornbeck | 2016, *QJE* 131(2) | peer-reviewed | QT5, H2 | High | **verified-open** | **Opposing pole**; engages Fogel by name (§II). **Correction: result is "moderately larger," 3.22% of GNP vs Fogel's 2.7% — NOT "more than double"** (Part C-H, Part G) |
| "The Transport Revolution in Industrializing Britain: A Survey" | Dan Bogart | WP ~2013 | working paper | QT1, QT5 | Medium-high | not-yet-checked | Cross-listed Part E (canals) |

### B4. Steam Power / GPT Diffusion — QT1, QT5.3

| Source | Author | Date | Type | Supports | Reliability | Access | Notes |
|---|---|---|---|---|---|---|---|
| *Steam Power and British Industrialization to 1860* | G.N. von Tunzelmann | 1978, Oxford UP | book | QT1, QT5.3 | High | not-yet-checked | An archive.org listing exists (`steampowerbritis0000vont`); free-vs-CDL not confirmed |
| "Steam as a General Purpose Technology" | Nicholas Crafts | 2004, *Economic Journal* 114(495) (LSE WP 75/03) | peer-reviewed | QT1, QT5.3, H5 | High | **verified-open** | Read (LSE WP). Complementary capital = high-pressure boilers/Lancashire boiler; ~80-yr lag after Watt; near-zero growth contribution pre-1830 (Part C-I) |
| "The early diffusion of the steam engine in Britain, 1700–1800" | Nuvolari, Verspagen & von Tunzelmann | 2011, *Cliometrica* 5(3) | peer-reviewed | QT1 | High | not-yet-checked | Covers 1700–1800 only — Bottomley (below) picks up 1800–70 |
| "Stationary steam power in the UK, 1800–70: An empirical reassessment" | Sean Bottomley | 2024/25, *Economic History Review* 78(3), 825–848 | peer-reviewed | QT1, QT5.3 (fills 1800–70) | High | **verified-open** (via Wayback) | Cardiff ORCA Cloudflare-blocks direct; read via Wayback mirror. Argues steam adoption far greater than the conventional (von-Tunzelmann-descended) view; "indispensable sustentative factor" |

### B5. Business/Financial History incl. Accounting — QT3, QT4.4 — two secondary disputes

| Source | Author | Date | Type | Supports | Reliability | Access | Notes |
|---|---|---|---|---|---|---|---|
| "The Beginnings of Accounting for Capital Consumption …" | A.J. Arnold & S. McCartney | 2002, *Accounting and Business Research* 32(4) | peer-reviewed | QT3, QT4.4 | High | verified-paywalled | No open copy |
| "Financial Reporting in the Context of Crisis …" | McCartney & Arnold | 2002, *European Accounting Review* 11(2) | peer-reviewed | QT3, QT4.4 | High | not-yet-checked | Not re-tested this round |
| "Were they ever 'productive to the capitalist'? Rates of return … 1830–55" | A.J. Arnold & S. McCartney | 2004, *J. European Economic History* 33, 383–410 | peer-reviewed | QT3, QT4.4, H4 (**fills pre-1870 gap**) | High | verified-paywalled | **No open full text found this round** (checked UEL Worktribe, ResearchGate, railwaymania.co.uk). A secondary "7.1% gross profit 1855" paraphrase is **unverified** — do not cite |
| "Accounting for the 'railway mania' of 1845 — a great railway swindle?" | Rob Bryer | 1991, *AOS* 16(5-6) | peer-reviewed | QT3, QT4.4 | Medium-high | not-yet-checked | Open at Warwick WRAP (Stage A); not re-tested |
| McCartney (& Arnold?), "Managerial Failure in early Victorian Britain … Railway Mania" | Sean McCartney (co-author attribution unresolved — Part G) | 2022 online/2024, *Business History* 66(5) | peer-reviewed | H3, H4; Part D | High | verified-open (project-site copy read by agent) | Reports YNM return-to-equity **10.1% pre-Mania network vs −0.3% Mania-era construction**; disputes Campbell & Turner (2015) |
| "Managerial failure in mid-Victorian Britain? … promotion boom" | Campbell & Turner | 2015, *Business History* 57(8) | peer-reviewed | H3, H4 | High | not-yet-checked | The "rational/optimal expansion" pole; McCartney disputes it |
| "How Good Was the Profitability of British Railways, 1870–1912?" | **B.R. Mitchell**, David Chambers & Nicholas Crafts | 2011, *Economic History Review* 64(3) (Warwick WP 859, 2009) | peer-reviewed | QT3, H4 | High | **verified-open** | Read (ageconsearch WP). **"Brian Mitchell" = B.R. Mitchell RESOLVED via internal self-citation chain** (Part C-E, Part G). ROCE = net traffic revenue / paid-up capital, 15 major companies |

**Secondary disputes:** (1) Bryer "swindle" vs. Arnold & McCartney measured account (asymmetric access). (2) Campbell & Turner 2015 "optimal expansion" vs. McCartney 2024 "managerial failure" (YNM case) — documented disagreement.

### B6. Official Statistics Compendia

| Source | Author/Compiler | Date | Type | Supports | Reliability | Access | Notes |
|---|---|---|---|---|---|---|---|
| *Abstract of British Historical Statistics* / *British Historical Statistics* | B.R. Mitchell (Brian Redman Mitchell; Deane; Jones) | 1962–1988 | official compendium | all UK quantitative | High | not-yet-checked | Same person as the Mitchell/Chambers/Crafts co-author (Part G) |
| "A Millennium of Macroeconomic Data for the UK" | Bank of England, v3.1 | to 2016 | official dataset | U1/U6 (consol yields, deflators) | High | verified-open (page reachable) | bankofengland.co.uk now reachable (curl 200); dataset content not yet deep-read |

### B7. Synthesis Works — orientation only, **NOT load-bearing evidence**

| Source | Author | Date | Type | Supports | Reliability | Access | Notes |
|---|---|---|---|---|---|---|---|
| *Technological Revolutions and Financial Capital* | Carlota Pérez | 2002, Edward Elgar | synthesis | framing only | Low-for-evidence | not-yet-checked | Never citable as evidence |
| *The Visible Hand* | Alfred D. Chandler Jr. | 1977, Harvard UP | narrative history | framing only | Low-for-evidence | not-yet-checked | Framing only |

---

## Part C — Tier 1 Full-Text Verification Findings (Stage B, second pass)

All items below were read from actual full text via `curl` + local extraction. Findings stay at the level of source scope/methodology/coverage/locations — no claim extraction (Stage C).

**Task A — UK broad equity benchmark (verified-open).** "Before the Cult of Equity" (QUCEH WP19-01): 1,000,000+ security-month observations, ~5,800 securities / ~4,500 companies, from Course of the Exchange (1829–68, London) + Investor's Monthly Manual (1869–1929). Builds **three** indices — capital gains, dividend yield, total return (return formula p.11). **Does NOT perform a survivorship adjustment** (explicit, p.11: "we make no attempt to examine the gains or losses from newly listing, delisting, or merging"). London-vs-provincial: for the *coverage-benchmarking* exercise it restricts to securities "chiefly traded in London (i.e., excluding securities listed only on provincial markets)" (p.7), but **it is genuinely ambiguous from the full text whether that restriction also applies to the main return indices** — flagged unresolved.

**Task B — railway price/return series (verified-open).** "Deriving the Railway Mania" (Campbell, sole): ~179.6 avg railway securities (peak 295), Railway Times/LSE, 1843–50, price index; delisting handled as a sensitivity ("All Railways rose by between 93.5 per cent and 98.4 per cent depending on how the delisting of shares is dealt with"; peak-to-trough −66.1% vs −69.9% under two delisting scenarios). "Greatest Bubble" (Campbell & Turner): 591 ordinary shares / 332 companies, daily, LSE, 1843–50; price index; explicit "Delisting scenarios" (100%/50%/0% of market price → 1850 levels 57.5/60.2/62.7% below peak). Both are price (not total-return) indices; dividends enter only as model inputs.

**Task C — cash-flow feasibility (verified-open sources; see Part D).** "Dispelling the Myth" holds **investor-level total-subscribed-capital** data (1845/46 Parliamentary subscription lists), **not** company-level call/installment schedules. A YNM cash-flow reconstruction is only partially supported by located sources — genuine gap (Part D).

**Task D — capital formation/overbuild.** FRED/NBER series = authorized mileage only (page reachable). A direct "capital authorized vs. capital called" series was not verified this round; likely in Mitchell's *Abstract of British Historical Statistics* (not yet read).

**Task E — operating vs. shareholder returns (verified-open).** Mitchell, Chambers & Crafts (Warwick WP 859): ROCE = net traffic revenue (Railway Returns) / paid-up capital (half-yearly accounts), 15 major companies (~¾ of route miles), plus a cumulated-capital-expenditure denominator. Discusses the general no-separate-depreciation convention across 1870–1912 but **does not** specifically cover the pre-1868 dividends-from-capital pathology (that's Arnold & McCartney / Odlyzko territory) — do not over-read it.

**Task F — failure/post-boom (verified-open).** Odlyzko "Collapse …": gives capital-invested (£44m peak 1847 ≈ 8% GDP; Nash: 42 lines invested £172m of £268m authorized by end-1848) and "~10%" early-1848 price decline — but **no computed aggregate investor-capital-loss figure**. Gap confirmed open. Poor's Manual (~1899/1900): receivership table 1884–99 (521 corporations, 78,582 miles, $5.35bn capitalization; 1893 alone: 119 companies, 27,883 miles, $835.8m share capital, $1.16bn funded debt). Lubben 2004 (Cornell, verified-open): ~half of railroads in receivership 1890–WWI.

**Task G — Mania dispute genuineness (verified-open both sides): GENUINE, CITATION-LEVEL.** Odlyzko fn 107 quotes and directly rebuts Campbell; Campbell's intro names Odlyzko (2010) as arguing "market inefficiency." Mechanism dispute is explicit: Odlyzko = predictable bust investors ignored (collective hallucination / inefficiency); Campbell = rational-but-myopic pricing consistent with dividend fundamentals.

**Task H — social-value dispute genuineness (verified-open): GENUINE, CITATION-LEVEL, but self-framed as extension.** Donaldson & Hornbeck engage Fogel by name (§II, "U.S. Railroads and 'Social Saving' Estimates"), position their GE market-access method as "a natural extension of Fogel's intuition," and report a **3.22% of GNP** loss — "moderately larger" than Fogel's 2.7% (upper bound 5.35%), **not "more than double."** Hawke vs. Leunig = successive refinement of one method (Leunig: "revises and extends Hawke").

**Task I — steam diffusion (verified-open).** Crafts (2004): complementary capital = high-pressure boilers (the early-1840s Lancashire boiler as key enabler); steam near-zero growth contribution pre-1830, ~80-year lag after Watt to major productivity effect. Bottomley (2024/25, via Wayback): newly-compiled Suffolk power census argues steam adoption was far greater than the econometric consensus held, "indispensable sustentative factor"; covers 1800–70 (fills the Nuvolari et al. 1700–1800 gap).

---

## Part D — Cash-Flow Reconstruction Candidate (for Stage C; not performed here)

**Candidate: York and North Midland Railway (YNM), George Hudson's flagship.** Rationale unchanged (rich documentation; McCartney's case study reports **10.1% pre-Mania vs −0.3% Mania-era** return-to-equity — the operating-vs-boom-capital distinction Gate 1 U2 needs).

**Verified this round:**
- "Dispelling the Myth of the Naive Investor" (Campbell & Turner 2012, verified-open) is **investor-level subscription data, not company call schedules** — cannot by itself support an IRR-style reconstruction.
- Henry Tuck's *Railway Shareholder's Manual* (1845 & 1847, verified-open on archive.org) **does** contain: paid-up capital by share class, a cumulative "amount raised by calls to 30 June 1846" total, half-yearly dividend-per-share, and (1845 ed.) an 1839–44 YNM share-price/premium series. It does **not** contain a dated, per-call schedule.

**Genuine remaining gap:** a call-by-call schedule (dates + amounts) and continuous 1845–50 half-yearly coverage. The 1846/1848/1849/1850 Tuck's/Bradshaw's editions were not located on archive.org; closing this would need HathiTrust (currently anti-bot-blocked), Railway Times/Herapath's call notices, or YNM's own half-yearly reports/minute books (archival, not confirmed accessible). **A partial-resolution reconstruction (inferring calls from paid-up-capital changes across editions) is feasible if the missing editions are located.** No reconstruction performed (Stage C).

---

## Part E — Tier 3: Canal Mania Bounded Comparison

Deliberately minimal (Gate 1 U4). Purpose: test whether infrastructure speculation predated railways and whether financing mechanisms were railway-specific — not a canal chapter, not a Pattern-promotion basis.

| Source | Author | Date | Type | Access | Role |
|---|---|---|---|---|---|
| "Collective Hallucinations …" | Andrew Odlyzko | 2010 | working paper | verified-open | **Double duty** (cross-listed B1): reviews financial statements of seven major English canals 1770s–1850s as a comparative baseline |
| "The Transport Revolution in Industrializing Britain: A Survey" | Dan Bogart | WP ~2013 | working paper | not-yet-checked | Cross-listed B3; comparative turnpike/canal/railway context |
| *The Finance of Canal Building in Eighteenth-Century England* | J.R. Ward | 1974, Oxford UP | monograph | not-yet-checked | Nearest near-primary canal-finance reconstruction; likely physical/OOP only |

---

## Part F — Provincial-Market Coverage Question

**Verdict (grounded in full text read this round): partially-resolved.**

- Both Railway Mania price series (Campbell 2013; Campbell & Turner 2010) are **explicitly London-Stock-Exchange-only** (Railway Times coverage); Campbell 2013 explicitly admits the London-listing count "underestimates" promotion because some railways "chose to only list on regional exchanges."
- "Rule Britannia!" (Acheson et al. 2009) is **explicitly London-only** (Course of the Exchange; 240 securities / £285m in 1870), authors attributing the coverage gap "largely" to absent foreign railways.
- The one paper quantifying provincial-only trading (Campbell, Rogers & Turner, QUCEH WP16-03, **confirmed authors**) covers **1869–1929 only** — 19+ years after the Mania. Its earliest year (1870) shows provincial-only-traded securities were railway-dominated (61%) and ~⅓ of all UK securities, and it flags its own counts as understated. Suggestive, not direct evidence for 1843–50.
- "Before the Cult of Equity" leaves genuinely ambiguous whether its main 1869–1929 indices include provincial-only IMM securities.

**Net:** the *existence and direction* of a provincial-underrepresentation limitation is well-documented in primary methodology text; its *magnitude for 1843–50 specifically* is unquantified in any full-text source examined. Carry into `REV-HIST-001` as an explicit stated limitation. **Not** "resolved-immaterial"; **not** yet "resolved-material" (magnitude unquantified).

---

## Part G — Bibliographic Corrections Log

**From Stage B pass 1 (search), reconfirmed by full text this round:**
1. "Deriving the Railway Mania" (2013) — **Gareth Campbell sole author** (confirmed from PDF cover), not Campbell & Turner.
2. "Myopic Rationality in a Mania" (2012) — **Gareth Campbell sole author** (confirmed from PDF byline).
3. "Cross-Section of a 'Bubble'" (MPRA 23580) — **Gareth Campbell sole author** (confirmed from MPRA landing).
4. Provincial-markets paper = **Campbell, Rogers & Turner** (QUCEH WP16-03, 1869–1929) — confirmed from PDF; NOT "Acheson, Hickson, Turner & Ye" (that group wrote the London-only *Rule Britannia!*).
5. "Atack GIS dataset" is **US-Midwest, not Great Britain** — replaced with Cambridge Group / GBHGIS (A6).

**New / corrected this round (full-text-grounded):**
6. **The Dec-1870-IMM survivorship check + buy-and-hold/−100% adjustment belongs to "Rule Britannia!" (Acheson et al. 2009), NOT "Before the Cult of Equity."** Stage B pass 1 mis-attributed this methodology; "Before the Cult of Equity" explicitly does *no* survivorship adjustment. Corrected in A2/B2.
7. **Donaldson & Hornbeck result: "moderately larger," 3.22% of GNP vs Fogel's 2.7% (upper bound 5.35%) — NOT "more than double."** Stage B pass 1's "more than double" was wrong; corrected in B3/Part C-H.
8. **"Brian Mitchell" (Mitchell/Chambers/Crafts 2011) = B.R. Mitchell** (compiler of *British Historical Statistics*): RESOLVED as the same person, via the paper's internal self-citation chain (1962/3 Cambridge DAE extraction for Phyllis Deane's project → "Mitchell, B.R., 'The coming of the railway…', JEH 1964"). Reverses Stage A's "not confirmed different" caution. Established by self-citation, not an explicit biographical statement.
9. "Managerial Failure in early Victorian Britain" (*Business History* 66(5)) — **co-authorship still unresolved** (agents disagree: McCartney solo vs. McCartney & Arnold). Confirm before Stage C citation.
10. Fogel (1964) on archive.org is **Controlled Digital Lending / borrow-only** — its "<5% GNP" claim is confirmed only via Donaldson & Hornbeck's reproduction, not primary text.

---

## Stage B Completion Summary (updated after full-text pass)

### A. Access Summary

| Status | Count | Notes |
|---|---|---|
| verified-open | ~20 | Full text (or data page) opened and read this stage — the Tier 1 load-bearing set |
| verified-partial | 1 | Fogel (1964), CDL borrow-only |
| verified-paywalled | ~6 | Fishlow 1965; Arnold & McCartney 2004 & the two 2002 papers; Martin 1974; Tufano 1997; Grossman 2002; *Economist* archive — no open full text found |
| access-failed | 2 | `papers.ssrn.com`, `babel.hathitrust.org` (server-side Cloudflare; both have working open substitutes) |
| not-yet-checked | remainder | Tier 2 (not researched, per budget guardrail) + Stage-A sources not re-tested after the network opened |

### B. Tier 1 Coverage Matrix (post-full-text)

| Requirement | Status | Basis |
|---|---|---|
| A. UK broad equity benchmark | **Sufficient for Stage C** (one caveat) | CGT 2019 read: universe, 3-index construction confirmed; provincial-inclusion of the main index remains ambiguous |
| B. Railway price/return series | **Sufficient for Stage C** | Both indices read; sample, price-only nature, and explicit delisting sensitivity confirmed |
| C. Call-based cash-flow | Partial | "Dispelling the Myth" has no call data; Tuck's gives partial YNM inputs; dated call schedule is a genuine gap (Part D) |
| D. Capital formation/overbuild | Partial | Authorized-mileage confirmed; capital-called series not yet read (likely in Mitchell's Abstract) |
| E. Operating vs. shareholder returns | **Sufficient for Stage C** | Mitchell/Chambers/Crafts read (method, 15 companies); Arnold & McCartney 2004 (pre-1870) paywalled |
| F. Failure/post-boom | **Sufficient for Stage C** (one gap) | Poor's Manual + Lubben read; UK aggregate capital-loss figure remains a genuine gap |
| G. Mania interpretations | **Sufficient — confirmed genuine, citation-level** | Both papers read; direct mutual rebuttal confirmed |
| H. Social-value interpretations | **Sufficient — confirmed genuine, citation-level** | Donaldson & Hornbeck read; Fogel figure corrected; Hawke/Leunig = refinement |
| I. Steam diffusion/timing | **Sufficient for Stage C** | Crafts + Bottomley read; 1800–70 gap now covered |

No requirement is Blocked.

### C. Load-Bearing Gaps (genuine, unresolved)

1. **Aggregate UK investor-capital-loss figure** for the Mania bust — confirmed absent from Odlyzko's full text; no sourced figure yet.
2. **YNM dated call schedule + continuous 1845–50 coverage** — Tuck's 1845/1847 give partial inputs; missing editions block a full cash-flow reconstruction.
3. **"Before the Cult of Equity" main-index provincial inclusion** — ambiguous even after full-text read.
4. **Provincial-underrepresentation magnitude for 1843–50** — direction documented, magnitude unquantified in any full-text source.
5. **Arnold & McCartney (2004)** pre-1870 rates-of-return paper — no open full text (paywalled).
6. **"Managerial Failure" (Business History 66(5)) co-authorship** — unresolved (solo vs. with Arnold).

### D. Paid-Access Escalation

**None triggered.** Applying the four-condition test: the paywalled items (Fishlow, Arnold & McCartney, Martin, Tufano, Grossman) each either have an open substitute anchoring the same Gate 2 requirement or are not strictly required for a hard minimum. Since the network is now open and ~20 load-bearing sources are verified-open, no source currently meets all four escalation conditions.

### E. Provincial-Market Conclusion

**Partially-resolved** (full reasoning in Part F): direction documented from primary methodology text; magnitude for 1843–50 unquantified.

### F. Cash-Flow Reconstruction Candidate

**York and North Midland Railway** (Part D). Partial inputs verified-open (Tuck's 1845/1847); dated call schedule is a genuine gap. Reconstruction deferred to Stage C.

### G. Network-Access Result

**Resolved at the proxy/allowlist level** (User widened the environment allowlist): `curl`-over-HTTPS now reaches all Tier 1 hosts; ~20 sources verified-open by direct full-text read via `curl` + `pypdf`/`bs4`. The **`WebFetch` tool itself is still 403** (separate network path). Two hosts (`papers.ssrn.com`, `babel.hathitrust.org`) remain blocked by their own Cloudflare anti-bot layer, both with working open substitutes.
