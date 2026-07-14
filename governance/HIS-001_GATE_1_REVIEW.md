---
id: HIS-001-GATE-1
type: review
title: HIS-001 Gate 1 — Research Design Review
status: stable
created: 2026-07-12
updated: 2026-07-14
owner: cyberbird
research_lead: claude-code
research_architect: chatgpt
review_date: 2026-07-12
confidence: high
sources: []
related:
  - HIS-001
---

# HIS-001 Gate 1 — Research Design Review

**Reviewer:** ChatGPT (Research Architect)
**Subject:** `knowledge/industrial-revolutions/HIS-001_RESEARCH_EXECUTION_PLAN.md`
**Verdict: PASS WITH CONDITIONS**

The plan may proceed to Stage A (source-register orientation, per `workflows/RESEARCH_WORKFLOW.md`) only after the 12 Required Revisions in Section 4 are implemented in the execution plan and confirmed here.

## 1. Gate 1 Verdict

Assessed against the five Gate 1 pass criteria (`governance/HIS-001_RESEARCH_BRIEF.md` §11 / `workflows/RESEARCH_WORKFLOW.md`):

| Criterion | Assessment |
|---|---|
| One primary question | Met. The plan does not introduce a second primary question; QT6 (AI relevance) is subordinate and sequenced last. |
| Bounded scope | Met, with conditions. The comparative modules (US panic episodes, canals) were under-bounded in the submitted plan and risked expanding into parallel full studies. See Required Revisions 4, 5, 12. |
| Explicit evidence requirements | Met. Section 2's per-branch evidence table and Section 6's minimum sourcing counts are adequate. |
| Explicit counter-evidence | Met. Sections 8–9 (risks/biases, survivorship-bias controls) are sufficient for Gate 1. |
| No premature AI conclusion | Met. No AI-era claim is asserted as fact anywhere in the plan; QT6 is explicitly deferred. |

## 2. Rulings on U1–U8

- **U1 — Excess-return benchmark.** Use a reconstructed broad UK equity index as the **primary** benchmark for long-term excess return; consols as **secondary**. A broad index is the stricter alpha test and the one relevant to an AI-era mapping (which will compare against equity markets, not gilts).
- **U2 — Return metric under call-based financing.** Qualitative money-weighted caveating alone is insufficient. Require a full cash-flow-aware (money-weighted) return calculation for **at least one representative cohort**; other cohorts may use scholarly time-weighted returns with qualitative caveats. This bounds the rigor increase to a single worked example rather than a full cash-flow rebuild across all cohorts.
- **U3 — Depth of US treatment.** Confirmed: UK is the primary case. US treatment is capped to **at most two** of the three panic episodes (1857/1873/1893), and scoped only to financing-fragility and receivership-outcome evidence — not a second full value-capture study.
- **U4 — Canals.** Confirmed: one bounded ledger section on canal-mania returns; no dedicated narrative chapter.
- **U5 — Source access constraints.** Open-access-first is the rule. Paid-access requests to the User are permitted, but only when explicitly triggered: (a) the source is load-bearing for a Gate 2 minimum-sufficiency requirement, and (b) no open-access substitute exists after a genuine search. Untriggered "just in case" access requests are out of process.
- **U6 — Real vs. nominal.** Benchmark-relative returns primary; real returns secondary. One named primary deflator (Bank of England "A Millennium of Macroeconomic Data") plus one sensitivity check against an alternative period price index.
- **U7 — Guaranteed-return structures.** Excluded from HIS-001 entirely — including as a bounded ledger item. The India/colonial guaranteed-railway case is a genuinely interesting financing-structure comparison but is geographically out of the declared scope (`governance/RESEARCH_SCOPE.md`); it may be proposed for a future sprint on its own merits, not folded into HIS-001 by convenience.
- **U8 — Pattern promotion threshold.** Confirmed: `draft` is the maximum pattern status achievable within HIS-001 alone. `active` requires cross-cycle validation from a second historical revolution.

