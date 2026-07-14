---
type: governance
title: Repository Audit — Sprint 0 (Sprint 0.1 disposition applied)
status: active
created: 2026-07-13
updated: 2026-07-14
---

# Repository Audit — Sprint 0 (Sprint 0.1 disposition applied)

Point-in-time integrity audit of the entire repository (35 tracked files as of Sprint 0). Performed by direct inspection — full file inventory, frontmatter extraction from every Markdown file, relative-link resolution, ID/status cross-checks, and filename-reference search for every non-template, non-workflow asset.

**Sprint 0 policy: no medium- or high-severity issue was automatically fixed at the time of the original audit.** Each entry stated a recommended fix pending explicit authorization. The Repository Architecture Review (2026-07-14) returned **PASS WITH CONDITIONS** and authorized Sprint 0.1 to apply a bounded set of these recommended fixes. Findings 1–5 below are now marked **RESOLVED — Sprint 0.1**; Findings 6–9 remain open, deferred by the Research Architect's own bounded scope for Sprint 0.1.

## Summary

| Severity | Count | Resolved (Sprint 0.1) | Open |
|---|---|---|---|
| High | 0 | — | — |
| Medium-High | 1 | 1 | 0 |
| Medium | 4 | 4 | 0 |
| Low | 4 | 0 | 4 |
| Informational (by-design, disclosed) | 1 | 0 | 1 |

## Findings

### 1. [Medium-High] Three documents independently declare `id: HIS-001`

**Affected files:** `governance/HIS-001_RESEARCH_BRIEF.md`, `governance/HIS-001_GATE_1_REVIEW.md`, `knowledge/industrial-revolutions/HIS-001_RESEARCH_EXECUTION_PLAN.md` (all frontmatter `id:` field).

The brief, the Gate 1 review, and the execution plan are three distinct deliverables but all carry the bare ID `HIS-001`, while sibling deliverables in the same family use suffixed IDs (`HIS-001-SOURCE-REGISTER`, `HIS-001-EVIDENCE-LEDGER`). It is not documented in `governance/NAMING_AND_IDS.md` whether `HIS-001` denotes the task as a whole (in which case multiple documents sharing it may be intentional) or should uniquely identify one asset. The inconsistency is that some deliverables get a unique suffixed ID and others do not, with no stated rule for which.

**Recommended fix:** Research Architect decides the rule — e.g., `HIS-001` names the task only, and the brief/plan/review each get their own suffixed ID (`HIS-001-BRIEF`, `HIS-001-PLAN`, `HIS-001-GATE-1`), consistent with the source register and evidence ledger. Then apply it uniformly. Not applied automatically because it changes IDs referenced elsewhere (`WORK_BOARD.md`, `DECISIONS.md`).

**RESOLVED — Sprint 0.1.** `HIS-001` is now the task ID only. `governance/HIS-001_RESEARCH_BRIEF.md` → `id: HIS-001-BRIEF`; `knowledge/industrial-revolutions/HIS-001_RESEARCH_EXECUTION_PLAN.md` → `id: HIS-001-PLAN`; `governance/HIS-001_GATE_1_REVIEW.md` → `id: HIS-001-GATE-1`. All three now list `HIS-001` in `related` (pointing back to the task), matching the convention already used by `PAT-###`, `REV-HIST-001`, and the evidence ledger/source register. `governance/FRONTMATTER_STANDARD.md`'s canonical schema example (reproduced from the brief) was updated to match, with a new note explaining the task-ID-vs-document-ID distinction. Checked: no other file referenced `HIS-001` as if it denoted a specific document rather than the task, so no other cross-reference needed updating.

### 2. [Medium] Stale `related` frontmatter referencing non-existent assets

**Affected files:**
- `governance/HIS-001_RESEARCH_BRIEF.md` frontmatter `related` — lists `MAP-001` and `THS-001`, neither of which exists (`MAP-001` was authorized then withdrawn per `DEC-009`; `THS-001` is Phase-3-locked).
- `knowledge/industrial-revolutions/HIS-001_RESEARCH_EXECUTION_PLAN.md` frontmatter `related` — lists `PAT-004` and `MAP-001`; `PAT-004` was never drafted (only `PAT-001`–`PAT-003` exist, and under different concepts — see Finding 3) and `MAP-001` does not exist.

