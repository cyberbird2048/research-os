---
type: governance
title: Next Action
status: active
created: 2026-07-13
updated: 2026-07-14
---

# Next Action

One-page operational handoff. If you read only one file to know what to do right now, read this one — then confirm against `governance/WORK_BOARD.md`, which is the live source if the two disagree.

## Current Sprint

Sprint 1 — HIS-002 Research Design / Pattern Validation. `governance/HIS-002_RESEARCH_BRIEF.md` is drafted; no evidence collection has begun. `patterns/PATTERN_VALIDATION_MATRIX.md` created to track `PAT-001`–`PAT-003` across revolutions.

## Current Objective

Get `HIS-002_RESEARCH_BRIEF.md` through **Gate 1 — HIS-002 Research Design Review**, resolving the three open research-design questions logged in the brief's §11 first.

## Current Blockers

- **`HIS-002` evidence collection is blocked** until Gate 1 passes.
- **Three open research-design questions require a Research Architect ruling** before Gate 1 can pass (`governance/HIS-002_RESEARCH_BRIEF.md` §11): (1) whether the brief's five-way supported/partially-supported/weakened/rejected/undecidable vocabulary maps correctly onto the Framework's Supports/Weakens/Rejects/Undecidable columns; (2) whether `PAT-001`–`PAT-003` need a formal `draft` → `validated-in-one-cycle` promotion decision before or alongside `HIS-002`'s cross-cycle test; (3) confirmation that bounding `HIS-002` to the United States (rather than, say, the UK) satisfies the intended institutional-diversity requirement.
- **Formal confirmation of the Pattern Validation Framework's own methodology review** has not been separately recorded — this sprint closed one internal-completeness gap (Undecidable handling in §3) and assessed the framework as ready, but did not itself constitute the Research Architect's review.
- **Historical-to-AI Mapping is blocked** until a Pattern reaches `cross-cycle-candidate` — unaffected by this sprint.
- **One item remains genuinely open** (not blocking): `MAP-001`'s structural spec was never supplied before that task was withdrawn.
- **Two items from the Sprint 0 audit remain genuinely open, deferred by design**: an HIS-001-family directory-placement rule and a template `status` schema clarification — see `governance/REPOSITORY_AUDIT.md` Findings 7 and 8.

## Assigned Responsibilities

Per `governance/AGENTS.md`: GitHub is the source of truth; Claude Code is Research Lead/Repository Operator (executes, does not self-authorize scope changes); the Research Architect (ChatGPT) designs research and reviews gates; Codex reviews evidence and logic; the User is the Investment Committee and final decision-maker. Sprint 1's work — the HIS-002 brief and Pattern Validation Matrix — was executed by Claude Code under explicit Research Architect instruction, framed as research design only, pending Gate 1.

## Immediate Next Action

1. Research Architect rules on the three open questions in `governance/HIS-002_RESEARCH_BRIEF.md` §11.
2. Research Architect conducts Gate 1 — HIS-002 Research Design Review against the brief's own §9 pass criteria.
3. Until Gate 1 passes, no agent should collect `HIS-002` evidence, create a Source Register or Evidence Ledger, draft a historical synthesis, create or promote any Pattern, or create `MAP-001`/`THS-001`.