## 3. Scope-Creep Check

- The submitted plan's comparative modules (US panics, canals) were the primary scope-creep risk: as written, they had no explicit time/depth ceiling relative to the core UK steam-and-railway analysis, and "US treatment" could plausibly have grown into a second full study. Revisions 4, 5, and 12 close this gap.
- The primary research question, geography (Great Britain primary, US secondary), and time range are unchanged from the brief. No expansion found there.
- No new revolutions, industries, or geographies were introduced. No AI-era conclusion was found anywhere in the plan.
- One structural defect unrelated to scope expansion but relevant to discipline: the submitted Section 11 (Stopping Conditions) made the historical-evidence-collection stage depend on an artifact (MAP-001) that by the plan's own execution sequence does not exist until after Gate 3. This is a sequencing bug, not a scope issue, but it would have silently blocked or confused the evidence-collection exit decision. See Required Revision 11.

## 4. Required Revisions (12)

All 12 must be implemented in `HIS-001_RESEARCH_EXECUTION_PLAN.md` before Gate 1 is considered fully passed:

1. Convert U1–U8 from "unresolved research-design questions" into resolved design decisions, referencing this review.
2. Broad-based UK equity index as the primary equity-alpha benchmark; consols as a secondary benchmark.
3. Require a cash-flow-aware (money-weighted) return calculation for at least one representative cohort.
4. Cap US case treatment to at most two panic episodes, scoped only to financing fragility and receivership outcomes.
5. Canals: one bounded ledger section only, no dedicated narrative chapter.
6. Add an open-access-first sourcing rule, plus explicit trigger conditions for requesting paid access.
7. Benchmark-relative returns as primary; real returns as secondary; name one primary deflator and require a sensitivity check.
8. Explicitly exclude colonial state-guaranteed railway cases from HIS-001.
9. Cap all patterns created within HIS-001 at `draft` status maximum.
10. Remove the rule that a rejected hypothesis defaults to creating an archived pattern file.
11. Fix the stopping conditions: MAP-001 must not be a precondition for historical evidence collection to stop, since MAP-001 is only created after Gate 3.
12. Add a research-budget guardrail: when a comparative module threatens to crowd out the core UK research, cut the comparative module first — do not extend the Sprint.

## 5. Escalation Conditions

Claude Code must escalate to the User (Investment Committee) rather than deciding alone if any of the following occur during Stage A onward:

- A source that is load-bearing for a Gate 2 minimum-sufficiency requirement (§2 of the plan) has no open-access substitute (per U5's trigger) — escalate the specific paid-access request rather than substituting a weaker source.
- The research-budget guardrail (Required Revision 12) triggers more than once in the same stage, suggesting the comparative modules cannot be bounded as designed.
- Evidence directly contradicts the plan's question tree or hypotheses in a way that would require redesigning the question tree itself (as opposed to simply returning a "rejected" verdict on a hypothesis, which is an expected, in-process outcome).
- Either of the two required competing-interpretation pairs (Railway Mania: rational vs. irrational; social savings: Fogel vs. Fishlow/Hawke) cannot be documented from accessible sources.
- Any condition matching brief §13 Failure Conditions (drift into general history, reliance on popular synthesis, AI mapping crowding out historical analysis, new revolutions introduced, untraceable claims) — pause and request redesign rather than continuing.

## 6. Next Step

Claude Code implements the 12 Required Revisions in the execution plan, updates `governance/WORK_BOARD.md` and `CHANGELOG.md`, and submits a single commit with: commit SHA, list of changed files, the 12-item revision checklist, and the file/line location of each implemented revision. Work board status moves to "Gate 1 revisions implemented — awaiting Research Architect confirmation." No evidence collection, Source Register, Evidence Ledger, Pattern, Mapping, or Thesis file may be created in that change set, and the primary research question and geographic/historical scope may not change.

Gate 1 is fully PASSED only after the Research Architect confirms all 12 revisions are correctly implemented.
