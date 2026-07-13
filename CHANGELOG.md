# Changelog

## 2026-07-12 — Workflow change: MAP-001 superseded by Pattern Validation Framework

Added:
- `governance/PATTERN_VALIDATION_FRAMEWORK.md` (`status: active`) — new governance document defining how a candidate Pattern (`PAT-###`) may be promoted from `draft` to `active`. Defines: a 6-state lifecycle (`draft → validated-in-one-cycle → cross-cycle-candidate → active → stable → archived`, each with meaning/entry/exit/review-authority/required-evidence); a reusable Validation Matrix template (rows: Steam & Railways, Electricity, Oil & Automobile, Semiconductor, Internet, Mobile, Cloud, AI — columns: Supports/Weakens/Rejects/Notes; no rows populated); minimum promotion requirements (≥2 independent revolutions, different institutional environments where possible, counter-evidence review, boundary/falsification conditions tested, no unresolved load-bearing gap, repeatable mechanism not narrative similarity); a 5-level evidence hierarchy (primary → near-primary quantitative → academic synthesis → historical interpretation → narrative analogy, with narrative analogy alone barred from ever promoting a Pattern); explicit rules for handling a contradicting revolution (boundary-narrowing vs. genuine rejection); a Pattern Quality Checklist; and a formal review process (Draft → Historical Validation → Counter-Evidence Review → Cross-Cycle Comparison → Promotion Decision, authority held jointly by the Research Architect and Investment Committee). Methodology only — no AI-era company, sector, or investment content.

Changed:
- `governance/WORK_BOARD.md` — HIS-001 status: "Pattern Validation Framework complete — awaiting methodology review." Records that the prior `MAP-001` authorization is withdrawn (no Mapping work existed or was started) and that the pipeline is now `Candidate Pattern → Pattern Validation Framework → Cross-cycle Historical Validation → Active Pattern → Historical → AI Mapping → Investment Thesis`. All three candidate Patterns remain `draft`; none reach `active` without a second historical revolution run through the new framework.

Note:
- This is a purely methodological change. No Historical Asset, Evidence Ledger, Source Register, Pattern content, Mapping, or Thesis was modified. No new historical research conducted.

## 2026-07-12 — HIS-001 Pattern Review: PASS WITH MINOR REVISIONS (1 of 2 applied)

Changed:
- `patterns/PAT-001_SOCIAL_VALUE_INVESTOR_RETURN_DIVERGENCE.md` — Pattern Statement revised per Pattern Review: removed the implication that HIS-001 observed social value, enterprise profitability, and investor return diverging within one fully matched episode/cohort. Now reads: "Across related infrastructure episodes, social value creation, enterprise profitability, and investor return can diverge materially. HIS-001 does not establish all three through one matched cohort-level dataset."

Note:
- Pattern Review authorized two minor Pattern revisions plus one bounded Historical-to-AI Mapping (`MAP-001`), but only the PAT-001 revision above was fully specified. The second revision's target file/wording and the required structure for `MAP-001` were not given — paused to ask the Research Architect for both rather than inventing MAP-001's structure, given its governance sensitivity (mandatory critical-differences section, falsifiability, no premature AI conclusion). No Mapping or Thesis file created yet.

## 2026-07-12 — HIS-001 Gate 3 PASSED; three candidate Patterns drafted

