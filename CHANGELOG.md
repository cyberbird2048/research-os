# Changelog

## 2026-07-22 — HIS-002 REV-HIST-002 Gate 3 minor revisions applied (resubmitted for confirmation)

Gate 3 (Historical Stability Review) returned **PASS WITH MINOR REVISIONS**. Claude Code applied the two required calibrations to `REV-HIST-002`; the amended synthesis is resubmitted for Gate 3 confirmation. Re-classification/calibration only — no new evidence, no Pattern verdict, no Matrix update, no Pattern promotion, no Cross-Cycle Comparison.

Changed:
- `knowledge/industrial-revolutions/REV-HIST-002_ELECTRICITY_GRID_AND_INDUSTRIAL_ELECTRIFICATION.md` — **Revision 1 (1937 → post-window sensitivity):** across §A.4, the §A "Why outcomes differed" close, §B, §D, and — for internal consistency — §G and §I PAT-002, the core-window conclusions now rest on the 1935 facts (output recovered above the 1929 peak; utilization materially recovered), the 1937 figures are labelled post-window sensitivity, E-206 is retained but reduced in weight, "fully absorbed by 1935" → "substantially reabsorbed by 1935, with further recovery visible in the 1937 post-window sensitivity", and unqualified "no permanent physical impairment" → "no evidence of persistent national utilization impairment through the available post-window sensitivity". **Revision 2 (§I PAT-001):** the causal "via holding-company structure" implication is removed — holding-company organization is now a candidate explanation the current index-level/open-source evidence does not identify as the causal mechanism (coexisting-divergence-only, no matched-cohort transfer, E-307 beta absorption, the operating-company economics gap, and the deferred S-005 limitation all preserved). The 1935 endpoint is labelled a **scope convention** from Brief §2.2, not a ledger-derived conclusion. Added a "Gate 3 revision record" note and updated the Stop point. Citation integrity re-checked (all cited `E-###` still exist in the ledger).
- `governance/WORK_BOARD.md`, `governance/PROJECT_STATE.md`, `governance/NEXT_ACTION.md` — Gate 3 recorded PASS WITH MINOR REVISIONS (calibrations applied), next step = Gate 3 confirmation; Cross-Cycle Comparison / Matrix HIS-002 verdicts remain blocked until confirmation.

Note:
- No Pattern verdict, no Matrix update, no Pattern promotion, no `MAP-001`/`THS-001`/AI-era/investment content. `PAT-003` stays `validated-in-one-cycle`; `PAT-001`/`PAT-002` stay `draft`; no Pattern is `active`.

## 2026-07-22 — HIS-002 REV-HIST-002 historical synthesis drafted (submitted for Gate 3)

Authored by claude-code under the Gate 2 authorization (DEC-016). Derived **strictly** from `HIS-002_EVIDENCE_LEDGER.md`; no new evidence introduced. Sets no Pattern verdict, updates no Validation Matrix, changes no Pattern status, promotes no Pattern, and contains no `MAP-001`/`THS-001`/AI-era/investment content.

Added:
- `knowledge/industrial-revolutions/REV-HIST-002_ELECTRICITY_GRID_AND_INDUSTRIAL_ELECTRIFICATION.md` (`id: REV-HIST-002`, `status: draft`, `confidence: low`) — the HIS-002 historical synthesis. Full required structure A–I (Executive Answer with the five value strata held separate; Historical Timeline 1900–1935; Value Creation vs Value Capture; Capital Cycle and Physical Capacity; Financing Structure and Investor Outcomes; Failure and Control Cases; Counter-Evidence and Alternative Explanations; Evidence Gaps; Pattern-Relevant Findings as descriptive input only). Every material conclusion cites an `E-###` ledger claim; citation integrity was checked programmatically (all 58 cited claims exist in the ledger; the only uncited claims are E-109/E-110/E-111, which the ledger marks adjacency/framing/non-load-bearing). Carries the three RA-imposed fixed boundaries verbatim.

Changed:
- `governance/WORK_BOARD.md`, `governance/PROJECT_STATE.md`, `governance/NEXT_ACTION.md` — current step = synthesis drafted, submitted for Gate 3; Gate Status gains a Gate-3 "IN REVIEW" row; Draft Assets gains `REV-HIST-002`; Active Task = Gate 3 Historical Stability Review; next review = Gate 3, after which the Cross-Cycle Comparison / Matrix verdict-setting begins.

