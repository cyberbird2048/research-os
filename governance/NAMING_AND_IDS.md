---
type: governance
title: Naming and ID Standard
status: active
created: 2026-07-12
updated: 2026-07-12
---

# Naming and ID Standard

## ID Scheme

| Prefix | Meaning | Example |
|---|---|---|
| `HIS-###` | Historical research task / sprint | `HIS-001` |
| `REV-HIST-###` | Historical revolution research asset | `REV-HIST-001` |
| `PAT-###` | Pattern (recurring, mechanism-based finding) | `PAT-001` |
| `MAP-###` | Historical-to-AI mapping | `MAP-001` |
| `THS-###` | Investment thesis | `THS-001` |
| `PRD-###` | Prediction journal entry | `PRD-001` |
| `DEC-###` | Decision log entry | `DEC-001` |
| `MR-YYYY-MM` | Monthly review | `MR-2026-07` |

IDs are assigned sequentially within their prefix and are never reused, even if an asset is later archived or rejected. Numbers are zero-padded to 3 digits (`001`, not `1`), except `MR-YYYY-MM`, which uses the calendar year and month.

## File Naming

- Canonical governance documents use `UPPER_SNAKE_CASE.md` (e.g. `PROJECT_CONSTITUTION.md`).
- Research and asset files are prefixed with their ID, followed by an underscore and an `UPPER_SNAKE_CASE` descriptive title:
  - `HIS-001_RESEARCH_BRIEF.md`
  - `HIS-001_RESEARCH_EXECUTION_PLAN.md`
  - `REV-HIST-001_STEAM_AND_RAILWAYS.md`
  - `HIS-001_EVIDENCE_LEDGER.md`
  - `HIS-001_SOURCE_REGISTER.md`
  - `PAT-001_INFRASTRUCTURE_BOTTLENECK_CAPTURE.md`
  - `MAP-001_RAILWAY_MANIA_AND_AI_INFRASTRUCTURE.md`
- Descriptive titles are short, literal, and content-derived — not marketing phrases.

## Branch Naming

Research branches follow:

```text
research/<ID>-<short-slug>
```

Example: `research/HIS-001-steam-railways`

Slugs are lowercase, hyphen-separated, and derived from the task title. One branch per active research task unless the task's own plan specifies otherwise.

## Status Lifecycle

Every asset with an ID carries a `status` field with exactly one of these values, in this order of maturity:

1. **draft** — in progress, not yet reviewed, may change substantially
2. **active** — in current use / current research focus, still subject to revision
3. **stable** — reviewed, evidenced, and not expected to change without new evidence
4. **archived** — superseded, rejected, or no longer maintained; retained for history

Status changes are one-directional in normal operation (draft → active → stable), except that any status may move to `archived`. Moving an asset backward (e.g. stable → draft) requires a recorded reason, typically a new decision log entry.

## Consistency Rule

An ID, once assigned in `governance/DECISIONS.md`, `governance/WORK_BOARD.md`, or a research asset's own frontmatter, must be identical across all three. Agents must not invent alternate spellings, casings, or numbering for an existing ID.