Added:
- `patterns/PAT-001_SOCIAL_VALUE_INVESTOR_RETURN_DIVERGENCE.md` — candidate pattern: infrastructure can create durable social/downstream value while direct investors see weak, uneven, or negative returns. Derived from `REV-HIST-001` §A/§E/§F and Evidence Ledger claims incl. C-107/108/109, C-112/113/120/121, C-133, C-188/190/191/192/193, C-224, C-272/273/274. `status: draft`, `confidence: low`.
- `patterns/PAT-002_CAPITAL_CYCLE_OVERBUILD.md` — candidate pattern: abundant speculative capital can accelerate deployment beyond near-term demand, impairing investors while leaving some productive capacity behind. Keeps authorization/subscription/called/paid/expenditure/completed-capacity/impairment strictly distinct per C-050/051/054–060/063/069/112/113/120/121/123. Presents both a rational-investment and a speculative-excess interpretation without forcing a binary. `status: draft`, `confidence: low`.
- `patterns/PAT-003_ENTRY_TIMING_AND_FINANCING_STRUCTURE.md` — candidate pattern: entry timing, leverage, and installment-call structure can dominate investor outcome within the same sector. Grounded in the cohort/leverage evidence (C-115–C-119, C-123/124) and explicit about the YNM cash-flow reconstruction's `undecidable` status (C-150–166) — cohort-level index evidence is not conflated with a verified representative investor's dated cash-flow history. `status: draft`, `confidence: low`.

Changed:
- `knowledge/industrial-revolutions/REV-HIST-001_STEAM_AND_RAILWAYS.md` — frontmatter `related` updated to add `PAT-001`–`003` now that those files exist; scope note updated to reflect their creation.
- `governance/WORK_BOARD.md` — HIS-001 status: "Candidate Pattern Drafts complete — awaiting Pattern Review." Historical Synthesis marked Gate 3 PASSED (stable historical asset).

Note:
- All three patterns derive only from `REV-HIST-001` and `HIS-001_EVIDENCE_LEDGER.md` — no new historical research conducted. Every substantive statement cites `C-###` IDs. Zero AI-era content (no companies, sectors, GPUs, data centers, valuations). No pattern may reach `active` within HIS-001 alone; cross-cycle validation from HIS-002/HIS-003 is required.
- No `MAP-001` or `THS-001` created.

## 2026-07-12 — HIS-001 Gate 3: minor revisions implemented

Changed:
- `knowledge/industrial-revolutions/REV-HIST-001_STEAM_AND_RAILWAYS.md` — implemented the 4 revisions from the Gate 3 Historical Stability Review (verdict: PASS WITH MINOR REVISIONS):
  1. Frontmatter `related` no longer lists nonexistent future assets (`PAT-001`–`004`, `MAP-001`); only `HIS-001` and `HIS-001-EVIDENCE-LEDGER` remain. Scope note updated to say future relationships are added once those files actually exist.
  2. §A: "the clearest available case" → "a well-documented case," with an explicit note that this study alone cannot establish comparative primacy across technological revolutions.
  3. §A: "much of the capital that financed it was impaired" → "identifiable cohorts, late entrants, and failed schemes suffered substantial impairment," with the no-aggregate-figure caveat restated inline.
  4. §H and the H3 row in §J: added explicit statement that the productive-overbuild evidence chain is cross-geography and cross-period (UK Railway Mania investor outcomes + US social-savings estimates + later UK productivity/infrastructure effects) — not a single-cohort UK capital-loss-to-social-benefit reconstruction, and that this supports H3 only partially.
- `governance/WORK_BOARD.md` — status: "Gate 3 minor revisions implemented — awaiting final confirmation."

Note:
- No Pattern, Mapping, or Thesis file created in this change set.

## 2026-07-12 — HIS-001 Historical Synthesis: REV-HIST-001 delivered (Gate 2 PASS)

Added:
- `knowledge/industrial-revolutions/REV-HIST-001_STEAM_AND_RAILWAYS.md` — the historical asset for HIS-001, derived strictly from the Evidence Ledger. ~3,880 words, mechanism-first and structured around the research question (Executive Answer; technology/cost; capital formation & overbuild; the Railway Mania interpretation debate; value creation vs value capture by actor; operating profit vs investor return; who lost money; was overbuild productive; profit-pool migration; H1–H5 verdicts; open questions; candidate reusable mechanisms). 75 distinct `C-###` claim IDs cited; every material conclusion traces to the ledger; **0 AI-era content** (no analogy, no AI companies, no GPUs/data centers/valuations). H1–H5 verdicts: H5 supported (medium-high); H2 & H3 partially supported; H1 partially supported with the supplier side undecidable; H4 undecidable. Candidate reusable mechanisms M1–M6 listed as provisional only — **no Pattern file created.** The four Gate 2 conditions are preserved as visible limitations (YNM cash-flow `undecidable`; provincial magnitude unquantified; no aggregate UK loss figure invented; two-hop citations labelled).