Boundaries carried by the synthesis (RA-imposed, DEC-015/DEC-016):
- **PAT-001** — coexisting divergence only, not a matched-cohort value transfer (E-113, E-117, E-118).
- **PAT-002** — a US 1920s national physical overbuild is not supported; 1930s slack ≈ Depression demand shock + pre-1929 pipeline capacity (E-208, E-210, E-204/E-205).
- **PAT-003** — index-tier dispersion exists but is absorbed by market beta (E-307); security-level mechanism Undecidable-pending-access (E-311, E-370).

Note:
- No historical conclusion is promoted beyond the ledger; §I is descriptive input for the later Cross-Cycle Comparison, not Supports/Weakens/Rejects verdicts. `PAT-003` stays `validated-in-one-cycle`; `PAT-001`/`PAT-002` stay `draft`; no Pattern is `active`. Operating-company income data remains an explicit gap (FTC S-005 deferred). Evidence origin held to the United States, c. 1900–1935.

## 2026-07-21 — HIS-002 Gate 2: Evidence Sufficiency Review PASSED (six corrections applied)

The Research Architect's Evidence Sufficiency Review of `HIS-002_EVIDENCE_LEDGER.md` returned **PASS WITH CONDITIONS** with six required ledger classification corrections. Claude Code applied all six, converting the verdict to **PASS** and authorizing the `REV-HIST-002` historical synthesis. This change set is bookkeeping and re-classification only — no new evidence was collected, no verdict was set, no Pattern was promoted.

Added:
- `governance/HIS-002_GATE_2_REVIEW.md` (`id: HIS-002-GATE-2`, `status: active`) — the Gate 2 review record: verdict PASS WITH CONDITIONS → PASS, the six-correction disposition table, the three fixed synthesis boundaries, the DEFERRED (Part D) access-escalation note, and the DEC-015/DEC-016 cross-reference.
- `governance/DECISIONS.md` — **DEC-016** appended (by Claude Code, the decision DEC-015 routed here): records that all six lane fixes are applied, that the Evidence Sufficiency Review auto-converts to PASS, and that `REV-HIST-002` is authorized with the three fixed boundaries. (DEC-015, the verdict record, was appended by the PI Agent in `6a6631a`.)

Changed:
- `knowledge/industrial-revolutions/HIS-002_EVIDENCE_LEDGER.md` — six corrections: (1) **E-109** relabelled *Adjacency — no outcome weight* (excluded from the PAT-001 Supports tally; employment reallocation is a third construct); (2) new **E-117** records the PAT-001 Rejects search as executed with disposition *"Rejects not established"* (does not auto-convert to Supports); (3) new **E-118** records the matched-cohort value-transfer question as *Undecidable with current evidence*, kept distinct from the coexisting-divergence question that may proceed to synthesis; (4) **E-211** reclassified *Weakens (mixed)* with the pending-access attribute removed (the data were obtained); (5) **E-301–E-305, E-308, E-310** relabelled *Descriptive — no independent Supports weight* (E-307 shows the index dispersion is fully absorbed by market beta), with a Module A header note; (6) the Anti-Confirmation Balance Check restated on the post-correction lane weights. Added an "Evidence Sufficiency Review — result and fixed synthesis boundaries" section and updated the Stage C stop point; `updated` → 2026-07-21; `HIS-002-GATE-2` added to `related`.
- `governance/WORK_BOARD.md`, `governance/PROJECT_STATE.md`, `governance/NEXT_ACTION.md` — Gate 2 recorded PASSED; next deliverable = `REV-HIST-002` synthesis (then Gate 3); Matrix HIS-002 verdicts and any Pattern promotion remain blocked until after Gate 3.

Fixed synthesis boundaries `REV-HIST-002` must carry (RA-imposed):
- **PAT-001** — coexisting divergence only, not a matched-cohort value transfer.
- **PAT-002** — a US 1920s national physical overbuild is not supported; the 1930s slack is mainly Depression demand shock + pre-1929 pipeline capacity.
- **PAT-003** — index-tier dispersion exists but is absorbed by market beta; the security-level financing/entry mechanism remains Undecidable-pending-access.

