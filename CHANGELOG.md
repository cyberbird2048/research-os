# Changelog

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