Changed:
- `governance/WORK_BOARD.md` — HIS-001 status: "Historical Synthesis complete — awaiting Gate 3 Historical Stability Review."

Note:
- Central finding, held to the evidence: technological importance, social value creation, enterprise profitability, shareholder return, and long-term excess return are five distinct things that diverged in this era — the "suppliers/builders were the winners" story is **untested** (not supported, not refuted) because the ledger has no supplier/coal/iron/landowner return data.
- No `PAT-*`, `MAP-001`, or `THS-001` created; no AI-era interpretation. Next: Gate 3 review, then (if passed) candidate pattern promotion and AI mapping.

## 2026-07-12 — HIS-001 Stage C complete: Evidence Ledger delivered

Added:
- `knowledge/industrial-revolutions/HIS-001_EVIDENCE_LEDGER.md` — the Stage C deliverable. **151 traceable claims** across C1–C8 (technology/cost/diffusion; capital formation/overbuild; prices/investor returns; cash-flow reconstruction; operating vs shareholder return; failure/impairment; competing interpretations; canals + US comparative), each read from actual full text at an exact page/table/figure location with unit/period/sample, counter-evidence, and limitations. Includes a Quantitative Backbone (21 core series), a disposition of the six carried Stage B gaps, and a Gate 2 readiness matrix. Claim tally: 105 supported / 29 partially-supported / 11 contested / 4 gap / 2 undecidable; classifications 66 quantitative-estimate / 37 historical-fact / 24 scholarly-interpretation / 15 research-inference; **0 ai-era analogy** (forbidden this stage).

Changed:
- `knowledge/industrial-revolutions/HIS-001_SOURCE_REGISTER.md` — applied the Stage C provenance correction (ledger C-197): the file previously mis-keyed "McCartney (2024) Managerial Failure" is actually **Campbell & Turner (2015) "Managerial Failure in Mid-Victorian Britain?"**; added **McCartney & Arnold (2001)** as the true (unread, paywalled) origin of the YNM 10.1%/−0.3% figures; added the newly-located **Tuck 1848/9th edition**.
- `governance/WORK_BOARD.md` — HIS-001 status: "Stage C complete — awaiting Gate 2 Evidence Sufficiency Review."

Note:
- **Cash-flow-aware reconstruction (York and North Midland Railway) = `undecidable`** with current evidence — no dated call schedule exists in any located source (three Tuck editions read, incl. one Stage B missed); no figure was fabricated or interpolated (ledger C-166).
- Genuine gaps carried forward: aggregate UK investor-capital-loss figure; provincial-underrepresentation magnitude for 1843–50; Arnold & McCartney (2004) full text; Odlyzko-vs-Mitchell railway-investment/GDP-share discrepancy.
- No `REV-HIST-001`, Pattern, Mapping, or Thesis created; no AI-era interpretation. Next: Gate 2 review, then (if passed) the historical draft.

## 2026-07-12 — HIS-001 Stage C active: Evidence Ledger construction

Changed:
- `governance/WORK_BOARD.md` — HIS-001 status: "Stage B PASS — Stage C Quantitative Backbone & Evidence Ledger active."

Note:
- Stage B passed Research Architect review. Stage C converts the verified source set into a traceable Evidence Ledger (`HIS-001_EVIDENCE_LEDGER.md`) with stable claim IDs, every claim tied to a source actually read at an exact location. No final narrative, no Pattern/Mapping/Thesis, no AI-era interpretation this stage. (Detailed Stage C completion entry appended when the ledger is delivered.)

