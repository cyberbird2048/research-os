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

Stage A ("Orientation") built the candidate source landscape below. Stage B ("Source Acquisition and Verification") tightened bibliographic metadata, checked for genuine (not title-level) disagreement between competing interpretations, identified a cash-flow reconstruction candidate, and — critically — **directly tested whether this environment can actually open external sources**. It cannot (see next section). **No Evidence Ledger claim rows exist yet, no historical narrative is written, and no Pattern/Mapping/Thesis file has been created** — those remain Stage C and beyond.

Sourcing follows the open-access-first rule and paid-access trigger established at Gate 1 (decision U5; `governance/HIS-001_GATE_1_REVIEW.md`, plan §5, §12).

## Network-Access Test Result (Stage B, confirmed directly)

Before touching research content, direct network capability was tested in this session — not inferred from subagent reports alone:

| Test category | URL tested | Tool | Result |
|---|---|---|---|
| Official/institutional page | `bankofengland.co.uk/statistics/research-datasets` | curl (via session HTTPS_PROXY) | `403` — CONNECT tunnel rejected |
| Official/institutional page | same URL | WebFetch tool | `403 Forbidden` |
| Academic working paper PDF | `mpra.ub.uni-muenchen.de/.../MPRA_paper_21820.pdf` | curl | `403` — CONNECT tunnel rejected |
| Academic working paper PDF | same URL | WebFetch tool | `403 Forbidden` |
| Downloadable book/PDF | `archive.org/details/railroadsamerica00foge` | curl | `403` — CONNECT tunnel rejected |
| Downloadable book/PDF | same URL | WebFetch tool | `403 Forbidden` |
| Dataset/data page | `fred.stlouisfed.org/series/A0284DGBA374NNBR` | curl | `403` — CONNECT tunnel rejected |
| Dataset/data page | same URL | WebFetch tool | `403 Forbidden` |

**Result: 4/4 categories blocked, in both a raw HTTP client and the WebFetch tool itself.** The session's agent-proxy status endpoint logs these as explicit `connect_rejected` / "gateway answered 403 to CONNECT (policy denial or upstream failure)" entries — an organizational egress policy denial, not a client misconfiguration, TLS problem, or per-host issue (the four hosts span a UK central bank, a German university repository, a US nonprofit digital library, and a US Federal Reserve Bank — about as diverse a sample as is available). Per this environment's own proxy guidance: report the blocked host, do not retry or route around it.

**Consequence:** true "full-text/dataset opened and read" verification is not achievable in this session for any external source. `WebSearch` remains functional (confirmed working throughout Stage A and Stage B) and can surface abstract-level content beyond bare titles, but this is explicitly **not** full-text verification. Both Stage B research passes independently hit this same wall across dozens of additional hosts (SSRN, NBER, RePEc, QUB, Wikipedia, Warwick WRAP, LSE, Cornell, Cardiff ORCA, etc.), consistent with a categorical, session-wide block rather than noise.

**Recommendation:** escalate this to the User as an infrastructure question distinct from any single paid-access request (see Paid-Access Escalation section below) — without working egress, no source in this register can ever reach `verified-open`/`verified-partial`/`verified-paywalled` status in this environment, which will also block Stage C evidence-ledger construction from citing exact pages/tables/figures with confidence.

### Access-status taxonomy (this file uses these five values only)

