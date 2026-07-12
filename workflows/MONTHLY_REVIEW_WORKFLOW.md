---
type: workflow
title: Monthly Review Workflow
status: active
created: 2026-07-12
updated: 2026-07-12
---

# Monthly Review Workflow

The monthly review is a manual discipline, not an automated report. It is produced by the User (Investment Committee) with support from Claude Code and ChatGPT, at minimum once per calendar month.

## Naming

`MR-YYYY-MM` (e.g. `MR-2026-07`), per `governance/NAMING_AND_IDS.md`.

## Required Sections

1. **This month's events.** What happened in the AI-era infrastructure/application landscape that is relevant to active research assets.
2. **Historical mappings touched.** Which `MAP-###` assets this month's events bear on, and how.
3. **Validated views.** Which prior predictions or thesis claims were supported by this month's evidence.
4. **Falsified views.** Which prior predictions or thesis claims were contradicted, and why.
5. **Thesis status changes.** Any thesis moved between `draft`, `active`, `stable`, or `archived`, with justification.
6. **Next month's watch list.** Specific, falsifiable items to monitor next month.

## Rules

- The review is manual. No scheduled job or agent may generate or publish it without human review.
- A review that finds nothing to validate or falsify must say so explicitly; it must not be skipped or padded with restated background.
- The first completed Monthly Review counts toward the Phase 3 entry gates in `governance/RESEARCH_SCOPE.md`.
- Reviews are cumulative evidence; they do not substitute for the evidence ledger of any individual research asset.

## Process

1. Claude Code drafts sections 1–2 from tracked sources and open research assets.
2. ChatGPT reviews sections 3–5 against the prediction journal and thesis status.
3. User confirms thesis status changes and the watch list before the file is marked `active`.
4. Update `governance/WORK_BOARD.md` and `CHANGELOG.md` to record the review.
