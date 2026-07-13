---
type: governance
title: Decision Log — Narrative Summary
status: active
created: 2026-07-13
updated: 2026-07-13
---

# Decision Log — Narrative Summary

**This file is not the authoritative decision record.** `governance/DECISIONS.md` is: it is the append-only, atomic ledger where every `DEC-###` entry lives, one per decision, never edited retroactively. This file is a companion — a prose synthesis of the same decisions, grouped by theme so a new agent or the Investment Committee can read "what has been decided and why" in a few minutes without walking the full ledger. If this file and `governance/DECISIONS.md` ever disagree, `DECISIONS.md` wins. See `governance/REPOSITORY_AUDIT.md` for the naming overlap this creates and why it was not resolved by merging or renaming either file in this sprint.

## GitHub as canonical source

GitHub is the single source of truth for CyberBird Research OS (`DEC-001`). Any other view — a local Obsidian vault, a chat transcript, a cached document — is a read-only convenience, not an authoritative copy. When any two representations disagree, the state committed to GitHub's `main` branch governs.

## Single active research question

Phase 2 (Historical Research) runs exactly one historical research task at a time (`DEC-002`). `HIS-001` was the first and, until a future decision authorizes otherwise, the only task that has been open. This prevents the repository from accumulating shallow, half-evidenced research across many revolutions simultaneously instead of one deep, well-evidenced chain.

## Gate review workflow

Historical research does not move from question to conclusion in one step. It passes through a fixed sequence of gates and stages, each with its own reviewer and pass/fail verdict (`DEC-007`, elaborating on the process first used for `HIS-001` and described in `workflows/RESEARCH_WORKFLOW.md`):

Gate 1 (Research Design) → Stage A (Source Orientation) → Stage B (Source Verification) → Stage C (Evidence Ledger) → Gate 2 (Evidence Sufficiency) → Historical Synthesis → Gate 3 (Historical Stability) → Candidate Patterns → Pattern Review.

Every gate in this sequence has now been run at least once, and every one of them returned a "PASS WITH CONDITIONS" or "PASS WITH MINOR REVISIONS" verdict rather than an unconditional pass — the repository's evidence discipline has, so far, always required at least a minor correction before proceeding.

## Pattern lifecycle

A Pattern is not credible after one historical episode. `governance/PATTERN_VALIDATION_FRAMEWORK.md` defines six lifecycle states (`draft → validated-in-one-cycle → cross-cycle-candidate → active → stable → archived`), and `DEC-008` makes it binding that no Pattern reaches `active` on single-cycle evidence. This is why `PAT-001`, `PAT-002`, and `PAT-003` — despite being carefully derived from a well-evidenced synthesis — remain `status: draft`, `confidence: low`: they describe mechanisms observed once, in the steam and railway era, and have not yet been checked against an independent revolution.

## Suspension of MAP-001 pending cross-cycle validation

An earlier authorization to draft `MAP-001_RAILWAY_MANIA_AND_AI_INFRASTRUCTURE.md` — the first Historical-to-AI Mapping — was withdrawn before any file was created (`DEC-009`). The reasoning: mapping a Pattern to the present AI cycle is an investment-relevant analogy, and drawing that analogy from a Pattern validated in only one historical cycle would smuggle unvalidated inference into what should be a disciplined comparison. Mapping work stays paused until a Pattern reaches at least `cross-cycle-candidate`.

## Phase locking rules

Phase 3 (the Investment Thesis Engine) is locked and cannot open early no matter how strong any single asset looks (`DEC-003`). Its entry gates — 3 completed historical assets, 5 cross-cycle validated Patterns, 3 Mappings, 1 monthly review, a demonstrated repeatable Phase 2 workflow — are unmet by a wide margin (currently 1, 0, 0, 0, and "run once" respectively; see `governance/ROADMAP.md`). Separately, `DEC-010` establishes that a consolidation sprint (like this one) runs before Phase 2 opens a second historical revolution or Phase 3 is approached, so that repository integrity is checked deliberately rather than assumed.

## Reading this alongside `DECISIONS.md`

Every claim above traces to a specific `DEC-###` entry cited in parentheses. If a future decision changes any of this, the change is recorded first in `governance/DECISIONS.md` as a new entry (never by editing an old one), and this file is then updated to reflect it — in that order, not the reverse.
