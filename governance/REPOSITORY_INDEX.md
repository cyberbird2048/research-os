---
type: governance
title: Repository Index
status: active
created: 2026-07-13
updated: 2026-07-14
---

# Repository Index

A map of the repository for a new agent (Claude Code, ChatGPT, Codex, or a future session with no prior context). Read in the order given under "Reading Order," not the order listed below.

## Directory Map

### `governance/`

Rules for how the repository operates: scope, roles, naming, frontmatter, decisions, and the current state snapshot. Nothing in here is historical research content.

| File | One-line description |
|---|---|
| `PROJECT_CONSTITUTION.md` | The repository's purpose, non-negotiable principles, and precedence order when documents conflict. |
| `RESEARCH_SCOPE.md` | The current phase model (Foundation → Historical Research → Investment Thesis Engine) and each phase's entry/exit gates. |
| `OPERATING_PRINCIPLES.md` | Evidence standards, claim classification taxonomy, mandatory counter-evidence/survivorship checks, and the value-separation rule. |
| `NAMING_AND_IDS.md` | ID scheme (`HIS-###`, `REV-HIST-###`, `PAT-###`, etc.), file naming conventions, and the status lifecycle (`draft → active → stable → archived`). |
| `FRONTMATTER_STANDARD.md` | The YAML frontmatter schema every file must carry, and the minimal subset for non-research files. |
| `AGENTS.md` | Roles and responsibilities: GitHub (source of truth), Claude Code (Research Lead/Operator), ChatGPT (Research Architect), Codex (Evidence Reviewer), User (Investment Committee). |
| `WORK_BOARD.md` | Live tracker of task state — Active / Waiting for Review / Backlog / Done. The single place to check "what is happening right now." |
| `DECISIONS.md` | Append-only, atomic ledger of governance decisions, one `DEC-###` per entry. The authoritative record. |
| `DECISION_LOG.md` | Narrative companion to `DECISIONS.md` — the same decisions grouped by theme and explained in prose. Read this for context; read `DECISIONS.md` for the authoritative entry. |
| `PROJECT_STATE.md` | One-page current-state snapshot: phase, sprint, gate status, stable/draft assets, blocked work, evidence gaps. Expected to go stale between sprints — treat `WORK_BOARD.md` as the live source if the two disagree. |
| `ROADMAP.md` | Completed/current/remaining phases with entry and exit criteria for each. |
| `NEXT_ACTION.md` | One-page operational handoff: what to do next, right now. |
| `REPOSITORY_AUDIT.md` | Point-in-time integrity audit (this sprint) — orphan files, broken links, inconsistent IDs/statuses, naming violations, with severity and recommended fixes. Not automatically kept current; check its `updated` date. |
| `PATTERN_VALIDATION_FRAMEWORK.md` | Defines the Pattern lifecycle, the cross-cycle validation matrix, minimum promotion requirements, evidence hierarchy, and the formal Pattern review process. |
| `ENVIRONMENT_NETWORK_REQUIREMENTS.md` | Which external domains the execution environment must allow for source verification, and known access gotchas. Operational/infrastructure, not research. |
| `HIS-001_RESEARCH_BRIEF.md` | The original brief for `HIS-001` (hypotheses H1–H5, evidence standards, originally-planned deliverables). Historical research content that lives in `governance/` for provenance reasons — see Repository Audit for the resulting cross-directory inconsistency. |
| `HIS-001_GATE_1_REVIEW.md` | The closed Gate 1 Research Design Review verdict for `HIS-001`. |
| `HIS-002_RESEARCH_BRIEF.md` | The research design brief for `HIS-002` (Electricity, Grid Infrastructure, and Industrial Electrification) — a cross-cycle validation case for `PAT-001`–`PAT-003`. Research design only; awaiting Gate 1. |

### `knowledge/industrial-revolutions/`

The working evidence trail and synthesis for each historical revolution under study. Currently contains only `HIS-001` material.

