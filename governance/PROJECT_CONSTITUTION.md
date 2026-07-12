---
type: governance
title: Project Constitution
status: active
created: 2026-07-12
updated: 2026-07-12
---

# Project Constitution

## North Star

There is exactly one north star. Every decision, module, and file must answer:

> Does this help discover, explain, test, or track AI-era investment alpha more reliably?

If a proposed action does not serve this question, it does not belong in this repository.

## Source of Truth

GitHub is the single source of truth for CyberBird Research OS.

- Obsidian is an optional read view only. It never holds content that does not also exist in GitHub.
- If governance documents and conversation history (including handoff material) conflict, the governance documents in `governance/` win. Conversation history explains intent; it does not override rules.

## The Seven Constitutional Principles

1. **Single north star.** The only test for any addition is whether it improves the discovery of AI-era alpha. There is no secondary goal.
2. **Repository stores assets, not information inventory.** This repository holds durable research assets — frameworks, patterns, mappings, theses, predictions, decisions, reviews. It does not store raw news, unprocessed PDFs, copied articles, or undigested notes.
3. **One phase answers one question.** Each phase has a single defined question. Work does not proceed to the next question until the current one is resolved or explicitly stopped.
4. **New modules must prove necessity.** No process, tool, folder, or role is added because it might be useful. It must be justified by a concrete, current need.
5. **Files have a lifecycle.** Every research asset moves through `draft → active → stable → archived`. Status is explicit in frontmatter and reflects actual maturity, not aspiration.
6. **No second system.** There is one repository, one canonical workflow, one set of IDs. Parallel or shadow structures (extra trackers, duplicate knowledge bases, ad hoc formats) are prohibited.
7. **Foundation before research before automation.** Governance and structure are established before historical research begins. Historical research is established and repeatable before any automation is introduced.

## Core Disciplines

> Save thinking, not information.

Do not archive source material for its own sake. Archive the reasoning, the claim, and its evidentiary basis.

> Depth over breadth.

One well-evidenced historical chain is worth more than many shallow surveys. Scope is deliberately narrow at every phase.

> Manual before automated.

Every workflow is run manually and proven repeatable before any automation is considered. Automation is a Phase 3+ concern, not a Phase 1 or Phase 2 concern.

## Precedence

When rules conflict, resolve in this order:

1. This constitution
2. `governance/RESEARCH_SCOPE.md` and `governance/OPERATING_PRINCIPLES.md`
3. Active research briefs (e.g. `governance/HIS-001_RESEARCH_BRIEF.md`)
4. Handoff / conversation history

No agent may reinterpret this order to expand scope or skip a review gate.