## 2026-07-12 — HIS-001 Stage B: full-text source verification (network reopened)

Changed:
- `knowledge/industrial-revolutions/HIS-001_SOURCE_REGISTER.md` — after the User widened the environment egress allowlist, ran a full-text verification pass. Built a `curl` + `pypdf`/`beautifulsoup4` toolchain (the WebFetch tool itself is still 403 on a separate path) and **read the actual full text of ~20 Tier 1 load-bearing sources**, upgrading them from `access-failed` to `verified-open`. Adopted the 5-way access taxonomy with real evidence behind each label. Key verified findings: both Gate 2 competing-interpretation pairs are genuine and **citation-level** (Odlyzko fn 107 rebuts Campbell by name; Donaldson & Hornbeck engage Fogel by name in §II). Two full-text corrections to earlier search-level claims: (1) Donaldson & Hornbeck's result is "moderately larger" — 3.22% of GNP vs Fogel's 2.7% (upper bound 5.35%) — **not "more than double"**; (2) the Dec-1870-IMM survivorship check + buy-and-hold/−100% bounds belong to *Rule Britannia!* (Acheson et al. 2009), **not** *Before the Cult of Equity* (which does no survivorship adjustment). Resolved "Brian Mitchell" = B.R. Mitchell (same person, via the 2011 paper's internal self-citation chain). Confirmed sole authorship of three Campbell papers from actual PDFs. Assessed the York and North Midland Railway cash-flow candidate against real sources: "Dispelling the Myth" has no company-level call data; Tuck's Manual (1845/1847, read on archive.org) gives partial YNM inputs but no dated call schedule — a genuine remaining gap. Poor's Manual (~1899/1900) and Lubben (2004) read for US receivership evidence.
- `governance/WORK_BOARD.md` — status: "Stage B complete, now with full-text verification — awaiting Research Architect review"; network prerequisite marked resolved.

Note:
- Network constraint resolved at the proxy/allowlist level. Genuine gaps remaining: aggregate UK investor-capital-loss figure (absent from Odlyzko's full text); YNM dated call schedule (missing Tuck's/Bradshaw's editions); provincial-underrepresentation magnitude for 1843–50; Arnold & McCartney (2004) pre-1870 returns paper (paywalled, no open copy); "Managerial Failure" (Business History 66(5)) co-authorship unresolved.
- No Evidence Ledger claim rows, `REV-HIST-001`, Pattern, Mapping, or Thesis created. No cash-flow reconstruction performed. Still Stage B.
- Next step: Stage B review by the Research Architect before Stage C.

## 2026-07-12 — Environment network-access requirements documented

Added:
- `governance/ENVIRONMENT_NETWORK_REQUIREMENTS.md` — living allowlist for the remote environment. Diagnoses the current "Trusted" network level (allows GitHub + package registries, blocks the general web incl. all HIS-001 academic/primary sources), and lists the domains the User must add to the environment's custom allowlist to unlock source verification. 8 Tier-1-required domains + supplementary/orientation lists, each mapped to what it unlocks. Extended as needed per the "add as needed" protocol in the file.

Note:
- This is an infrastructure/operational change, not research content. No Evidence Ledger, narrative, Pattern, Mapping, or Thesis affected. HIS-001 remains at "Stage B complete — awaiting Research Architect review"; resolving network access is a prerequisite for Stage C, tracked separately from Stage C authorization.

## 2026-07-12 — HIS-001 Stage B: source verification, cash-flow candidate, network-access constraint confirmed

Changed:
- `knowledge/industrial-revolutions/HIS-001_SOURCE_REGISTER.md` — full Stage B pass. Directly tested network capability (curl + WebFetch against 4 diverse URLs: official/institutional page, academic working paper, downloadable book, dataset page) — **confirmed 403 in all 8 attempts**, logged by the session proxy as explicit policy denials. Adopted the 5-way access-status taxonomy (verified-open/partial/paywalled/access-failed/not-yet-checked); since no fetch succeeded, essentially all ~58 register entries are labeled `access-failed` rather than any `verified-*` status. Applied 8 bibliographic corrections (several "Campbell & Turner" papers are sole-authored by Campbell; the provincial-markets paper was misattributed; the Atack GIS dataset covers the American Midwest, not Great Britain; the "Brian Mitchell"/"B.R. Mitchell" identity flag now leans toward same-person, reversing Stage A's caution). Confirmed genuine (not title-level) disagreement for both required Gate 2 competing-interpretation pairs (Railway Mania: Campbell vs. Odlyzko; social savings: Fogel/Fishlow vs. Donaldson & Hornbeck), and reclassified Hawke vs. Leunig as a successive refinement, not a second pair. Identified a cash-flow reconstruction candidate (York and North Midland Railway) with supporting sources. Added a minimal Tier 3 canal-source set (3 sources). Resolved the provincial-market question as "partially resolved — material limitation for the Mania-period series." Assessed all 9 Tier 1 requirements as Partial or Sufficient-for-Stage-C; none Blocked. No Paid Access Escalation triggered (four-condition test applied and not met for any candidate).
- `governance/WORK_BOARD.md` — status: "Stage B complete — awaiting Research Architect review."

Note:
- **Network-access constraint is the dominant finding of this stage:** true full-text/dataset verification is not achievable in this session for any external source (organizational egress policy, not a per-host or client issue). Recommend the User treat this as a distinct infrastructure question, separate from any single paywalled source.
- No Evidence Ledger claim rows, `REV-HIST-001`, Pattern, Mapping, or Thesis created. No cash-flow reconstruction performed (candidate only). Stage B scope limits otherwise unchanged.
- Next step: Stage B review by the Research Architect. No automatic continuation into Stage C.

## 2026-07-12 — HIS-001 Gate 1 PASSED; Stage A Orientation complete

Added:
- `knowledge/industrial-revolutions/HIS-001_SOURCE_REGISTER.md` — Stage A deliverable: candidate source landscape across 6 primary/near-primary categories and 7 academic/institutional categories (plan §3, §4), with metadata, reliability, access path, and source-chain notes for ~45 candidate sources. Candidate sources identified; bibliographic metadata provisionally verified during Stage A. Full-text accessibility, methodological suitability, and actual evidentiary support are subject to Stage B verification. Both required Gate 2 competing-interpretation pairs have openly-claimed candidate sources on each side (Railway Mania: Campbell & Turner vs. Odlyzko; social savings: Fogel/Fishlow vs. Donaldson & Hornbeck) — genuine disagreement and accessibility remain to be confirmed in Stage B.

**Correction (2026-07-12, Stage B):** the phrase "~45 real, verified candidate sources" in this entry overstated Stage A's actual verification level. Stage A verified bibliographic existence (real titles/authors/venues) via web search, not full-text or dataset accessibility. Corrected per Research Architect Stage A review (PASS WITH CONDITIONS).

Changed:
- `governance/WORK_BOARD.md` — HIS-001 status: "Gate 1 PASS — Stage A Orientation active"; Gate 1 recorded as confirmed PASSED by the Research Architect.

Note:
- **Infrastructure constraint flagged:** this session's network egress policy rejected outbound `WebFetch` to every external domain tested (NBER, Bank of England, SSRN, RePEc, Wikipedia, institutional repositories), confirmed via the agent-proxy status endpoint as explicit policy denials, not client misconfiguration. All "open access" judgments in the Source Register are therefore based on web-search metadata and cross-confirmation, not a confirmed direct fetch, and are flagged as needing re-verification before Stage B treats any single source as load-bearing.
- Genuine gaps identified: (1) UK Parliamentary/regulatory records (A1) is the weakest-confirmed category; (2) ~10 likely-paywalled sources with no open substitute found, several load-bearing (Fishlow 1965, von Tunzelmann 1978, Arnold & McCartney 2002 papers, Grossman 2002); (3) an unresolved provincial-exchange digitization-bias question — reconstructed British share indices may underrepresent non-London-listed companies; (4) canal-mania sources (needed for the Gate 1 U4 bounded ledger section) were not covered in this Stage A pass and must be sourced before Stage C.
- No Evidence Ledger claim rows, `REV-HIST-001`, Pattern, Mapping, or Thesis file created in this change set, per Stage A scope limits.
- Next step: Stage A review. No automatic continuation into Stage B.

## 2026-07-12 — HIS-001 Gate 1 revisions implemented

Added:
- `governance/HIS-001_GATE_1_REVIEW.md` — Research Architect's Gate 1 Research Design Review (verdict: PASS WITH CONDITIONS), with rulings on U1–U8, scope-creep check, 12 required revisions, and escalation conditions.

Changed:
- `knowledge/industrial-revolutions/HIS-001_RESEARCH_EXECUTION_PLAN.md` — implemented all 12 Gate 1 required revisions: U1–U8 converted from unresolved questions to resolved decisions (§12); broad UK equity index set as primary excess-return benchmark, consols secondary (§10, §12 U1); cash-flow-aware return required for ≥1 cohort (§10, §12 U2); US case capped to ≤2 panic episodes, scoped to financing fragility/receivership only (§9.4, §12 U3); canals confirmed as one bounded ledger section, no narrative chapter (§12 U4); open-access-first sourcing rule with explicit paid-access trigger added (§5, §12 U5); benchmark-relative returns primary / real returns secondary with named deflator and sensitivity check (§10, §12 U6); colonial guaranteed-railway cases explicitly excluded (§12 U7); patterns capped at `draft` status within HIS-001 (§6, §12 U8); removed default "rejected hypothesis → archived pattern file" rule (§6); restructured Stopping Conditions into staged exit criteria so MAP-001 no longer gates evidence-collection or historical-draft completion (§11); added a Research-Budget Guardrail section (§13).
- `governance/WORK_BOARD.md` — HIS-001 status: "Gate 1 revisions implemented — awaiting Research Architect confirmation"; branch updated to `main`.

Note:
- No evidence collection started. No Source Register, Evidence Ledger, Pattern, Mapping, or Thesis file created in this change set. Primary research question and geographic/historical scope unchanged.
- Next step: Research Architect confirms all 12 revisions are correctly implemented; Gate 1 fully passes only after that confirmation.

## 2026-07-12 — HIS-001 kickoff: Research Execution Plan submitted

Added:
- `knowledge/industrial-revolutions/HIS-001_RESEARCH_EXECUTION_PLAN.md` — first HIS-001 deliverable (planning only; awaiting Gate 1 Research Design Review)
- `governance/HIS-001_RESEARCH_BRIEF.md` — imported from handoff package v1.0

Changed:
- `governance/WORK_BOARD.md` — HIS-001 claimed by claude-code; status: awaiting Research Design Review

Note:
- Repository foundation files were reconstructed from handoff package v1.0 (`PROJECT_STATUS.md`, `ORIGINAL_CONVERSATION.md`, HIS-001 brief) because the original Phase 1 files were not present in the GitHub repository. See DEC-006 in `governance/DECISIONS.md`.
- No evidence collection has started. Next gate: Research Design Review.

## 2026-07-12 — Foundation v1.1

Added:
- project constitution
- research scope
- operating principles
- naming and ID standard
- frontmatter standard
- agent instructions
- work board
- decision log
- research workflows
- canonical templates
- GitHub issue and pull-request templates
- AI revolution baseline