This is the same class of issue already corrected in `REV-HIST-001_STEAM_AND_RAILWAYS.md`'s frontmatter during the Gate 3 revisions (nonexistent future assets removed from `related`); the brief and execution plan were not in scope for that revision and still carry it.

**Recommended fix:** Remove `PAT-004`, `MAP-001`, `THS-001` from both files' `related` lists (or replace with a prose footnote noting they were originally planned and superseded — see Finding 3 for why deleting outright may lose useful provenance). Deferred to the Research Architect since it touches HIS-001-family documents outside this sprint's authorized scope (governance/repository-integrity only, no research-asset edits).

**RESOLVED — Sprint 0.1.** `PAT-004`, `MAP-001`, `THS-001` removed from both files' `related` frontmatter (Research Architect explicitly instructed not to preserve nonexistent assets there). A prose outcome annotation was added to each file's body instead (see Finding 3's disposition) so the provenance is not lost, just relocated from frontmatter to an explanatory note.

### 3. [Medium] Originally-planned Pattern concepts no longer match the Patterns actually drafted

**Affected files:** `governance/HIS-001_RESEARCH_BRIEF.md` §9D ("Candidate Patterns," listing `PAT-001_INFRASTRUCTURE_BOTTLENECK_CAPTURE`, `PAT-002_SOCIAL_VALUE_VS_INVESTOR_RETURN`, `PAT-003_CAPITAL_CYCLE_OVERBUILD`, `PAT-004_PROFIT_POOL_MIGRATION`); `knowledge/industrial-revolutions/HIS-001_RESEARCH_EXECUTION_PLAN.md`'s file-plan table (same four names).

What was actually drafted, under Gate 3 authorization and titled according to what the evidence actually supported, is a different set: `PAT-001_SOCIAL_VALUE_INVESTOR_RETURN_DIVERGENCE`, `PAT-002_CAPITAL_CYCLE_OVERBUILD`, `PAT-003_ENTRY_TIMING_AND_FINANCING_STRUCTURE`. The concepts originally slotted as `PAT-002` and `PAT-003` were drafted as `PAT-001` and `PAT-002` instead; "Infrastructure Bottleneck Capture" and "Profit Pool Migration" were never drafted; "Entry Timing and Financing Structure" does not appear in the original plan at all. This divergence is expected and appropriate — Patterns were drafted from evidence, not a pre-committed list — but the brief and plan still read as current, which could mislead a new agent into expecting a `PAT-004` is pending.

**Recommended fix:** Add a short annotation (not a rewrite — the original plan has provenance value) to brief §9D and the plan's file-plan table, cross-referencing the Patterns actually drafted and stating the four originally-named concepts were superseded by evidence-driven titling. Deferred — touches HIS-001-family research documents, out of this sprint's scope.

**RESOLVED — Sprint 0.1.** Added an "Outcome annotation" block to brief §9D and to the plan's file-plan table (the original lists were left untouched, per instruction not to rewrite the plan retrospectively). Each annotation names the three Patterns actually drafted and states the disposition of every originally-planned concept: Infrastructure Bottleneck Capture not promoted (insufficient supplier-side evidence); Profit Pool Migration remained undecidable; Social Value vs. Investor Return and Capital Cycle Overbuild were both drafted, under `PAT-001`/`PAT-002` rather than `PAT-002`/`PAT-003`; Entry Timing and Financing Structure (not in the original list) emerged as `PAT-003` from the Evidence Ledger and Historical Synthesis.

### 4. [Medium] `workflows/THESIS_WORKFLOW.md` uses a non-standard `status` value

**Affected file:** `workflows/THESIS_WORKFLOW.md` frontmatter, `status: locked`.

`governance/NAMING_AND_IDS.md` defines exactly four status values (`draft`, `active`, `stable`, `archived`). `locked` is not one of them. It appears intended to mirror `RESEARCH_SCOPE.md`'s "Phase 3: locked," but that conflates the *workflow document's own lifecycle* (is this process definition finished and reviewed?) with the *phase-gate state of when the workflow may be used* (Phase 3 hasn't opened yet) — two different things.

**Recommended fix:** Set `status` to `draft` or `stable` (Research Architect's call, depending on whether the workflow content itself is considered final), and add a body note: "Not usable until Phase 3 opens — see `governance/RESEARCH_SCOPE.md`." Not applied automatically since it requires a judgment call on the workflow's actual completeness.

**RESOLVED — Sprint 0.1.** `status` changed to `draft` (Research Architect's explicit instruction). Body note added: "This workflow is not usable until Phase 3 entry gates in `RESEARCH_SCOPE.md` are satisfied," replacing the redundant "Status: LOCKED" bold line that duplicated the frontmatter.

### 5. [Medium] `README.md` status section and core-loop diagram are stale

**Affected file:** `README.md`, "Status" section and "Core Loop" diagram.

"Status" reads `Historical research: not started`, but Phase 2 has since passed Gates 1–3, produced a stable historical synthesis, and drafted three candidate Patterns. The "Core Loop" diagram (`Evidence → Historical Mapping → Pattern → Investment Thesis → Prediction → Validation → Review`) omits the gate-review stages entirely and shows Patterns feeding Mapping directly, with no Pattern Validation / cross-cycle step — inconsistent with `governance/PATTERN_VALIDATION_FRAMEWORK.md`, adopted this sprint's predecessor.

**Recommended fix:** Update the Status bullets to reflect current Phase 2 progress, and insert a Pattern Validation step in the Core Loop diagram between Pattern and Historical Mapping. README.md is a root-level, non-research file — editing it is arguably within Sprint 0's "governance and repository integrity" remit, but it was left as a recommended fix rather than auto-applied, since Sprint 0's brief listed six specific documents to create/update and did not name README.md among them.

**RESOLVED — Sprint 0.1.** Status section rewritten to reflect Phase 1 complete, `HIS-001` complete through Gate 3, `REV-HIST-001` stable, `PAT-001`–`003` draft, Pattern Validation Framework awaiting review, Mapping/Thesis blocked, `HIS-002` not authorized. Core Loop replaced with `Research Question → Source Verification → Evidence Ledger → Historical Synthesis → Candidate Pattern → Cross-Cycle Validation → Historical-to-Current Mapping → Investment Thesis → Prediction → Monitoring and Review`. Start Here links now point to `governance/PROJECT_STATE.md`, `governance/NEXT_ACTION.md`, and `governance/REPOSITORY_INDEX.md`.

### 6. [Low] Two files are never referenced by name anywhere else in the repository

**Affected files:** `templates/SOURCE_REGISTER_TEMPLATE.md`, `workflows/GIT_WORKFLOW.md`.

Confirmed via a repository-wide search for each filename string outside the file itself: zero hits for either. Both files are otherwise well-formed and not broken; the issue is pure discoverability — a new agent following links from `README.md` or `WORK_BOARD.md` would never land on them without already knowing they exist.

**Recommended fix:** Already partially mitigated this sprint — both are now described in `governance/REPOSITORY_INDEX.md`'s directory map. A further fix (adding them to `README.md`'s "Start Here" list) is left to the Research Architect since it edits a file outside this sprint's named deliverables.

### 7. [Low] No documented rule for HIS-001-family file placement across `governance/` vs `knowledge/`

**Affected files:** `governance/HIS-001_RESEARCH_BRIEF.md`, `governance/HIS-001_GATE_1_REVIEW.md` (in `governance/`) vs. `knowledge/industrial-revolutions/HIS-001_RESEARCH_EXECUTION_PLAN.md`, `HIS-001_SOURCE_REGISTER.md`, `HIS-001_EVIDENCE_LEDGER.md` (in `knowledge/`).

All cross-references between these files resolve correctly today (verified — zero broken links repository-wide), so this is not a functional defect. But no governance document states a rule for which HIS-001 deliverables belong in which top-level directory, which will become ambiguous once `HIS-002` starts and someone has to decide where its brief and gate review go.

**Recommended fix:** Research Architect documents a placement rule in `governance/NAMING_AND_IDS.md` (e.g., "task-definition and gate-review documents live in `governance/`; evidence, source, and synthesis content lives in `knowledge/`"), treating the current `HIS-001` placement as a grandfathered legacy pattern rather than moving files and breaking working references.

### 8. [Low] Template files' `status: draft` may be a schema gap, not a defect

**Affected files:** all seven files in `templates/`.

Every template carries `status: draft`, consistently. `governance/FRONTMATTER_STANDARD.md` does not define what `status` means for `type: template` — the four-value lifecycle (draft/active/stable/archived) is written with research assets and governance documents in mind, not templates, which are either "the current canonical template" or superseded, not a document that itself matures through drafting.

**Recommended fix:** Research Architect clarifies whether templates should use `status: active` (meaning "in current use as the canonical template") instead, or whether `FRONTMATTER_STANDARD.md` should carve out an explicit exception for `type: template`. Purely a documentation clarity issue — nothing in the repository currently branches on a template's status value.

### 9. [Low-Medium, informational — created by this sprint, disclosed rather than hidden] `DECISIONS.md` and the newly created `DECISION_LOG.md` have overlapping names and purposes

**Affected files:** `governance/DECISIONS.md` (frontmatter `title: Decision Log`, H1 `# Decision Log`) and the new `governance/DECISION_LOG.md` (this sprint's required deliverable).

Sprint 0 explicitly required creating `governance/DECISION_LOG.md`. `governance/DECISIONS.md` already existed and already titles itself "Decision Log" internally, despite its filename being `DECISIONS.md`. To reduce ambiguity, `DECISION_LOG.md` was given the differentiated title "Decision Log — Narrative Summary," an explicit disclaimer at its top stating `DECISIONS.md` is authoritative, and a distinct purpose (atomic append-only ledger vs. prose synthesis grouped by theme) rather than being a duplicate ledger. The underlying naming collision (a file named `DECISIONS.md` whose own title is "Decision Log," alongside a new file literally named `DECISION_LOG.md`) still exists and could confuse someone searching by title.

**Recommended fix:** Either rename `DECISIONS.md`'s frontmatter `title` to something clearly distinct (e.g., "Decision Ledger") in a future sprint, or formally merge the two documents. Not done in this sprint per the "do not automatically fix" instruction and because `DECISIONS.md`'s title is pre-existing content outside this sprint's edit scope.

## Clean — No Issues Found

- **Broken internal references:** zero. All 11 relative Markdown links (all located in `governance/WORK_BOARD.md`) resolve to existing files.
- **Duplicate templates:** zero. All seven files in `templates/` have distinct content (verified by line count and content hash).
- **File naming convention violations:** zero. Every governance/workflow document uses `UPPER_SNAKE_CASE.md`; every ID-bearing asset is correctly prefixed with its ID. (The naming standard's own illustrative examples in `governance/NAMING_AND_IDS.md`, lines 34–35, are now stale relative to the actual Pattern titles — see Finding 3 — but this is a documentation-currency issue, not a violation of the naming rule itself.)
- **Duplicated governance content:** none found beyond the disclosed `DECISIONS.md`/`DECISION_LOG.md` overlap (Finding 9), which was created by this sprint's own required deliverable and is explicitly flagged above rather than silently resolved.
- **Missing frontmatter:** none. Every file expected to carry frontmatter carries it; the files without frontmatter (`README.md`, `CHANGELOG.md`, `.github/PULL_REQUEST_TEMPLATE.md`) are all conventionally exempt file types.
- **Orphaned research assets:** none. The evidence ledger, source register, historical synthesis, and all three Patterns are each referenced from `governance/WORK_BOARD.md`.

## Methodology Note

This audit is a snapshot as of 2026-07-13, with Sprint 0.1's fix disposition (2026-07-14) recorded inline against each resolved finding. It does not re-run automatically; a future consolidation sprint should re-run the same checks (full file inventory, frontmatter dump, relative-link resolution, filename-reference search, status-value scan) rather than assume this file stays current — in particular, Findings 6–9 remain open and unverified against any repository changes made after 2026-07-14.