| File | One-line description |
|---|---|
| `HIS-001_RESEARCH_EXECUTION_PLAN.md` | The Gate-1-approved execution plan: question tree, evidence needs, source strategy, stopping conditions. |
| `HIS-001_SOURCE_REGISTER.md` | Every source consulted, with access status (`verified-open` / `verified-partial` / `verified-paywalled` / `access-failed` / `not-yet-checked`) and coverage notes. |
| `HIS-001_EVIDENCE_LEDGER.md` | The 151-claim evidence ledger (`C-001`–`C-316`), each claim tied to an exact source location, classified, and rated. |
| `REV-HIST-001_STEAM_AND_RAILWAYS.md` | The stable historical synthesis answering `HIS-001`'s research question, with H1–H5 hypothesis verdicts and candidate reusable mechanisms. |

### `patterns/`

Candidate reusable mechanisms distilled from historical syntheses. All currently `status: draft`, `confidence: low` — none may reach `active` on single-cycle evidence (see `PATTERN_VALIDATION_FRAMEWORK.md`).

| File | One-line description |
|---|---|
| `PAT-001_SOCIAL_VALUE_INVESTOR_RETURN_DIVERGENCE.md` | Infrastructure can create durable social value while direct investors see weak, uneven, or negative returns. |
| `PAT-002_CAPITAL_CYCLE_OVERBUILD.md` | Abundant speculative capital can accelerate buildout beyond near-term demand, impairing investors while leaving productive capacity behind. |
| `PAT-003_ENTRY_TIMING_AND_FINANCING_STRUCTURE.md` | Entry timing, leverage, and installment-call structure can dominate investor outcome within the same sector. |
| `PATTERN_VALIDATION_MATRIX.md` | The single canonical cross-Pattern tracking table (Pattern × Revolution → Supports/Weakens/Rejects/Undecidable). A tracking asset, not evidence; does not itself promote any Pattern. |

### `research/ai-revolution/`

The (currently orientation-only) AI-era baseline that future Mappings will eventually connect to.

| File | One-line description |
|---|---|
| `AI_REVOLUTION_BASELINE.md` | Unverified orientation notes on the present AI infrastructure cycle. No AI-era-analogy content is permitted here or anywhere until the Mapping stage is authorized. |

### `templates/`

Canonical starting structure for each asset type. Copy, do not reference directly as a live asset.

`EVIDENCE_LEDGER_TEMPLATE.md`, `HISTORICAL_RESEARCH_TEMPLATE.md`, `MAPPING_TEMPLATE.md`, `PATTERN_TEMPLATE.md`, `PREDICTION_TEMPLATE.md`, `SOURCE_REGISTER_TEMPLATE.md`, `THESIS_TEMPLATE.md`.

### `workflows/`

Step-by-step process definitions for recurring activities.

| File | One-line description |
|---|---|
| `RESEARCH_WORKFLOW.md` | The end-to-end Gate 1 → Stage A/B/C → Gate 2 → Synthesis → Gate 3 → Pattern pipeline, as actually run for `HIS-001`. |
| `GIT_WORKFLOW.md` | Branching, commit, and push conventions. |
| `MONTHLY_REVIEW_WORKFLOW.md` | Process for the recurring `MR-YYYY-MM` monthly review (not yet run — zero completed monthly reviews). |
| `THESIS_WORKFLOW.md` | Process for building an investment thesis once Phase 3 opens. `status: draft`; not usable until Phase 3 entry gates are satisfied (fixed Sprint 0.1 — was `status: locked`, a non-standard value). |

### Root

| File | One-line description |
|---|---|
| `README.md` | Public-facing entry point: North Star, repository role, current scope, start-here list. Contains a stale status line — see Repository Audit. |
| `CHANGELOG.md` | Append-only, reverse-chronological log, one entry per completed stage/sprint. |

## Reading Order for a New Agent

1. `governance/PROJECT_CONSTITUTION.md` — why this repository exists and its precedence rules.
2. `governance/PROJECT_STATE.md` — where things stand right now.
3. `governance/RESEARCH_SCOPE.md` — the phase model and what is and isn't in scope today.
4. `governance/AGENTS.md` — who does what.
5. `governance/WORK_BOARD.md` — the live task tracker.
6. `governance/NEXT_ACTION.md` — the immediate next step.
7. `governance/NAMING_AND_IDS.md` and `governance/FRONTMATTER_STANDARD.md` — conventions, before touching any file.
8. Only then: the specific research asset(s) relevant to the task at hand (`knowledge/`, `patterns/`, `research/`).
9. Before making any change: `governance/DECISIONS.md` (has this already been decided?) and `governance/REPOSITORY_AUDIT.md` (is this file already a known issue?).
