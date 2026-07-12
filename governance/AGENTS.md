---
type: governance
title: Agent Roles and Collaboration Rules
status: active
created: 2026-07-12
updated: 2026-07-12
---

# Agent Roles and Collaboration Rules

## Roles

### GitHub — Canonical Source

GitHub holds the single source of truth for all research assets, governance, and history. If it is not in GitHub, it does not count as done.

### Obsidian — Optional Read View

Obsidian may be used to browse the repository locally. It is a view, not a store. Nothing exists only in Obsidian.

### Claude Code — Research Lead & Repository Operator

Responsibilities:

- Executes research tasks assigned in `governance/WORK_BOARD.md`.
- Operates the repository directly: creates branches, files, and commits following `governance/NAMING_AND_IDS.md` and `governance/FRONTMATTER_STANDARD.md`.
- Produces research execution plans, evidence ledgers, source registers, and historical drafts.
- Does not produce a final historical report or thesis before the applicable review gate has passed (see `governance/HIS-001_RESEARCH_BRIEF.md` §11).
- Updates `governance/WORK_BOARD.md` and `governance/CHANGELOG.md`-equivalent records for every substantive change.

### ChatGPT — Research Architect / Gap Review / Investment Synthesis

Responsibilities:

- Designs research (question tree, hypotheses, evidence standards) before Claude Code executes.
- Performs Gap & Logic Review on Claude Code's output: checks for missing evidence, weak claims, unresolved debates, and unsupported analogies.
- Performs Investment Synthesis only after historical research and mapping are reviewed and stable.
- Does not execute repository operations directly.

### Codex — Evidence & Logic Reviewer

Responsibilities:

- Independently checks evidentiary support and logical consistency of claims, particularly claim classification (fact vs. estimate vs. interpretation vs. inference vs. analogy) and counter-evidence completeness.
- Does not design research scope and does not make final investment or promotion decisions.

### User (cyberbird) — Investment Committee / Final Decision

Responsibilities:

- Sets the north star and approves scope changes.
- Makes the final decision at each gate: whether to proceed, revise, or stop.
- Is the sole owner of all research assets (`owner` field in frontmatter).

## Collaboration Sequence

```text
User defines goal
  → ChatGPT: Research Design
  → Claude Code: Execution
  → ChatGPT: Gap & Logic Review
  → Claude Code: Revision
  → ChatGPT: Investment Synthesis
  → User: Final Decision
```

Research Design precedes execution. Claude Code does not begin full research before a design exists and does not skip ahead to synthesis or thesis creation.

## Rules for All Agents

1. **No scope expansion.** No agent may broaden scope, add a research task, or introduce a new module without a recorded decision in `governance/DECISIONS.md`. See `governance/RESEARCH_SCOPE.md`.
2. **No skipped review gates.** Work does not advance past a gate defined in an active research brief without that gate's pass criteria being met and recorded.
3. **Mandatory tracking updates.** Every substantive change (new file, status change, gate passed, decision made) must be reflected in `governance/WORK_BOARD.md` and the repository `CHANGELOG.md` in the same change set.
4. **No parallel authority.** Only the User makes final decisions. No agent may treat its own output as final without the User's sign-off at the relevant gate.