Note:
- No historical synthesis written yet, no Pattern Validation Matrix verdict update, no Pattern promotion, no `MAP-001`/`THS-001`, no AI-era mapping or investment conclusion. `PAT-003` stays `validated-in-one-cycle`; `PAT-001`/`PAT-002` stay `draft`; no Pattern is `active`. The bounded access escalation (Moody's PU manuals S-012 + Taylor 1962 S-011 + a browser HathiTrust session for FTC S-005) remains open.

## 2026-07-20 — HIS-002 Stage C: Evidence Ledger complete

Built under the Research Architect's Source Verification Review (Stage B PASSED; Stage C AUTHORIZED, with the (b)-base + bounded-parallel-escalation path). Executed by claude-code via four parallel extraction agents (curl + pypdf/bs4/xlrd), real data from open sources only. Verification/extraction, not verdicts.

Added:
- `knowledge/industrial-revolutions/HIS-002_EVIDENCE_LEDGER.md` (`id: HIS-002-EVIDENCE-LEDGER`, `status: draft`) — **58 `E-###` claims** across four auditable lanes (Supports / Weakens / Rejects / Undecidable-pending-access) for `PAT-001`/`PAT-002`/`PAT-003`, each tied to an exact source location. Quantitative Backbone: Cowles tier total-return + price (QB-1), Historical Statistics G-series physical (QB-2), CFC security-level micro-sample (QB-3). Includes an Anti-Confirmation Balance Check and a carried-gaps section. Key evidence recorded (verdicts belong to the Evidence Sufficiency Review): PAT-003 index-tier holding-vs-operating dispersion is real (holding total return −89.8% vs operating −74.6%, Sep-1929→Jun-1932) **but fully explained by static market beta** (E-307), with the security-level mechanism Undecidable-pending-access; PAT-002 US 1920s capacity tracked demand ~1:1 (E-210) and the 1929→1932 utilization drop is ≈55% Depression demand shock (E-208), so the Weakens/Rejects lane is at least as strong as Supports; PAT-001 establishes only coexisting divergence across two different outcome constructs (E-113).

Changed:
- `governance/WORK_BOARD.md`, `governance/PROJECT_STATE.md`, `governance/NEXT_ACTION.md` — Stage C recorded complete; next review = Evidence Sufficiency Review; historical synthesis and Matrix HIS-002 verdicts remain blocked pending that review.

Source discipline honored (RA Source Verification Review):
- S-005 / S-011 / S-012 bear **no substantive claim** (full text not obtained) — appear only as Undecidable-pending-access pointers. S-016 not load-bearing (orientation only). S-019 supporting adjacency. S-014 non-load-bearing financing-efficiency counter only, never realized-return evidence. Every S-008 return claim retains the electric/gas-mix, index-construction, base-convention (inception=100, not 1926=100), and survivorship caveats.
- PAT-001 = coexisting divergence only; PAT-002 physical-overbuild rests on capacity/output/utilization (no equity-decline/impairment proxy); PAT-003 index-tier dispersion is not treated as `Supports` for the Pattern (security-level module Undecidable-pending-access).

Note:
- No historical synthesis, no Pattern Validation Matrix verdict update, no Pattern promotion, no `MAP-001`/`THS-001`, no AI-era mapping or investment conclusion. `PAT-003` stays `validated-in-one-cycle`; `PAT-001`/`PAT-002` stay `draft`; no Pattern is `active`. Evidence origin held to the United States, c. 1900–1935.

## 2026-07-20 — HIS-002 Stage B: Source Acquisition & Verification complete

Executed by claude-code under the Research Architect's Stage A review verdict ("PASSED WITH STAGE B CONDITIONS"). Every Tier 1 source was fetched through the session proxy and the actual object opened/parsed (curl + pypdf / bs4 / xlrd, via four parallel verification agents). Verification only — no Evidence Ledger, synthesis, Mapping, Thesis, or Pattern promotion.

Changed:
- `knowledge/industrial-revolutions/HIS-002_SOURCE_REGISTER.md` — appended a "Stage B — Source Acquisition & Verification (verified-source readiness package)" section: per-Tier-1-source readiness records (identity, access + HTTP, exact object, tables/datasets, method/units, Pattern/outcome use, operating-vs-holding classification, load-bearing, gaps); priority-order verdicts; a bibliographic corrections log; the FTC S-005 index-first acquisition map; and a bounded access-escalation recommendation. Stage A content (Codex) left intact; frontmatter gains `stage_b_verification_lead: claude-code`, `updated` → 2026-07-20.
- `governance/WORK_BOARD.md`, `governance/PROJECT_STATE.md`, `governance/NEXT_ACTION.md` — Stage B recorded complete; next review = Source Verification Review; Stage C blocked pending that review.

Key verdicts (all evidence-graded from objects actually reached):
- **PAT-003 return feasibility — FEASIBLE-BUT-BOUNDED.** The Cowles data (Yale SOM ICF, open) yields a monthly total-return series split by operating (Series C-11) vs holding (C-16) tier vs all-stocks control (C-1), 1900–1935 — refuting Stage A's concern that the tiers could not be separated (Gate 1 escalation conditions #1 and #2 not met at the index tier). The security-level extension (issuance vintage / capital structure / individual delistings) is blocked on Moody's Public Utility Securities manuals (HathiTrust Cloudflare-403; not on archive.org) and the paywalled Taylor 1962 Insull study → bounded access escalation recommended, not the blanket PAT-003 escalation.
- **PAT-002 physical compatibility — COMPATIBLE-BUT-BOUNDED.** Capacity (kW), output (kWh), and a native utilization series (Historical Statistics G-204) are defined in consistent units with ownership separable (private vs public 1902; municipal 1920), no price proxy needed; clean annual data from ~1920.
- **PAT-001 matched-window — MATCHED-WINDOW-EXISTS** (~1900–1935, anchored by NBER 28076 + David & Wright), with the honesty caveat that the overlap is temporal across different outcome constructs (productivity vs investor return).

Bibliographic corrections logged: S-007 citation "S. Doc. 238" is unverified/conflated (real docs: S. Doc. 91 / S. Doc. 146); S-014 = Schrade & Walls (IAEE 2005 → J. Energy & Development 2006), a cost-of-capital argument not a "high returns" series, remains NON-load-bearing; S-016 canonical = Oxford ESH WP _033 (1999, rev. 2005); S-019 = Gaggl, Gray, Marinescu & Morin (Labour Economics 2020); S-020 correct DOI 10.1257/000282803769206377.

Note:
- No Evidence Ledger, historical synthesis, Mapping, Thesis, or Pattern promotion. Stage C not authorized. `PAT-003` remains `validated-in-one-cycle`; `PAT-001`/`PAT-002` remain `draft`; no Pattern is `active`. Evidence origin held to the United States, c. 1900–1935.

## 2026-07-16 — HIS-002 Gate 1 confirmed passed; Stage A unblocked

Changed:
- `governance/HIS-002_GATE_1_REVIEW.md` — recorded the Research Architect's confirmed-passed re-review and replaced the reconstructed Gate 2+ escalation list with the original six conditions verbatim.
- `governance/DECISIONS.md` — appended DEC-014, authorizing Stage A after the confirmed re-review and completed DEC-013 prerequisite.
- `governance/PROJECT_STATE.md`, `governance/NEXT_ACTION.md`, `governance/WORK_BOARD.md` — reconciled the canonical state: Gate 1 and the Single-Cycle Pattern Validation prerequisite are complete; `HIS-002_RESEARCH_EXECUTION_PLAN.md` is binding; Stage A Source Orientation is active.

Note:
- No historical evidence claim was added, no Pattern status changed, and no Mapping or Thesis was created.

## 2026-07-14 — Sprint 1: HIS-002 Research Execution Plan authored

Added:
- `knowledge/industrial-revolutions/HIS-002_RESEARCH_EXECUTION_PLAN.md` (`id: HIS-002-PLAN`, `status: draft`) — the operational plan implementing `governance/HIS-002_RESEARCH_BRIEF.md` §8.4. §4 defines explicit, parallel evidence searches for all four cross-cycle outcomes (Supports / Weakens / Rejects / Undecidable) for each of `PAT-001`, `PAT-002`, and `PAT-003`, testing the post-Single-Cycle-Validation (DEC-013) narrowed mechanisms: PAT-001's two-ledger core (operating-profit as supporting sub-mechanism); PAT-002's two separated claims (financing-side impairment vs. the physical-overbuild load-bearing gap, with equity-price decline barred as an overbuild proxy); PAT-003's cohort/vintage/financing-tier/capital-structure dispersion with a broad-market control. Includes anti-confirmation controls (balanced four-lane search budget, Reject/Weaken evidence first-class, Undecidable as a real verdict, mechanism-not-shape rule, pre-synthesis completeness check), an `E-###` evidence-ledger claim-ID scheme distinct from HIS-001's `C-###`, the operating-vs-holding-company value-separation discipline, a ≥3 named failure-case quota, an open-access-first source strategy, staged stopping conditions, and an explicit out-of-scope section (no evidence yet, no Mapping/Thesis, no promotion). Internally checked against the approved brief.

Changed:
- `governance/WORK_BOARD.md`, `governance/PROJECT_STATE.md`, `governance/NEXT_ACTION.md` — Execution Plan recorded as authored and internally checked; the sole remaining gate before broad HIS-002 evidence collection is now the Gate 1 re-review confirmation.

Note:
- No evidence collected. No Source Register, Evidence Ledger, or historical synthesis created. No Pattern created or promoted (dispositions unchanged from DEC-013). No `MAP-001`, `THS-001`, AI mapping, or investment recommendation. No AI-era content in the plan (verified). Broad evidence collection remains blocked pending the Gate 1 re-review.

## 2026-07-14 — Sprint 1: Single-Cycle Pattern Validation (HIS-001) applied (DEC-013)

The Research Architect (ChatGPT) executed the Single-Cycle Pattern Validation Gate introduced by DEC-012 §11.2, relayed by the User (Investment Committee). Dispositions applied to the three candidate Patterns and recorded as binding governance.

Added:
- `governance/HIS-001_SINGLE_CYCLE_PATTERN_VALIDATION.md` (`id: HIS-001-SCPV`) — full gate record: verdict (PASSED), per-Pattern dispositions, gate interpretation.

Changed:
- `patterns/PAT-001_SOCIAL_VALUE_INVESTOR_RETURN_DIVERGENCE.md` — remains `status: draft`. Core mechanism narrowed to "measurable social or downstream value and direct-investor return are distinct ledgers and can diverge materially"; enterprise operating-profit divergence demoted to a supporting sub-mechanism, not a required third matched leg; cross-geography/cross-period/unmatched-cohort limitations preserved.
- `patterns/PAT-002_CAPITAL_CYCLE_OVERBUILD.md` — remains `status: draft`. Two claims separated explicitly: (1) financing-side capital overcommitment → construction lag → investor impairment (supported within HIS-001); (2) physical capacity exceeding near-term demand/utilization (not fully measured — load-bearing gap). Added an explicit falsification condition; added a caution that equity-price decline alone is not evidence of physical overbuild.
- `patterns/PAT-003_ENTRY_TIMING_AND_FINANCING_STRUCTURE.md` — **`status: draft` → `validated-in-one-cycle`**. Recorded originating-cycle bounds (London-listed railway ordinary equities; 1843–1850; partial-payment/compulsory-call financing; authorization-cohort timing; subscription-to-first-post-authorization-call measurement); YNM money-weighted gap marked precision-only, not load-bearing; added the Research Architect's verbatim falsification statement. Not `active`; does not count toward the Phase 3 gate.
- `governance/DECISIONS.md` — appended DEC-013 (the three dispositions + gate interpretation).
- `patterns/PATTERN_VALIDATION_MATRIX.md` — HIS-001 column now records the DEC-013 dispositions; PAT-003 Current Status → `validated-in-one-cycle`.
- `governance/WORK_BOARD.md`, `governance/PROJECT_STATE.md`, `governance/NEXT_ACTION.md` — updated: Single-Cycle Pattern Validation PASSED; next research deliverable is `HIS-002_RESEARCH_EXECUTION_PLAN.md`.

Note:
- No broad evidence collection begun. No Source Register, Evidence Ledger, or historical synthesis. No `MAP-001`, `THS-001`, AI mapping, or investment recommendation. `validated-in-one-cycle` is a single-cycle status, not `active`; PAT-001/PAT-002 remain `draft`. Per DEC-012 §11.2, PAT-001/PAT-002 may be tested in HIS-002 while `draft` but cannot advance directly to `cross-cycle-candidate`; PAT-003 may enter formal cross-cycle testing via HIS-002.

## 2026-07-14 — Sprint 1: Gate 1 revisions applied + Gate 1 review recorded (DEC-012)

Research Architect (ChatGPT) completed Gate 1 — HIS-002 Research Design Review and returned **PASS WITH CONDITIONS**, with explicit rulings on the three open §11 questions and 8 required revisions. All 8 revisions applied in this same change set; Gate 1 review recorded as a governance asset; §11 rulings canonicalized into the brief and DECISIONS.md.

Added:
- `governance/HIS-002_GATE_1_REVIEW.md` (`id: HIS-002-GATE-1`) — full Gate 1 review record: verdict, per-§9-criterion assessment, rulings on §11.1/§11.2/§11.3, 8 required revisions, Gate 2+ escalation conditions.

Changed:
- `governance/HIS-002_RESEARCH_BRIEF.md` — §8 canonicalized to four-label vocabulary (Supports/Weakens/Rejects/Undecidable); §8.1/§8.2/§8.3 Supports, Rejects, and Undecidable criteria rewritten to test mechanism rather than reproduce HIS-001's empirical shape; new §8.4 Anti-Confirmation Rule; new §12 Resolved Research-Design Decisions recording the three §11 rulings.
- `governance/DECISIONS.md` — appended DEC-012: §11.1/§11.2/§11.3 rulings + Gate 1 verdict + the §11.2 programmatic consequence (Single-Cycle Pattern Validation gate required before HIS-002 evidence collection).
- `governance/WORK_BOARD.md` — Active section: next review changed to Gate 1 re-review (PASS WITH CONDITIONS); scope updated to reflect US-only origin and DEC-012 consequence.
- `governance/PROJECT_STATE.md` and `governance/NEXT_ACTION.md` — updated to reflect: Gate 1 verdict (PASS WITH CONDITIONS), §11 rulings now resolved, new Single-Cycle Pattern Validation (HIS-001) gate identified, HIS-002 evidence collection still blocked pending Gate 1 re-review confirmation.

Note:
- No evidence collection, Source Register, Evidence Ledger, or historical synthesis begun. No Pattern created, promoted, or content-edited. No `MAP-001`, `THS-001`, AI mapping, or investment recommendation. PAT-001–PAT-003 remain `status: draft`, `confidence: low`. Gate 1 re-review required (verdict must be confirmed PASSED) before HIS-002 evidence collection may begin; even then, a separate Single-Cycle Pattern Validation gate must pass first per DEC-012 §11.2.
- One documented gap: the handoff package referenced the Research Architect's six Gate 2+ escalation conditions but did not transcribe their verbatim text, so the escalation section in `HIS-002_GATE_1_REVIEW.md` is reconstructed by the Repository Operator and flagged for confirmation at the Gate 1 re-review rather than presented as ChatGPT's verbatim wording.

## 2026-07-14 — Governance: PI Agent role registered (DEC-011)

Added:
- `governance/AGENTS.md` — new role "PI Agent — Operating System / Continuity Agent" and a "Default Task Routing" section. Non-committing continuity/routing layer; GitHub authoritative; hard limits (no Pattern promotion, no investment conclusions, no methodology changes, no parallel governance).

Changed:
- `governance/DECISIONS.md` — appended DEC-011.
- `governance/WORK_BOARD.md` — governance note: PI Agent role registered (DEC-011); no research task state change.

Note:
- No research asset, Pattern, Mapping, or Thesis created or modified. No gate advanced. Repository operator remains Claude Code; this adds a continuity/routing role, not a second repository operator.

## 2026-07-14 — Sprint 1: HIS-002 Research Design / Pattern Validation

Research OS architecture frozen for this sprint (Research Executor role). `HIS-002` — Electricity, Grid Infrastructure, and Industrial Electrification — opened as a cross-cycle validation case for `PAT-001`–`PAT-003`. No Pattern assumed true; no evidence collected.

Added:
- `governance/HIS-002_RESEARCH_BRIEF.md` (`id: HIS-002-BRIEF`) — primary research question (how social value, capital cycles, financing structure, and entry timing affected value creation/capture/impairment during US electricity/grid buildout, and what this evidence does to `PAT-001`–`PAT-003`); bounded to the United States, c. 1900–1935 (deliberately a different institutional/regulatory environment from `HIS-001`'s British frame, per Framework §4.2); included/excluded infrastructure layers; evidence, counter-evidence, and failure-case requirements (≥3 named failure/impairment cases); investor-return requirements (cohort-level where obtainable, `undecidable` where not — no interpolation); explicit operating-profit-vs-shareholder-return distinction naming holding-company pyramiding as the era's candidate divergence mechanism (distinct from `HIS-001`'s accounting-practice mechanism); explicit Supports/Weakens/Rejects/Undecidable validation criteria for each of `PAT-001`, `PAT-002`, `PAT-003`; Gate 1 pass criteria. Three open research-design questions logged for Research Architect ruling (§11). No evidence collection begun.
- `patterns/PATTERN_VALIDATION_MATRIX.md` — the single canonical cross-Pattern tracking table (Pattern × Revolution), instantiating `governance/PATTERN_VALIDATION_FRAMEWORK.md` §3 in one location rather than duplicating a matrix inside each `PAT-###` file. HIS-001 column populated from each Pattern's own existing Pattern Eligibility table and `REV-HIST-001`'s hypothesis verdicts, not simplified to a uniform rating: `PAT-001` and `PAT-002` recorded `Supports (partial)`; `PAT-003` recorded `Supports`. HIS-002/HIS-003 columns: pending. No Pattern promoted.

Changed:
- `governance/PATTERN_VALIDATION_FRAMEWORK.md` — one minimum-necessary completeness fix: §3 now defines how an `Undecidable` cross-cycle result is recorded (in the Notes column, not as a new table column), and clarifies it neither counts toward promotion nor blocks `cross-cycle-candidate` entry. No other change; lifecycle, matrix template, and promotion requirements unchanged. Assessed as internally complete and ready for Research Architect methodology review; that formal sign-off itself was not part of this sprint.
- `governance/WORK_BOARD.md` — Active section replaced with Sprint 1; `HIS-002` moved from Backlog to Active with its refined title; next review set to Gate 1 — HIS-002 Research Design Review.
- `governance/PROJECT_STATE.md`, `governance/NEXT_ACTION.md` — updated to reflect Sprint 1's state, the three open research-design questions, and the Framework readiness assessment.
- `governance/REPOSITORY_INDEX.md` — added entries for `HIS-002_RESEARCH_BRIEF.md` and `PATTERN_VALIDATION_MATRIX.md`.

Note:
- No evidence collection, Source Register, Evidence Ledger, or historical synthesis for `HIS-002`. No new Pattern created; no existing Pattern promoted or content-edited. No `MAP-001`, `THS-001`, AI mapping, or investment recommendation. Governance, roles, repository structure, and the research lifecycle were not redesigned.

## 2026-07-14 — Sprint 0.1: Repository Integrity Fix

Following the Repository Architecture Review verdict on Sprint 0's audit (PASS WITH CONDITIONS), applied a bounded set of the recommended fixes.

Changed:
- `governance/HIS-001_RESEARCH_BRIEF.md` — `id: HIS-001` → `id: HIS-001-BRIEF`; `related` no longer lists `MAP-001`/`THS-001` (now lists `HIS-001` instead, pointing back to the task); added an outcome annotation to §9D reconciling the four originally-planned Pattern concepts against the three actually drafted.
- `knowledge/industrial-revolutions/HIS-001_RESEARCH_EXECUTION_PLAN.md` — `id: HIS-001` → `id: HIS-001-PLAN`; `related` no longer lists `PAT-004`/`MAP-001` (now lists `HIS-001` instead); added the matching outcome annotation to the file-plan table.
- `governance/HIS-001_GATE_1_REVIEW.md` — `id: HIS-001` → `id: HIS-001-GATE-1`.
- `governance/FRONTMATTER_STANDARD.md` — canonical schema example updated to `id: HIS-001-BRIEF` (it reproduces the brief's frontmatter), with a new note distinguishing the task ID (`HIS-001`) from a document's own suffixed ID.
- `workflows/THESIS_WORKFLOW.md` — `status: locked` → `status: draft`; body note now reads "This workflow is not usable until Phase 3 entry gates in `RESEARCH_SCOPE.md` are satisfied," replacing the redundant "Status: LOCKED" line.
- `README.md` — Status section rewritten (Phase 1 complete; `HIS-001` complete through Gate 3; `REV-HIST-001` stable; `PAT-001`–`003` draft; Pattern Validation Framework awaiting review; Mapping/Thesis blocked; `HIS-002` not authorized). Core Loop replaced with `Research Question → Source Verification → Evidence Ledger → Historical Synthesis → Candidate Pattern → Cross-Cycle Validation → Historical-to-Current Mapping → Investment Thesis → Prediction → Monitoring and Review`. Start Here now links to `governance/PROJECT_STATE.md`, `governance/NEXT_ACTION.md`, `governance/REPOSITORY_INDEX.md`.
- `governance/REPOSITORY_AUDIT.md` — Findings 1–5 marked RESOLVED — Sprint 0.1 with disposition notes; Findings 6–9 remain open (deferred, outside this sprint's bounded scope).
- `governance/PROJECT_STATE.md`, `governance/NEXT_ACTION.md` — updated to reflect Sprint 0.1 completion, `HIS-001` marked complete, and active task set to Pattern Validation Framework methodology review; removed the stale claim that the second Pattern Review revision was unspecified.
- `governance/WORK_BOARD.md` — Sprint 0, Sprint 0.1, and `HIS-001` moved to Done; Active now holds only "Pattern Validation Framework — methodology review."

Verified, not changed:
- `patterns/PAT-002_CAPITAL_CYCLE_OVERBUILD.md` — the second of the two Pattern Review revisions ("apply two minor Pattern revisions") is the operational definition of overbuild. Verified it was already present in the file's Mechanism section (the authorization→subscription→called→paid→expenditure→completed→impaired chain, kept strictly distinct) since the file's original drafting. No content change was needed; recorded as complete.

Note:
- Scope was bounded to the eight numbered fixes in the Repository Architecture Review's instruction. No new historical research, no Pattern promotion, no AI mapping, no investment thesis. `HIS-002`, `MAP-001`, and `THS-001` remain blocked — `HIS-002` awaits Research Architect review of `governance/PATTERN_VALIDATION_FRAMEWORK.md`'s methodology, the sole remaining gate.
- Repository Audit Findings 6–9 (two orphaned files, an undocumented HIS-001 directory-placement rule, a template `status` schema gap, and the disclosed `DECISIONS.md`/`DECISION_LOG.md` naming overlap) were left open — they were not named in the Repository Architecture Review's eight-item instruction.

## 2026-07-13 — Sprint 0: Repository Consolidation

Added:
- `governance/PROJECT_STATE.md` — one-page current-state snapshot: phase, sprint, gate-by-gate verdict table, stable/draft asset lists, blocked work, known evidence gaps, next required review.
- `governance/REPOSITORY_INDEX.md` — directory map of every major directory with a one-sentence description of each key file, plus a numbered reading order for a new agent.
- `governance/ROADMAP.md` — completed/current/remaining phases with entry and exit criteria for each, including a Phase 3 gate-progress table (1/3 historical assets, 0/5 cross-cycle Patterns, 0/3 Mappings, 0/1 monthly reviews).
- `governance/DECISION_LOG.md` — narrative companion to `governance/DECISIONS.md`, summarizing the six architectural-decision themes the Research Architect asked to have recorded (GitHub as canonical source, single active research question, gate review workflow, Pattern lifecycle, MAP-001 suspension, phase locking), each citing its authoritative `DEC-###` entry. Explicitly not a competing ledger — `DECISIONS.md` remains authoritative on conflict.
- `governance/NEXT_ACTION.md` — one-page operational handoff: current sprint, objective, blockers, assigned responsibilities, immediate next action.
- `governance/REPOSITORY_AUDIT.md` — full repository integrity audit (35 files inspected): frontmatter completeness, ID consistency, relative-link resolution, filename-reference/orphan check, status-value consistency, duplicate-template check, naming-convention compliance. Result: 0 high, 1 medium-high (triple `id: HIS-001` collision across brief/plan/gate-review), 4 medium (stale `PAT-004`/`MAP-001`/`THS-001` references in the brief and execution plan's `related` frontmatter; originally-planned Pattern concepts no longer matching the Patterns actually drafted; `workflows/THESIS_WORKFLOW.md`'s non-standard `status: locked`; stale `README.md` status section and Core Loop diagram), 4 low (two orphaned files — `templates/SOURCE_REGISTER_TEMPLATE.md`, `workflows/GIT_WORKFLOW.md`; undocumented HIS-001-family directory-placement rule; template `status: draft` schema gap; stale illustrative examples in `NAMING_AND_IDS.md`), 1 disclosed informational finding (naming overlap this sprint's own `DECISION_LOG.md` creates with `DECISIONS.md`'s internal title). No medium/high finding was automatically fixed, per explicit instruction.

Changed:
- `governance/DECISIONS.md` — appended `DEC-007` (multi-gate evidence pipeline formalized), `DEC-008` (Pattern lifecycle adopted; no Pattern reaches `active` on single-cycle evidence), `DEC-009` (MAP-001 authorization withdrawn; Mapping gated behind Pattern Validation), `DEC-010` (repository consolidation sprints required before phase progression) — recording decisions already made in substance but not yet logged as formal entries.
- `governance/WORK_BOARD.md` — added a Sprint 0 entry under Active; HIS-001 marked paused awaiting Research Architect review before any further Pattern/Mapping/HIS-002 work.

Note:
- Scope strictly limited to governance, repository integrity, and operating-system quality, per instruction. No new historical research, no Pattern promotion, no AI mapping, no investment thesis, and no new research asset was created or modified — `knowledge/`, `patterns/`, and `research/` content is untouched this sprint.
- Verified before starting: the sole pending item from the prior Pattern Review (the `PAT-001` wording revision) was already committed (`d0b7910`); the working tree was clean at sprint start.

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
## 2026-07-16 — HIS-002 Stage A Source Orientation complete

Added:
- `knowledge/industrial-revolutions/HIS-002_SOURCE_REGISTER.md` — bounded 20-source candidate landscape for US electricity generation/grid infrastructure and industrial electrification, c. 1900–1935. Sources are mapped to `PAT-001`/`PAT-002`/`PAT-003` and to Supports/Weakens/Rejects/Undecidable lanes. The register separates bibliographic/access orientation from evidentiary claims, defines the access taxonomy, identifies a five-item Stage B priority queue, and preserves genuine gaps around security-tier returns, entity linkage, physical utilization, matched-period value/return evidence, and negative-control cases.

Changed:
- `governance/PROJECT_STATE.md`, `NEXT_ACTION.md`, and `WORK_BOARD.md` — Stage A marked complete and awaiting Source Orientation review; Stage B and Stage C remain unauthorized.

Note:
- No Evidence Ledger claim rows, historical synthesis, Pattern promotion, AI Mapping, or Thesis were created. PAT-003 remains `validated-in-one-cycle`; PAT-001/PAT-002 remain `draft`.
