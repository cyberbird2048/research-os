---
id: <TASK-ID>-EVIDENCE-LEDGER
type: evidence-ledger
title: <Task ID> Evidence Ledger
status: draft
created: 2026-07-12
updated: 2026-07-12
owner: cyberbird
research_lead: claude-code
research_architect: chatgpt
review_date: YYYY-MM-DD
confidence: low
sources: []
related: []
---

# <Task ID> Evidence Ledger

Built before narrative drafting begins (Step 4 of `workflows/RESEARCH_WORKFLOW.md`). Every claim used in the corresponding historical research asset must have a row here.

## Claim-Type Legend

- **historical fact** — directly documented, not in serious dispute
- **quantitative estimate** — a number with a stated methodology and margin of uncertainty
- **scholarly interpretation** — a reasoned conclusion by historians/economists, contested or not
- **research inference** — this project's own reasoning from the above, not directly sourced
- **AI-era analogy** — a comparison to the AI cycle; permitted only in mapping assets, never in historical assets

## Ledger

| Claim ID | Claim | Evidence | Source | Type | Confidence | Counter-Evidence | Notes |
|---|---|---|---|---|---|---|---|
| CLM-001 | Example: UK rail freight rates fell substantially between 1830 and 1850 | Contemporary rate schedules and freight volume series | [Author, Year, p.xx] | quantitative estimate | medium | Regional variation was large; some routes saw little change | Placeholder row — replace before Gate 2 |

## Rules

- One row per discrete claim. Do not bundle multiple claims into one row.
- `Counter-Evidence` is mandatory where it exists; write "none found" only if a search was actually performed.
- A claim with no source is not permitted to appear in the historical draft.
- `Confidence` uses the repository-wide scale: low / medium / high.
