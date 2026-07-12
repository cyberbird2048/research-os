---
type: governance
title: Frontmatter Standard
status: active
created: 2026-07-12
updated: 2026-07-12
---

# Frontmatter Standard

All Markdown files in this repository carry YAML frontmatter. The canonical schema is defined by `governance/HIS-001_RESEARCH_BRIEF.md` and reproduced below.

## Canonical Schema

```yaml
---
id: HIS-001
type: research-brief
title: Steam, Railways, and Wealth Creation in the First Industrial Revolution
status: active
created: 2026-07-12
updated: 2026-07-12
owner: cyberbird
research_lead: claude-code
research_architect: chatgpt
review_date: 2026-08-01
confidence: low
sources: []
related:
  - REV-HIST-001
  - PAT-001
---
```

## Field Definitions

| Field | Required | Description |
|---|---|---|
| `id` | For assets with an ID | The asset's canonical ID (see `governance/NAMING_AND_IDS.md`) |
| `type` | Yes | One of the allowed types below |
| `title` | Yes | Human-readable title, matches the file's H1 |
| `status` | Yes | One of `draft`, `active`, `stable`, `archived` |
| `created` | Yes | Date the file was first created, `YYYY-MM-DD` |
| `updated` | Yes | Date of the most recent substantive edit, `YYYY-MM-DD` |
| `owner` | For research assets | The accountable person (currently `cyberbird`) |
| `research_lead` | For research assets | Agent executing the research (currently `claude-code`) |
| `research_architect` | For research assets | Agent responsible for design and review (currently `chatgpt`) |
| `review_date` | For research assets | Date the next review is due |
| `confidence` | For research assets | One of `low`, `medium`, `high` |
| `sources` | For research assets | List of source identifiers or citations; may be empty pending the source register |
| `related` | Recommended | List of related IDs (`REV-HIST-###`, `PAT-###`, `MAP-###`, `THS-###`, etc.) |

## Allowed `type` Values

- `research-brief`
- `execution-plan`
- `historical-research`
- `evidence-ledger`
- `source-register`
- `pattern`
- `mapping`
- `thesis`
- `prediction`
- `decision`
- `review`
- `governance`
- `workflow`
- `template`
- `baseline`

Agents must not introduce a new `type` value without recording the addition as a decision in `governance/DECISIONS.md`.

## Minimal Subset for Non-Research Files

Governance, workflow, and template files (`type: governance`, `type: workflow`, `type: template`) may omit research-specific fields. Their minimal required set is:

- `id` (optional — most governance files have no ID)
- `type`
- `title`
- `status`
- `created`
- `updated`

Example:

```yaml
---
type: governance
title: Naming and ID Standard
status: active
created: 2026-07-12
updated: 2026-07-12
---
```

## Rules

- Frontmatter is always the first content in the file, delimited by `---` lines.
- `status` in frontmatter must match the asset's actual lifecycle stage per `governance/NAMING_AND_IDS.md`; it is not aspirational.
- `updated` must change whenever the file's substance changes; cosmetic-only edits (typo fixes) do not require it.
- `sources` and `related` use YAML list syntax, even for a single item, for parser consistency.