- **verified-open** — actual full text/dataset was successfully opened in this session. *(Not achieved for any source this round — see above.)*
- **verified-partial** — actual abstract/paywall page was successfully opened, confirming partial access. *(Not achieved for any source this round.)*
- **verified-paywalled** — actual paywall/login page was successfully reached and observed. *(Not achieved for any source this round — the block happens before reaching any destination, so a paywall itself was never observed.)*
- **access-failed** — verification was attempted (via this session's confirmed categorical network block) and failed for infrastructure reasons, not because the source doesn't exist or isn't real.
- **not-yet-checked** — no verification attempt made this round (applies to the deliberately-deferred Tier 2 category; see Research-Budget Guardrail below).

**Given the confirmed categorical block, essentially every source below carries `access-failed`.** This is not a defect in the source landscape — the sources are real, and Stage A/B search-based reconnaissance (titles, authors, venues, abstracts) remains valid — it is a statement about what this session can confirm about *accessibility*.

### How to read the other columns

- **Expected Claims/Questions Supported** — references question-tree branches (QT1–QT6) and hypotheses (H1–H5), since no Evidence Ledger claim IDs (`C-###`) exist yet.
- **Reliability** — a judgment on the source itself (methodology, peer-review status, distance from primary data), never on whether it supports a desired conclusion, per `governance/OPERATING_PRINCIPLES.md`.

---

## Part A — Primary / Near-Primary Sources (plan §3)

### A1. UK Parliamentary and Regulatory Records — serves QT1, QT4

| Source | Author/Compiler | Date | Source Type | Primary/Secondary | Claims/Questions Supported | Reliability | Access | Notes |
|---|---|---|---|---|---|---|---|---|
| NBER Macrohistory series: "Mileage of New Railway Lines Authorized by Parliament for Great Britain" | H.G. Lewin, *Early British Railways* / *The Railway Mania and Its Aftermath, 1845–1852* (1936), via NBER Macrohistory Database | annual ~1822–52, 1847–79 | reconstructed statistical series | Near-primary | QT1, QT4 | Medium-high | access-failed | https://fred.stlouisfed.org/series/A0284DGBA374NNBR — **Stage B confirms (bibliographic cross-check):** this is an *authorized-mileage-only* series; there is no paired "actually built" series bundled with it — any authorized-vs-built comparison is a **derived** cross-source comparison, not one dataset's internal distinction |
| The Railways Archive (railwaysarchive.co.uk) | independent volunteer digitization project | from 1841 | primary-document repository | Primary (scanned items) | QT1, QT4 | Medium | access-failed | Whether the specific annual statistical Railway Returns (vs. accident/legislative documents) are digitized here remains unconfirmed |
| Digitized UK Parliamentary Papers (scattered volumes) | UK Parliament / archive.org | 1801–1852 (partial) | parliamentary record | Primary | QT1 | Low-medium | access-failed | Comprehensive corpus is ProQuest (institutional-subscription); archive.org has only scattered volumes — structural gap, unchanged from Stage A |

**Category flag:** still the weakest category. No Stage B improvement — not tasked this round given Tier 1 priority (per the research-budget guardrail).

### A2. Contemporary Security Price Records — serves QT2, QT3, QT4

| Source | Author/Compiler | Date | Source Type | Primary/Secondary | Claims/Questions Supported | Reliability | Access | Notes |
|---|---|---|---|---|---|---|---|---|
| *The Course of the Exchange, and Other Things* | John Castaing (from 1698), successors | 1698–19th c. | periodical | Primary | QT2, QT3 | High | access-failed | Foundational primary source, accessible only indirectly through the reconstructions below |
| "Before the cult of equity: the British stock market, 1829–1929" | Gareth Campbell, Richard Grossman, John D. Turner | published *European Review of Economic History* 25(4), Nov 2021, pp. 645–679 (was QUCEH WP19-01 / CEPR DP13717) | reconstructed index, now peer-reviewed | Near-primary | QT2, QT3, QT4; **primary candidate for Gate 1 U1 benchmark** | High | access-failed | **Stage B correction:** working paper is now confirmed published in EREH 2021 (bibliographic metadata cross-confirmed, though the specific DOI `10.1093/ereh/heab003` surfaced only once — tentative). See Part C, Task A for methodology detail |
| "Deriving the railway mania" (2013, *Financial History Review* 20(1)) | **Gareth Campbell (sole author)** | 2013 | peer-reviewed article | Near-primary | QT2, QT3, QT4 (Mania/bust window) | High | access-failed | **Stage B correction:** this paper is sole-authored by Campbell, not "Campbell & Turner" as Stage A recorded — cross-confirmed across 3 independent queries (SSRN, RePEc, Cambridge Core). See Part G, Bibliographic Corrections Log |

**Flags:**
- **Provincial-exchange digitization bias — see Part F (Provincial-Market Resolution) below for the Stage B answer.** Stage A's claim that the relevant provincial-markets paper was by "Acheson, Hickson, Turner & Ye" was itself a **misattribution** — that author group wrote the London-only *Rule Britannia!* paper (B2). The actual provincial-markets paper is Campbell, Rogers & Turner, "The Rise and Decline of the UK's Provincial Stock Markets, 1869–1929" (QUCEH WP16-03) — corrected in Part G.

### A3. Company Records — serves QT2, QT3, QT4, QT5

| Source | Author/Compiler | Date | Source Type | Primary/Secondary | Claims/Questions Supported | Reliability | Access | Notes |
|---|---|---|---|---|---|---|---|---|
| TNA (Kew) railway company records, RAIL series | The National Archives, UK | 19th–20th c. | primary company records | Primary | QT2, QT3, QT4, QT5 | High | access-failed | Not tasked this round; catalogue-level access only, unchanged from Stage A |
| "Railway Returns and Railway Audit" (House of Lords, 5 Feb 1850), Historic Hansard | UK Parliament | 1850 | primary debate transcript | Primary | QT3 | High | access-failed | Not re-tasked this round |
| "Development of British Railway Accounting: 1800–1911" | (eGrove repository, U. Mississippi) | — | secondary, documents primary practice | Secondary | QT3 | High | access-failed | Not re-tasked this round |

### A4. Contemporary Press and Reference Works — serves QT2, QT3, QT4, QT5

| Source | Author/Compiler | Date | Source Type | Primary/Secondary | Claims/Questions Supported | Reliability | Access | Notes |
|---|---|---|---|---|---|---|---|---|
| *The Economist*, Historical Archive | Gale (digitizer) | from 1843 | periodical | Primary | QT2, QT3, QT4 | High | access-failed | No open substitute found; candidate for future paid-access discussion, but not yet triggered (see summary) |
| *The Railway Times* | London periodical | 1837/1839–1863 (partial) | periodical | Primary | QT2, QT3, QT4 | High | access-failed | Not re-tasked this round |
| Bradshaw's Railway Manual, Shareholders' Guide and Official Directory | W.J. Adams / Bradshaw's office | annual, 1848–1923 | reference work | Primary | QT2, QT3, QT5 | Medium-high | access-failed | **Now a Tier 1 input for the cash-flow reconstruction candidate — see Part D** |
| The Railway Shareholder's Manual | Henry Tuck | 19th c. (8th ed. 1847) | reference work | Primary | QT2, QT3, QT4 | Medium-high | access-failed | **Now a Tier 1 input for the cash-flow reconstruction candidate — see Part D**; 1847 edition is closer to the Mania peak than Bradshaw's annual series |

### A5. Failure Records — serves QT4, QT5 (US comparative capped to ≤2 panics per Gate 1 U3)

| Source | Author/Compiler | Date | Source Type | Primary/Secondary | Claims/Questions Supported | Reliability | Access | Notes |
|---|---|---|---|---|---|---|---|---|
| Poor's Manual of the Railroads of the United States | Henry Varnum Poor | annual, 1868–1917 | statistical compendium | Near-primary | QT5, US comparative | High | access-failed | Reconfirmed via bibliographic cross-check this round (multiple archive.org/HathiTrust volumes) — best-supported open primary source, still not directly re-fetched |
| Odlyzko cluster on the Mania bust and shareholder ruin (3 papers, incl. "...Robert Lucas Nash...") | Andrew Odlyzko | 2010–2011 | secondary, recovers primary analyst's work | Secondary/near-primary | QT4 (bust mechanics, shareholders ruined by calls) | High | access-failed | All three self-hosted (umn.edu) — reconfirmed bibliographically this round |
| US receivership figures for 1873 and 1893 | various secondary/tertiary sources | 1873–74, 1893–94 | secondary/tertiary restatement | Secondary | QT4, QT5 (2-of-3 cap) | Medium | access-failed | **Stage B finding:** figures vary across sources (89 vs. 76 US railroads bankrupt by 1873–74; ~$1.8bn vs. ~$2.5bn receivership capitalization in 1893) — treat as approximate ranges, not precise figures, until re-derived from Poor's Manual annual volumes or the academic sources below |
| Albro Martin, "Railroads and the Equity Receivership: An Essay on Institutional Change" | Albro Martin | 1974, *Journal of Economic History* 34(3), pp. 685–709 | peer-reviewed article | Secondary | QT4, QT5 (US comparative) | High | access-failed | **New, Stage B.** Bibliographic metadata cross-confirmed; accessibility not checked |
| Peter Tufano, "Business Failure, Judicial Intervention, and Financial Innovation: Restructuring U.S. Railroads in the Nineteenth Century" | Peter Tufano | 1997, *Business History Review* 71(1), pp. 1–40 | peer-reviewed article | Secondary | QT4, QT5 (US comparative) | High | access-failed | **New, Stage B.** Bibliographic metadata cross-confirmed |
| Stephen J. Lubben, "Railroad Receiverships and Modern Bankruptcy Theory" | Stephen J. Lubben | 2004, *Cornell Law Review* 89(6) | peer-reviewed article | Secondary | QT4, QT5 (US comparative) | High | access-failed | **New, Stage B.** Search indicates this is hosted openly at `scholarship.law.cornell.edu` — a genuinely promising open lead, but not independently fetch-confirmed given the network block |

**UK abandonment scale (unchanged from Stage A, still not a sourced ledger claim):** of ~12,000 miles authorized 1844–48, only ~7,200 miles (~60%) completed by 1852; share prices fell ~53–66% 1845–1850. **Stage B could not find a single citable aggregate "total UK investor capital lost" figure with stated methodology** — this is now flagged as a genuine load-bearing gap (see Summary).

### A6. US Quantitative Compendia — serves QT5, QT6 (US comparative, capped per U3)

| Source | Author/Compiler | Date | Source Type | Primary/Secondary | Claims/Questions Supported | Reliability | Access | Notes |
|---|---|---|---|---|---|---|---|---|
| ICPSR Study 2896 | Michael R. Haines | — | statistical compendium | Near-primary | QT5 | High | access-failed | Institutional-membership gated per Stage A; unchanged |
| Cambridge Group for the History of Population and Social Structure — GB railway-lines GIS (built from Michael Cobb's *The Railways of Great Britain: A Historical Atlas*, 1807–1998); also Great Britain Historical GIS (GBHGIS, U. Portsmouth) | Cambridge Group / GBHGIS | shapefiles from 1831 census years onward | GIS geographic dataset | Near-primary | QT1, QT5 | High | access-failed | **Stage B correction, replaces the Stage A entry:** the prior register listed "Jeremy Atack's GIS dataset" for this purpose, but Stage B search confirms **Atack's well-known historical-GIS railway dataset covers the American Midwest, not Great Britain** — that was a misattribution. These two GB-focused alternatives are the actual candidates and have not yet been individually verified |
| Historical Statistics of the United States — 1949/1960 (free) vs. 2006 Millennial Edition (paywalled) | US Census Bureau; Carter et al. eds. (2006) | 1949, 1960, 2006 | official statistical compendium | Primary/near-primary | QT5, QT6 | High | access-failed | Unchanged from Stage A |

---

## Part B — Academic / Institutional Sources (plan §4)

### B1. Railway Mania Financial Economics — serves QT4, H3, H5 — **required competing-interpretation pair present, genuineness now confirmed (Part C, Task G)**

| Source | Author | Date | Source Type | Primary/Secondary | Claims/Questions Supported | Reliability | Access | Notes |
|---|---|---|---|---|---|---|---|---|
| "Dispelling the Myth of the Naive Investor during the British Railway Mania, 1845–1846" | Gareth Campbell & John D. Turner | 2012, *Business History Review* 86(1) | peer-reviewed | Secondary | QT4, H3, H5 | High | access-failed | Uses a scrip-register/shareholder-allocation dataset; investigated in Part C Task C as a possible cash-flow source — inconclusive without full text |
| "Myopic rationality in a Mania" | **Gareth Campbell (sole author)** | 2012, *Explorations in Economic History* 49(1) | peer-reviewed | Secondary | QT4, H5 | High | access-failed | **Correction:** sole-authored, not Campbell & Turner |
| "'The Greatest Bubble in History': Stock Prices during the British Railway Mania" | Gareth Campbell & John D. Turner | ~2010, MPRA WP 21820 | working paper — **no journal publication found despite two targeted Stage B searches** | Secondary | QT2, QT3, QT4 | Medium-high | access-failed | Appears to remain an unpublished working paper; report as "not further confirmable" rather than assuming it was later published |
| "Cross-Section of a 'Bubble': Stock Prices and Dividends during the British Railway Mania" | **Gareth Campbell (sole author)** | ~2010, MPRA WP 21821 | working paper | Secondary | QT2, QT3, QT4 | Medium-high | access-failed | **Correction:** sole-authored, not Campbell & Turner |
| "Deriving the railway mania" | **Gareth Campbell (sole author)** | 2013, *Financial History Review* 20(1) | peer-reviewed | Secondary | QT4 | High | access-failed | **Correction (repeated from A2):** dataset is "863 railway equity securities listed on the LSE, 1843–1850, daily prices" (abstract-level, single strong source) |
| "The role of the media in a bubble" | Campbell, Turner & Walker | 2012, *Explorations in Economic History* 49(4) | peer-reviewed | Secondary | QT4 | High | access-failed | Unchanged |
| "Collective Hallucinations and Inefficient Markets: The British Railway Mania of the 1840s" | Andrew Odlyzko | 2010 (working paper; also *B.E. Journal of Economic Analysis & Policy* 10(1), 2010 per Stage B) | working paper / peer-reviewed | Secondary | QT4, H3, H5 | Medium-high | access-failed | **Opposing position, genuineness confirmed — see Part C Task G** |
| "Bubbles, Gullibility, and Other Challenges..." | Andrew Odlyzko | 2010, *First Monday* 15(9) | peer-reviewed (open-access journal) | Secondary | QT4 | High | access-failed | Unchanged |
| "The Collapse of the Railway Mania... Robert Lucas Nash..." | Andrew Odlyzko | 2011, *Accounting History Review* 21(3) | peer-reviewed | Secondary | QT4 | High | access-failed | Unchanged; cross-listed at A5 |

**Required competing-interpretation pair #1 (Gate 2) — Stage B genuineness check: CONFIRMED, see Part C Task G.**

### B2. Long-Run UK Asset Returns — serves the Gate 1 U1/U6 excess-return benchmark

| Source | Author | Date | Source Type | Primary/Secondary | Claims/Questions Supported | Reliability | Access | Notes |
|---|---|---|---|---|---|---|---|---|
| "Rule Britannia! British Stock Market Returns, 1825–1870" | Acheson, Hickson, Turner & Ye | 2009, *Journal of Economic History* 69(4) | peer-reviewed | Primary-adjacent | QT2, QT3, U1 (pre-1870 segment) | High | access-failed | **Stage B confirms this is an explicit LSE-only sample (240 securities, ~£285m market cap)** — relevant to Part F provincial resolution |
| "New Indices of British Equity Prices, 1870–1913" | Richard S. Grossman | 2002, *Journal of Economic History* 62(1) | peer-reviewed | Secondary | U1 (post-1870 segment) | High | access-failed | No open copy found; likely substitutable by the entry below |
| "Before the cult of equity: the British stock market, 1829–1929" | Campbell, Grossman & Turner | *European Review of Economic History* 25(4), 2021 (was QUCEH WP19-01) | peer-reviewed (Stage B: publication confirmed) | Secondary | **Primary candidate for U1 benchmark** | High | access-failed | Cross-listed at A2; see Part C Task A for full methodology detail |
| "What Moved Share Prices in the Nineteenth-Century London Stock Market?" | Campbell, Quinn, Turner & Ye | 2018, *Economic History Review* | peer-reviewed | Secondary | QT2, QT3 | High | access-failed | Unchanged |
| "Stocks for the Long Run: New Monthly Indices of British Equities, 1869–1929" | Richard S. Grossman | Wesleyan WP 2017-004 / CEPR DP12121 | working paper | Secondary | U1 (alternative splice) | Medium-high | access-failed | Unchanged |

### B3. Social Savings / Counterfactual Literature — serves QT5, H2 — **required competing-interpretation pair present, genuineness now confirmed (Part C, Task H)**

| Source | Author | Date | Source Type | Primary/Secondary | Claims/Questions Supported | Reliability | Access | Notes |
|---|---|---|---|---|---|---|---|---|
| *Railroads and American Economic Growth* | Robert W. Fogel | 1964, Johns Hopkins UP | book | Secondary | QT5, H2 | High | access-failed | archive.org listing found in Stage A |
| *American Railroads and the Transformation of the Ante-bellum Economy* | Albert Fishlow | 1965, Harvard UP | book | Secondary | QT5, H2 | High | access-failed | No open copy found; **not strictly load-bearing for Gate 2** since Fogel's own open book already represents this camp — see Paid-Access Escalation reasoning below |
| *Railways and Economic Growth in England and Wales, 1840–1870* | G.R. Hawke | 1970, Clarendon Press | book | Secondary | QT5, H2 (UK) | High | access-failed | **Stage B reclassification: Hawke vs. Leunig is NOT a second genuine competing pair** — see Part C Task H |
| "Time is Money: A Re-Assessment of the Passenger Social Savings from Victorian British Railways" | Tim Leunig | 2006, *Journal of Economic History* 66(3) | peer-reviewed | Secondary | QT5, H2 | High | access-failed | Confirmed (abstract-level) to be an explicit re-assessment/extension of Hawke's method with a revised counterfactual, not a materially different method |
| "Social savings" (survey) | Tim Leunig | 2010, *Journal of Economic Surveys* 24(5) | peer-reviewed survey | Secondary | QT5, H2 | High | access-failed | Unchanged |
| "Railroads and American Economic Growth: A 'Market Access' Approach" | Dave Donaldson & Richard Hornbeck | 2016, *QJE* 131(2) | peer-reviewed | Secondary | QT5, H2 | High | access-failed | **Opposing position, genuineness confirmed with high confidence — see Part C Task H.** Headline: removing all 1890 US railroads would cut agricultural land value 73%, GNP 6.3% — "more than double" Fogel's estimate |
| "The Transport Revolution in Industrializing Britain: A Survey" | Dan Bogart | working paper, ~2013 | working paper | Secondary | QT1, QT5 | Medium-high | access-failed | **Also a Tier 3 canal-comparison source — see Part E** |

**Required competing-interpretation pair #2 (Gate 2) — Stage B genuineness check: CONFIRMED, high confidence, see Part C Task H.** Hawke vs. Leunig reclassified as internal refinement, not a second pair — this does not threaten Gate 2 since the pair requirement is already met independently.

### B4. Steam Power / GPT Diffusion Economics — serves QT1, QT5.3

| Source | Author | Date | Source Type | Primary/Secondary | Claims/Questions Supported | Reliability | Access | Notes |
|---|---|---|---|---|---|---|---|---|
| *Steam Power and British Industrialization to 1860* | G.N. von Tunzelmann | 1978, Oxford UP | book | Secondary | QT1, QT5.3 | High | access-failed | **Stage B finding: an archive.org listing (`archive.org/details/steampowerbritis0000vont`) was found, marked "Free Download, Borrow, and Streaming" — this potentially contradicts Stage A's "no open copy found" claim.** Not confirmed whether this is genuine free download or Controlled-Digital-Lending (borrow-only); needs direct manual check |
| "Steam as a General Purpose Technology: A Growth Accounting Perspective" | Nicholas Crafts | 2004, *Economic Journal* 114(495) | peer-reviewed | Secondary | QT1, QT5.3, H5 | High | access-failed | DOI confirmed: `10.1111/j.1468-0297.2003.00200.x`. Complementary-capital-requirements detail found only at moderate confidence (see Part C Task I) |
| "The early diffusion of the steam engine in Britain, 1700–1800: A reappraisal" | Nuvolari, Verspagen & von Tunzelmann | 2011, *Cliometrica* 5(3) | peer-reviewed | Secondary | QT1 | High | access-failed | **Stage B scope caveat: covers 1700–1800 only** — does not reach HIS-001's core 1800–1860 period |
| "Stationary steam power in the United Kingdom, 1800–70: An empirical reassessment" | Sean Bottomley | 2024/2025, *Economic History Review* 78(3), pp. 825–848 | peer-reviewed | Secondary | QT1, QT5.3 (fills the 1800–1860 gap) | High | access-failed | **New, Stage B.** DOI `10.1111/ehr.13375`; a Cardiff University ORCA repository copy was found (`orca.cardiff.ac.uk/id/eprint/171089/1/ehr.13375.pdf`) — promising open lead, not fetch-confirmed. Directly covers the period gap left by Nuvolari et al. (2011) |

### B5. Business/Financial History of Railway Companies, incl. Accounting — serves QT3, QT4.4 — **secondary dispute present, second dispute added in Stage B**

| Source | Author | Date | Source Type | Primary/Secondary | Claims/Questions Supported | Reliability | Access | Notes |
|---|---|---|---|---|---|---|---|---|
| "The Beginnings of Accounting for Capital Consumption..." | A.J. Arnold & S. McCartney | 2002, *Accounting and Business Research* 32(4) | peer-reviewed | Primary-adjacent | QT3, QT4.4 | High | access-failed | No open copy found; **not strictly load-bearing for Gate 2** (see Paid-Access Escalation reasoning) |
| "Financial Reporting in the Context of Crisis..." | S. McCartney & A.J. Arnold | 2002, *European Accounting Review* 11(2) | peer-reviewed | Secondary | QT3, QT4.4 | High | access-failed | Unchanged |
| "Were they ever 'productive to the capitalist'? Rates of return on Britain's railways, 1830–55" | A.J. Arnold & S. McCartney | 2004, *Journal of European Economic History* 33, pp. 383–410 | peer-reviewed | Primary-adjacent | QT3, QT4.4, H4 — **fills the pre-1870 gap left by Mitchell/Chambers/Crafts (2011)** | High | access-failed | **New, Stage B.** Directly covers 1830–55 (the Mania and immediate aftermath) with a comparable rates-of-return method |
| "Accounting for the 'railway mania' of 1845 — A great railway swindle?" | Rob Bryer | 1991, *Accounting, Organizations and Society* 16(5-6) | peer-reviewed | Secondary | QT3, QT4.4 | Medium-high | access-failed | Unchanged |
| "Revisiting the British railway 'mania' of 1845–1846 with Marx's theory of crises..." | Rob Bryer | 2024/2025, *Accounting History Review* 35(1) | peer-reviewed | Secondary | QT3, QT4.4 | Medium | access-failed | Unchanged |
| McCartney (& Arnold?) case study on the York and North Midland Railway | Sean McCartney (Stage A/B agents disagree on whether Arnold is a co-author — **unresolved attribution, see Part G**) | 2022 online / 2024 print, *Business History* 66(5), pp. 1187–1213 | peer-reviewed | Secondary | H3, H4; **core input to Part D cash-flow candidate** | High | access-failed | **Stage B finding (abstract-level, important):** reports YNM return to equity of **10.1% on its pre-Mania network vs. −0.3% on its Mania-era construction** — direct operating-vs-boom-capital distinction. Explicitly disputes Campbell & Turner (2015) below |
| "Managerial failure in mid-Victorian Britain? Corporate expansion during a promotion boom" | Gareth Campbell & John D. Turner | 2015, *Business History* 57(8) | peer-reviewed | Secondary | H3, H4 | High | access-failed | **New dispute identified in Stage B:** argues 1860s-boom expansion by established railways was rational/optimal — the McCartney paper above explicitly challenges this "optimal" framing for the 1840s Mania via the YNM case. A second, Campbell/Turner-adjacent scholarly dispute distinct from Task G's Mania-interpretation pair |
| "How Good Was the Profitability of British Railways, 1870–1912?" | Brian Mitchell, David Chambers & Nick Crafts | 2011, *Economic History Review* 64(3), pp. 798–831 | peer-reviewed | Primary-adjacent | QT3, H4 | High | access-failed | DOI confirmed `10.1111/j.1468-0289.2010.00550.x`. **Identity disambiguation reversed in Stage B — see Part G:** circumstantial evidence now leans toward "Brian Mitchell" being the **same person** as B.R. Mitchell (B6), not confirmed different as Stage A stated |

**Secondary disputes (not the two required Gate 2 pairs, but relevant to QT3/QT4.4/H3/H4):**
1. Bryer's "manipulation/swindle" framing vs. Arnold & McCartney's more measured account — asymmetric access (Bryer open, Arnold & McCartney paywalled).
2. **New in Stage B:** Campbell & Turner (2015, "optimal expansion") vs. McCartney (2024, YNM case, "managerial failure") — a live, documented disagreement specifically about the Mania-era buildout decision.

### B6. Official Statistics Compendia — serves all quantitative branches; benchmark deflator source

| Source | Author/Compiler | Date | Source Type | Primary/Secondary | Claims/Questions Supported | Reliability | Access | Notes |
|---|---|---|---|---|---|---|---|---|
| *Abstract of British Historical Statistics* / *British Historical Statistics* | B.R. Mitchell (Brian Redman Mitchell; with Phyllis Deane; later H.G. Jones) | 1962 (later eds. to 1988) | official statistics compendium | Secondary compendium | all quantitative UK branches | High | access-failed | **Stage B finding:** B.R. Mitchell's full name confirmed as Brian Redman Mitchell, Fellow of Trinity College Cambridge, lectured in Economic History at Cambridge 1967–1991, research interests explicitly included transport/distribution — see Part G disambiguation |
| "A Millennium of Macroeconomic Data for the UK" | Bank of England (dataset, v3.1, to 2016) | — | official statistics dataset | Secondary/tertiary compilation | Gate 1 U1/U6 benchmark (consol yields), deflators | High | access-failed | Unchanged; bankofengland.co.uk directly confirmed as a blocked host in Stage B's own network test (see top of file) |

### B7. Synthesis Works — orientation only, **explicitly NOT load-bearing evidence**

| Source | Author | Date | Source Type | Primary/Secondary | Claims/Questions Supported | Reliability | Access | Notes |
|---|---|---|---|---|---|---|---|---|
| *Technological Revolutions and Financial Capital* | Carlota Pérez | 2002, Edward Elgar | book (non-empirical synthesis) | N/A — framing only | none | Low-for-evidence | access-failed | Unchanged; must never be cited as evidence |
| *The Visible Hand* | Alfred D. Chandler Jr. | 1977, Belknap/Harvard UP | book (narrative history) | N/A — framing only | none | Low-for-evidence | access-failed | Unchanged; framing only |

---

## Part C — Tier 1 Deep-Dive Verification Findings (Stage B)

All findings below are WebSearch-derived (bibliographic cross-confirmation and/or abstract-level snippet content), **not full-text confirmed**, per the network-access constraint above.

**Task A — UK broad equity benchmark.** Publication confirmed (EREH 2021, cross-listed A2/B2). Security universe: "over 5,800 securities representing about 4,500 companies," 1+ million security-month observations (Course of the Exchange 1829–1868 + Investor's Monthly Manual 1869–1929). Dividend treatment: three parallel series constructed — capital-gains, dividend-yield, and total-return (plus a 30-company blue-chip series spliced to the FT30). Survivorship/delisting: authors checked the December 1870 IMM for disappeared companies, found some had merely moved to a regional exchange, and applied two alternative survivorship adjustments (buy-and-hold, and a conservative "−100% return/zero dividend at delisting" upper-bound) — this specific detail (incl. a cited "77 firms" figure) came from a single search hit and is **not independently cross-confirmed**, moderate confidence only. London-vs-provincial coverage: not resolved by this task directly — see Part F.

**Task B — Railway Mania price/return series.** Sample: "863 railway equity securities listed on the LSE between 1843 and 1850," daily prices (single strong source, Cambridge Core/QUB snippet, not independently re-confirmed by a second query). Companion cross-sectional paper on dividends ("Cross-Section of a 'Bubble'") appears to remain an unpublished MPRA working paper. Dividend treatment of the daily index itself: moderate confidence it is price-only (capital-gains), not total-return — not confirmed with high confidence either way. Delisting: explicitly tested as a sensitivity issue — "the broader index of All Railways rose by between 93.5 percent and 98.4 percent **depending on how the delisting of shares is dealt with**" — a real strength, exact mechanics not visible in snippets.

**Task C — Call-based financing and investor cash flows.** No existing paper found performing a full company-level, call-by-call cash-flow reconstruction. Closest candidate, "Dispelling the Myth of the Naive Investor" (Campbell & Turner 2012), uses a scrip-register/shareholder-allocation dataset characterizing investor types and aggregate performance — **not confirmed to contain company-level call-schedule data** without full text. Proposed candidate and required sources: see Part D.

**Task D — Capital formation and overbuild.** NBER/FRED series confirmed authorized-mileage-only (see A1). "Capital authorized vs. actually raised/called" (e.g., "paid-up capital £30m early-1840s → >£100m by 1849" against "~8,590 miles authorized 1845–47") came from a single unsourced secondary snippet — **treat as a lead to verify directly, not an established fact**; likely underlying compilation is B.R. Mitchell's *Abstract of British Historical Statistics*/*International Historical Statistics*, unconfirmed. Atack GIS misattribution corrected (see A6, Part G). Bonus finding: a live scholarly dispute on whether Mania-era expansion by established railways was rational (Campbell & Turner 2015) or managerial failure (McCartney 2024, YNM case) — see B5.

**Task E — Operating economics vs. shareholder returns.** Mitchell/Chambers/Crafts (2011) methodology: ROCE = net traffic revenue / paid-up capital on "all lines worked," 5-year averages; net revenue from official *Railway Returns*, paid-up capital from half-yearly accounts; exact company count not confirmed. Whether the paper explicitly addresses the pre-1868 depreciation problem is **not confirmed** either way. Strong companion for the earlier period found: Arnold & McCartney (2004), covering 1830–55 directly (see B5). Disambiguation of "Brian Mitchell": see Part G.

**Task F — Failure and post-boom outcomes.** No citable aggregate UK investor-capital-loss figure found for the Mania bust — **genuine, currently unfilled gap** (H.G. Lewin 1936 is the most likely repository of such a figure, not accessible via search). US 1873/1893 receivership figures found only as approximate, inconsistent secondary/tertiary restatements (see A5); three real academic sources identified as a better foundation (Martin 1974, Tufano 1997, Lubben 2004 — the last appears openly hosted at Cornell). Poor's Manual and the Odlyzko cluster reconfirmed as solid, accessible-by-hosting-pattern foundations.

**Task G — Railway Mania competing interpretations: genuineness.** **Confirmed as a genuine, substantive disagreement**, not merely differently-titled papers. Odlyzko (abstract-level): "...induced a collective hallucination that made investors ignore [available quantitative warning signs]." Campbell (abstract-level): investors were "myopic" (short-horizon) but "rational" given their expectations; prices tracked non-railway fundamentals once short-term growth is controlled for. A secondary synthesis found directly in search corroborates the opposition: "Odlyzko (2010) suggested that 'collective hallucinations' were responsible... whilst Campbell (2010) argued that changes in dividends... were the main cause." **Caveat:** this confirms opposite empirical/interpretive claims about the same episode, but search snippets did not confirm a direct citation-level rebuttal within either paper's own text — treat as "abstract-level, cross-confirmed disagreement of substance," not "documented citation-level rebuttal," pending full-text access.

**Task H — Social-value competing interpretations: genuineness.** **Confirmed, high confidence.** Donaldson & Hornbeck's own framing explicitly starts from Fogel's agricultural-sector approach and replaces the partial-equilibrium "social saving" measure with a general-equilibrium "market access" measure; headline result more than double Fogel's estimate. Fishlow's own estimate differs from Fogel's within the same method (via a different counterfactual), which supports treating "Fogel/Fishlow" as one coherent partial-equilibrium camp opposing Donaldson & Hornbeck's general-equilibrium camp. **Hawke vs. Leunig reassessed as NOT a second genuine pair** — Leunig's paper explicitly reassesses/extends Hawke's method with a revised counterfactual (walking vs. stage-coach), same underlying framework, different assumptions and bottom-line number. Use this pairing as "successive refinement," not a second competing interpretation, in any future Evidence Ledger entry.

**Task I — Steam diffusion and productivity timing.** Crafts (2004): steam contributed near-zero growth pre-1830, peak growth-accounting impact roughly a century after Watt; delay attributed to "comprehensive adjustment processes, co-inventions, and complementary investments." A more specific complementary-capital list (boiler materials, mechanical/engineering understanding, coal-transport costs, iron-foundry buildout) surfaced via a broader, less precisely-sourced synthesis — **not confirmed as a direct quote from Crafts (2004) specifically**, treat as plausible background only. Nuvolari/Verspagen/von Tunzelmann (2011) reappraises the Kanefsky & Robey steam-engine census but **covers only 1700–1800** — does not reach HIS-001's 1800–1860 core period. New finding: Bottomley (2024/2025) directly covers 1800–1870 and may be open via Cardiff ORCA — a stronger, more current, more period-relevant candidate than relying on the 2011 paper alone. Von Tunzelmann's 1978 book may have a genuine archive.org listing (see B4) — needs a manual check to resolve "free download" vs. "borrow-only."

---

## Part D — Cash-Flow Reconstruction Candidate (for Stage C; not performed here)

**Proposed candidate: York and North Midland Railway (YNM), George Hudson's flagship company.**

**Why representative:**
1. As Hudson's own company, YNM has unusually rich surviving documentation and scandal-driven contemporary/scholarly scrutiny.
2. A directly relevant, recent academic case study already exists — the McCartney (2024) *Business History* paper reports YNM's **return to equity as 10.1% on its pre-Mania network vs. −0.3% on its Mania-era construction** — precisely the "operating conditions vs. boom-capital-committed" distinction HIS-001's cash-flow requirement (Gate 1 U2) needs, and it comes with independent scholarly corroboration since it explicitly engages (and disputes) Campbell & Turner's competing account.
3. Two independent, open, contemporary reference works (Bradshaw's Railway Manual, Henry Tuck's Railway Shareholder's Manual) plus Campbell's 863-security daily price index give plausible cross-checks for capital, dividends, and market valuation at specific dates.

**Required cash-flow fields (not yet located via search — genuine remaining gap):**
- Subscription/deposit-per-share terms at IPO
- Installment/call schedule: exact dates and amounts called
- Dividend timing and amounts across the Mania and bust (1845–1850)
- Market/exit value at specific dates (available via Campbell's daily index once cross-referenced to YNM specifically)

**Verified-by-search-only sources available:** Bradshaw's Railway Manual (annual, from 1848 — per-company paid-up capital, calls, dividends); Henry Tuck's Railway Shareholder's Manual (1845/1847 editions — closer to the Mania peak, subscription/contract terms); McCartney (2024) case-study figures; Campbell's daily price index for market valuation.

**Remaining gaps:** the exact call-schedule dates/amounts for YNM specifically were not found via search — this requires reading specific Bradshaw's/Tuck's pages, which the network-access block currently prevents. Alternative candidates considered but less well-supported by existing academic groundwork: Eastern Counties Railway (also Hudson-chaired, similarly troubled reputation), York, Newcastle & Berwick Railway, Caledonian Railway. YNM is recommended primarily because McCartney (2024) has already done comparable groundwork.

**This is a candidate proposal only — the reconstruction itself is Stage C work, not performed here.**

---

## Part E — Tier 3: Canal Mania Bounded Comparison

Deliberately minimal, per plan §12 (U4) and the Stage B instructions (max: one quantitative/near-primary source, one or two academic sources). Purpose is narrowly to test whether infrastructure speculation/capital overcommitment predated railways and whether financing mechanisms were railway-specific — **not** a canal narrative chapter or a basis for cross-revolution Pattern promotion.

| Source | Author | Date | Source Type | Access | Role |
|---|---|---|---|---|---|
| "Collective Hallucinations and Inefficient Markets: The British Railway Mania of the 1840s" | Andrew Odlyzko | 2010 | working paper | access-failed | **Does double duty** — cross-listed at B1. Search confirms it explicitly reviews financial statements of **seven major English canals from the 1770s to the 1850s** as a comparative basis for the railway-mania capital-market theory it argues against |
| "The Transport Revolution in Industrializing Britain: A Survey" | Dan Bogart | working paper, ~2013 | working paper | access-failed | Cross-listed at B3. Broad comparative context across turnpike/canal/railway waves; not quantitative-primary on canal share prices specifically |
| *The Finance of Canal Building in Eighteenth-Century England* | J.R. Ward | 1974, Oxford Historical Monographs, Oxford UP | academic monograph | access-failed | **New, Stage B, genuinely canal-specific.** Closest thing found to a near-primary quantitative reconstruction (e.g., a cited finding that ~59% of share purchases in one canal case were from outside the local region, ~36% from London). Appears to be a physical/OOP book (AbeBooks/Amazon only in search results) — likely the weakest-accessibility item in this set |

**Data-availability caveat (low-weight, non-academic source, flagged for completeness only):** one non-academic source suggested the 1790s Canal Mania specifically has a thinner quantitative record than the Railway Mania (contemporary papers announced share auctions but rarely printed resulting prices). Treat as an unconfirmed background consideration, not a sourced fact, when scoping the Stage C canal ledger section.

---

## Part F — Provincial-Market Coverage Question

**Conclusion: partially resolved — material limitation for the Railway-Mania-specific series; less clear (leaning toward less material, but genuinely unresolved) for the broader 1829–1929 benchmark index.**

Reasoning:
- The Mania-specific price series (Campbell 2013, 863 securities) is **explicitly, confirmedly London-only** ("listed on the London Stock Exchange"). Likewise "Rule Britannia!" (Acheson, Hickson, Turner & Ye 2009), which spans the Mania period, is confirmed as an explicit **LSE-only sample** (240 securities, ~£285m market cap).
- Independently-documented provincial railway trading during exactly this period was substantial: Glasgow hosted 110 listed railway companies by end-1845; an 1836 Liverpool share list already had 38 railways among 71 listed companies (>53%); new exchanges opened in Manchester, Aberdeen, Edinburgh, and roughly a dozen English towns in 1844–45.
- The actual provincial-markets paper (Campbell, Rogers & Turner, QUCEH WP16-03 — corrected from Stage A's misattribution) covers **1869–1929**, i.e., strictly *after* the Mania — it cannot itself confirm or deny 1840s provincial coverage.
- For the post-1869 portion of the 1829–1929 total-return benchmark, the Investor's Monthly Manual records where companies were "chiefly traded" across exchanges, which may partially (not fully) mitigate the gap for that later period — no snippet confirmed or denied whether provincial-**only** securities are systematically excluded from the 1829–1929 index.

**Net effect on HIS-001:** treat provincial-exchange exclusion as a **material, evidenced limitation** specifically for any claim built on the Mania-period price series; carry this into `REV-HIST-001` as an explicit, stated limitation rather than an assumption that it's solved. The broader benchmark's post-1869 exposure to this bias remains genuinely unresolved, not merely "probably fine."

---

## Part G — Bibliographic Corrections Log (Stage B)

1. "Deriving the railway mania" (2013, *Financial History Review*) — **sole-authored by Gareth Campbell**, not "Campbell & Turner" as Stage A recorded.
2. "Myopic rationality in a Mania" (2012, *Explorations in Economic History*) — **sole-authored by Gareth Campbell**.
3. "Cross-Section of a 'Bubble'" (MPRA WP 21821) — **sole-authored by Gareth Campbell**.
4. The provincial-markets paper is **Campbell, Rogers & Turner** (QUCEH WP16-03, covers 1869–1929) — **not** "Acheson, Hickson, Turner & Ye," which is instead the London-only *Rule Britannia!* paper (JEH 2009, covers 1825–1870). Do not conflate.
5. "Jeremy Atack's GIS dataset" (previously listed at A6) covers the **American Midwest, not Great Britain** — misattribution corrected; replaced with the Cambridge Group / GBHGIS candidates (unverified).
6. "Managerial Failure in early Victorian Britain..." (*Business History* 66(5)) — Stage B's two research passes **disagree on authorship**: one pass reports Sean McCartney as sole author; the other reports "McCartney, S. and Arnold, A.J." as co-authors. **This is itself unresolved and flagged rather than silently resolved** — confirm exact authorship before citing in Stage C.
7. "Brian Mitchell" (co-author, Mitchell/Chambers/Crafts 2011) vs. "B.R. Mitchell" (*British Historical Statistics* compiler) — **Stage A flagged these as not-confirmed-different; Stage B circumstantial evidence now leans toward SAME person** (matching Cambridge affiliation, matching "transport and distribution" research interest, and a related Chambers/Crafts working paper explicitly thanking "Brian Mitchell" for supplying unpublished rate-of-return estimates — consistent with B.R. Mitchell's known practice of compiling exactly this kind of data). **Not full-text confirmed either way** — recommend checking the 2011 article's author-affiliation footnote or Trinity College Cambridge's Annual Record (Mitchell appears to have died ~2012–2013 per search) directly.
8. "Before the Cult of Equity..." (QUCEH WP19-01) is now confirmed published as "Before the cult of equity: the British stock market, 1829–1929," *European Review of Economic History* 25(4), 2021, pp. 645–679 — the published title dropped "New Monthly Indices of."

---

## Stage B Completion Summary

### A. Access Summary

| Status | Count |
|---|---|
| verified-open | 0 |
| verified-partial | 0 |
| verified-paywalled | 0 |
| access-failed | ~58 (all Part A, Part B, and Part E entries touched in Stage A/B — full-text/dataset opening attempted via the confirmed categorical network block and failed for infrastructure reasons) |
| not-yet-checked | Tier 2 (equipment/locomotive manufacturers, coal/iron/steel suppliers, landowners, logistics hubs, downstream industrial users, non-London-listed railway companies as a distinct research target) — **deliberately deferred, 0 sources identified**, per the research-budget guardrail (Tier 1 completeness prioritized over Tier 2 breadth, and Tier 1 itself could not be fully verified this round) |

### B. Tier 1 Coverage Matrix

| Requirement | Status | Basis |
|---|---|---|
| A. UK broad equity benchmark | Partial | Strong candidate confirmed published (EREH 2021), security universe/dividend treatment found at abstract level; survivorship-adjustment detail only moderate-confidence; provincial coverage unresolved (Part F) |
| B. Railway price/return series | Partial | Strong candidate (863-security LSE daily index), delisting explicitly handled as sensitivity test; dividend treatment (price-only vs. total-return) not confirmed with high confidence |
| C. Call-based financing/cash-flow | Partial | No existing full reconstruction found; strong, well-evidenced candidate company (YNM) and required source combination identified; exact call-schedule data still missing (Part D) |
| D. Capital formation/overbuild | Partial | Authorized-mileage series confirmed but not paired with a "built" series in one dataset; capital-raised figure weakly sourced; GIS dataset misattribution corrected but replacement unverified |
| E. Operating economics vs. shareholder returns | Partial | Core source (Mitchell/Chambers/Crafts 2011) and a strong earlier-period companion (Arnold & McCartney 2004) both identified; methodology detail and depreciation-treatment confirmation still pending full text |
| F. Failure/post-boom outcomes | Partial | Poor's Manual and Odlyzko cluster reconfirmed as solid; UK aggregate capital-loss figure remains a genuine unfilled gap; US receivership figures approximate, three real academic sources identified as a better foundation |
| G. Railway Mania competing interpretations | Sufficient for Stage C (with caveat) | Genuine substantive disagreement confirmed at abstract level; citation-level rebuttal not confirmed — acceptable for Gate 2's "competing interpretations" bar |
| H. Social-value competing interpretations | Sufficient for Stage C | High-confidence, explicit methodological disagreement confirmed (Donaldson & Hornbeck vs. Fogel); Hawke/Leunig correctly reclassified as not a second pair |
| I. Steam diffusion/productivity timing | Partial | Crafts (2004) confirmed; core 1800–1860 period gap identified and a promising new candidate (Bottomley 2024/25) found to fill it, not yet confirmed open |

**No requirement is rated "Blocked"** — a plausible path exists for all nine, contingent on resolving the network-access constraint or on manual/external verification.

### C. Load-Bearing Gaps (genuine, unresolved)

1. **No citable aggregate figure for total UK investor capital lost in the Railway Mania bust** — a real, currently unfilled evidentiary gap for QT4.3.
2. **Exact call-schedule/subscription data for the YNM cash-flow candidate** — not located via search; requires direct reading of Bradshaw's/Tuck's specific pages.
3. **Provincial-exchange coverage of the broader 1829–1929 benchmark index (post-1869)** — genuinely unresolved, not just under-confirmed.
4. **Whether Mitchell/Chambers/Crafts (2011) explicitly addresses the pre-1868 depreciation problem** — not confirmed either way.
5. **Authorship of the McCartney "Managerial Failure" paper** (solo vs. with Arnold) — the two Stage B research passes disagree; needs a single authoritative check.
6. **"Brian Mitchell" identity** — now leaning toward being the same person as B.R. Mitchell, reversing Stage A's caution, but not confirmed.
7. **The fundamental network-access constraint itself** — see below.

### D. Paid-Access Escalation

**None triggered this round.** The formal four-condition trigger (plan/Gate-1 U5; Stage B §9) requires: (1) load-bearing for Gate 2, (2) no credible open-access substitute exists, (3) exact missing material identified, (4) explicit consequence if unavailable. Applying this rigorously:
- *The Economist* archive, Fishlow (1965), Arnold & McCartney's 2002 papers, and Grossman (2002) all appear paywalled with no confirmed open substitute — **but** for each, either (a) a credible open substitute already satisfies the relevant Gate 2 requirement without it (e.g., Fogel's open book already represents the partial-equilibrium social-savings camp; Bryer's open 1991 paper partially covers the accounting-manipulation dispute), or (b) accessibility itself is unconfirmed rather than confirmed-paywalled, since the network block prevents even reaching a paywall page to observe it, or (c) it is useful but not strictly required for a hard Gate 2 minimum.
- No candidate currently meets all four conditions simultaneously. Per the Stage B rule ("do not ask merely because a famous source is paywalled"), none are escalated as a formal Paid Access Escalation this round.
- **Separately and more importantly:** the network-access constraint itself (see top of file) is flagged as an infrastructure question for the User — it is a different kind of blocker than any single paywalled source, and it caps how far "verification" can ever go in this session regardless of which sources are targeted.

### E. Provincial-Market Conclusion

**Partially resolved.** See Part F for full reasoning: material limitation confirmed for the Mania-period-specific series; genuinely unresolved (not simply "probably fine") for the broader post-1869 benchmark index.

### F. Cash-Flow Reconstruction Candidate

**York and North Midland Railway (YNM).** See Part D for full reasoning, required fields, available sources, and remaining gaps. Not performed in Stage B, per instructions.

### G. Network-Access Result

**Confirmed blocked.** Direct testing (curl and the WebFetch tool, against 4 diverse real URLs spanning official/institutional pages, academic working papers, downloadable books, and dataset pages) returned HTTP 403 in all 8 attempts, logged by the session's own proxy-status endpoint as explicit policy-denial events. `WebSearch` remains functional and was the sole basis for all Stage B findings above. See the top-of-file section for full detail and the recommendation to escalate this as a distinct infrastructure question.
