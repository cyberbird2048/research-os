---
type: governance
title: Pattern Validation Framework
status: active
created: 2026-07-12
updated: 2026-07-12
---

# Pattern Validation Framework

This is a governance document, not a research asset. It defines the rules by which a candidate Pattern (`PAT-###`) may eventually be promoted from `draft` to `active`, and the conditions under which it must instead be weakened, bounded, or rejected. It defines **methodology only**. It contains no discussion of current AI companies, AI infrastructure, or investment opportunities, and none may be added to this file.

This framework exists because a mechanism observed in a single historical revolution is a hypothesis, not a validated pattern. Promoting it prematurely — before checking whether it recurs, under what conditions it fails, and whether a second revolution contradicts it — risks building a convincing narrative on a sample size of one. The framework is the gate between "one good historical case" and "a mechanism trusted enough to inform an AI-era mapping."

It governs every `PAT-###` file uniformly and supersedes any ad hoc promotion judgment made while drafting an individual Pattern.

---

## 1. What Qualifies as a Reusable Historical Pattern

A candidate is eligible to be recorded as a Pattern (at `draft`) only if it states:

1. **A mechanism**, not a narrative similarity. "Both eras had a boom and a bust" is not a mechanism. "Partial-payment financing creates leverage that amplifies both gains and losses, so cohort entry timing dominates realized return" is a mechanism — it names the causal linkage, not just the shape of the outcome.
2. **A scope** — the actors, instruments, and conditions under which the mechanism is claimed to operate (e.g., equity-financed infrastructure with installment-call financing, not "capital markets" in general).
3. **At least one falsification condition** — a specific, observable outcome that would count against the mechanism, stated at the time the Pattern is drafted, not invented after the fact.
4. **At least one boundary condition** — a precondition (market structure, financing structure, regulatory environment, or similar) required for the mechanism to apply, so the Pattern is not silently treated as universal.

A Pattern that only restates a historical finding ("railway returns were timing-dependent") without generalizing to a mechanism, scope, falsification condition, and boundary condition does not qualify for a `PAT-###` file at all — it stays inside the historical asset (`REV-HIST-###`) as a finding.

---

## 2. Pattern Lifecycle

```text
draft
  ↓
validated-in-one-cycle
  ↓
cross-cycle-candidate
  ↓
active
  ↓
stable
  ↓
archived
```

Movement is one-directional except that any state may move to `archived` (rejection), and a move backward (e.g. `active` → `cross-cycle-candidate`) requires a recorded reason in `governance/DECISIONS.md`, consistent with `governance/NAMING_AND_IDS.md`'s general status-lifecycle rule.

### `draft`

- **Meaning:** A candidate mechanism has been proposed from a single historical episode. It is a hypothesis, not a finding trusted for reuse.
- **Entry requirements:** Satisfies §1 (mechanism, scope, falsification condition, boundary condition); derived only from an existing `REV-HIST-###` and its `HIS-###-EVIDENCE-LEDGER`; every substantive statement cites `C-###` claim IDs; counter-evidence section present.
- **Exit requirements:** The single supporting historical episode's evidence is judged internally sufficient (see §4's per-episode bar) by the Research Architect.
- **Review authority:** Research Lead drafts; Research Architect confirms entry criteria are met.
- **Required evidence:** One historical episode (one `REV-HIST-###`), evidence-graded per §5.

### `validated-in-one-cycle`

- **Meaning:** The mechanism is well-evidenced within its originating revolution, but has not yet been tested against a second, independent revolution. This is the ceiling for any Pattern originating from a single `HIS-###` task — it must not be read as "confirmed," only as "the first cycle's evidence holds up under scrutiny."
- **Entry requirements:** A completed Counter-Evidence Review (§8) within the originating cycle; no unresolved load-bearing evidence gap for the mechanism's core claim (per §4); the falsification condition has been actively checked against the evidence, not merely stated.
- **Exit requirements:** A second, independent historical revolution has been studied (its own `HIS-###` → `REV-HIST-###` → Evidence Ledger chain complete) and the Pattern has been tested against it via the Validation Matrix (§3).
- **Review authority:** Research Architect.
- **Required evidence:** Still one episode; the Validation Matrix (§3) has exactly one populated row.

### `cross-cycle-candidate`

- **Meaning:** A second independent revolution has been checked against the mechanism and the result is `Supports` or, at worst, `Weakens` without `Rejects`. The Pattern is a serious candidate for promotion but has not yet cleared the full minimum bar in §4.
- **Entry requirements:** Validation Matrix has ≥2 populated rows, no row marked `Rejects` without a recorded resolution (see §6); counter-evidence reviewed for each row.
- **Exit requirements:** All minimum promotion requirements in §4 are met.
- **Review authority:** Research Architect, with escalation to the Investment Committee (User) for any judgment call on whether a `Weakens` entry is tolerable.
- **Required evidence:** ≥2 independent revolutions, at least one from a different institutional/regulatory environment where evidence permits (§4).

### `active`

- **Meaning:** The mechanism is trusted for reuse — specifically, it is eligible to be cited as an input to a future Historical → AI Mapping (`MAP-###`). `active` is not a claim that the mechanism is universal; it is a claim that it has cleared the minimum cross-cycle bar this framework sets.
- **Entry requirements:** All of §4's minimum promotion requirements satisfied simultaneously; formal Promotion Decision recorded (§8).
- **Exit requirements:** Sustained, unchallenged applicability across further review cycles (no fixed count; assessed at each Monthly Review, per `workflows/MONTHLY_REVIEW_WORKFLOW.md`).
- **Review authority:** Research Architect and Investment Committee jointly (see §8).
- **Required evidence:** ≥2 independent revolutions at `Supports`, full counter-evidence review, no unresolved load-bearing gap.

### `stable`

- **Meaning:** The mechanism has been repeatedly reused (e.g., across multiple Mappings or a Monthly Review cycle) without requiring revision, and is treated as durable project infrastructure.
- **Entry requirements:** No revision required across at least one full additional review cycle after reaching `active`.
- **Exit requirements:** New contradictory evidence surfaces (moves to `archived` or back to `cross-cycle-candidate` with a recorded reason).
- **Review authority:** Research Architect and Investment Committee jointly.
- **Required evidence:** Same evidentiary base as `active`, undisturbed over time.

### `archived`

- **Meaning:** Rejected, superseded, or no longer maintained. Retained for history — never deleted, never silently dropped.
- **Entry requirements:** A recorded reason in `governance/DECISIONS.md` — rejection by counter-evidence, contradiction by a later revolution (§6), or supersession by a better-specified Pattern.
- **Exit requirements:** None (terminal state) — an archived Pattern is never silently revived; a materially new version is a new `PAT-###`.
- **Review authority:** Research Architect.
- **Required evidence:** The evidence that caused the rejection/supersession, cited.

---

## 3. Validation Matrix

Every Pattern maintains a Validation Matrix as it accumulates cross-cycle evidence. This is the reusable template; **no future rows are populated by this framework document** — only actual `PAT-###` files populate rows, and only as the corresponding `HIS-###` research is actually completed.

| Historical Revolution | Supports | Weakens | Rejects | Notes |
|---|---|---|---|---|
| Steam & Railways | | | | |
| Electricity | | | | |
| Oil & Automobile | | | | |
| Semiconductor | | | | |
| Internet | | | | |
| Mobile | | | | |
| Cloud | | | | |
| AI | | | | |

Column definitions:

- **Supports** — the mechanism operated as stated, with cited evidence, in this revolution.
- **Weakens** — evidence is mixed, partial, or requires a narrower boundary condition than originally stated; the mechanism is not rejected but confidence and/or scope must be revised.
- **Rejects** — evidence directly contradicts the mechanism's core claim in a way that cannot be resolved by narrowing scope; see §6.
- **Notes** — the specific `C-###`/claim-equivalent evidence, and any scope narrowing applied.

A row is populated only from a completed `HIS-###` chain (Evidence Ledger → Historical Asset). It is never populated from narrative impression, from a revolution that has not yet been researched under this project, or in anticipation of AI-era evidence — the `AI` row exists in the template because Phase 3 will eventually require it, not because it may be filled in now. Populating the `AI` row is out of scope until Phase 3 gates open per `governance/RESEARCH_SCOPE.md`.

---

## 4. Minimum Promotion Requirements (Draft/Candidate → Active)

A Pattern may not be promoted to `active` unless **all** of the following are satisfied simultaneously:

1. **At least two independent technological revolutions** show the mechanism at `Supports` in the Validation Matrix (§3), with no unresolved `Rejects`.
2. **Evidence from different institutional environments where possible** — e.g., not two revolutions both drawn from the same single national capital market and regulatory regime, when comparative evidence is available. Where genuinely unavailable, this is recorded as a limitation, not silently waived.
3. **Explicit counter-evidence review completed** for each supporting revolution (§8's Counter-Evidence Review stage), not merely a counter-evidence section left over from the original draft.
4. **Boundary conditions defined and tested** — the conditions under which the mechanism is claimed to hold must have been checked against at least one case near or outside that boundary.
5. **Falsification conditions stated and actively checked** — not merely present in the file, but shown to have been examined against the accumulated evidence.
6. **No unresolved load-bearing evidence gap** — a gap is load-bearing if the Pattern's core claim would change materially depending on how the gap is resolved (per the same standard used in `HIS-001_EVIDENCE_LEDGER.md`'s Gate 2 readiness assessment). Precision-only gaps do not block promotion; load-bearing gaps do.
7. **A repeatable economic mechanism, not narrative similarity** — the promotion record must state the causal mechanism in terms general enough to apply across the supporting revolutions, and distinct from merely observing that "a similar-looking event happened again" (see §1 and §5).

Failing any single condition keeps the Pattern at `cross-cycle-candidate` or lower — partial satisfaction does not average out to promotion.

---

## 5. Evidence Hierarchy

Within a Pattern's supporting evidence, stronger evidence outweighs repetition of weaker evidence. Preferred order, highest first:

1. **Primary evidence** — original records, filings, contemporary statistics, and data as first published.
2. **Near-primary quantitative evidence** — scholarly reconstructions built directly from primary records (e.g., reconstructed price indices, compiled statistical series).
3. **Academic synthesis** — peer-reviewed or university-press economic history that interprets primary/near-primary evidence.
4. **Historical interpretation** — reputable non-academic secondary synthesis, used for framing and context.
5. **Narrative analogy** — an impressionistic similarity between episodes, with no direct evidentiary chain.

**Narrative analogy alone must never promote a Pattern.** A Pattern citing only level-5 evidence cannot leave `draft`, regardless of how many analogous episodes are cited, and ten narrative analogies do not equal one piece of primary or near-primary evidence. This mirrors the evidence priority order already established in `governance/OPERATING_PRINCIPLES.md` for individual claims, applied here at the Pattern level.

---

## 6. Handling Contradictory Revolutions

When a new revolution's evidence conflicts with a Pattern already at `validated-in-one-cycle` or higher:

1. **First, check whether the conflict is genuine or a boundary-condition mismatch.** If the contradicting case falls outside the Pattern's stated boundary conditions (§1), the correct response is to tighten the boundary conditions explicitly, not to reject the Pattern — the Validation Matrix row is marked `Weakens` with a note explaining the boundary narrowing, not `Rejects`.
2. **If the conflict is genuine** (the contradicting case is within the stated boundary conditions and still contradicts the core mechanism), the row is marked `Rejects` and the Pattern **may not hold or advance past `cross-cycle-candidate`** until either:
   - the mechanism statement is revised and the revision is re-tested against all prior supporting revolutions (a materially revised mechanism is treated as requiring re-validation, not grandfathered in on the old evidence), or
   - the Pattern is moved to `archived` with the contradiction recorded as the reason.
3. **A single `Rejects` entry is not automatically fatal if the mechanism is revised and the revision survives re-testing** — but silently narrowing the mechanism after every contradiction, without re-testing against earlier cases, is not permitted; each revision is tracked and re-validated, per the traceability rule in `governance/OPERATING_PRINCIPLES.md`.
4. **Contradictions are never omitted from the Validation Matrix.** A Pattern's file must show its full history of support and contradiction, not only the revolutions that supported it.

---

## 7. Pattern Quality Checklist

Every Pattern should eventually be able to answer all of the following, either directly in its own text or by explicit reference to its supporting `REV-HIST-###`/Evidence Ledger:

- What is the mechanism?
- Why does it work (what is the causal linkage, not just the correlation)?
- Under what conditions does it hold (boundary conditions)?
- When does it fail (failure modes, observed or anticipated)?
- What evidence supports it?
- What evidence weakens it?
- What evidence rejects it?
- What observable indicators would signal the mechanism is operating in a new case?
- What remains unknown?

A Pattern with unanswered items is not disqualified from `draft`, but each unanswered item is an explicit blocker to promotion past `validated-in-one-cycle`.

---

## 8. Pattern Review Process

```text
Draft Pattern
     ↓
Historical Validation
     ↓
Counter-Evidence Review
     ↓
Cross-Cycle Comparison
     ↓
Promotion Decision
```

- **Draft Pattern** — Research Lead drafts per §1, deriving only from an existing historical asset and its Evidence Ledger.
- **Historical Validation** — confirms the Pattern's claims are correctly traced to `C-###` claim IDs and correctly characterize the source evidence (no overstated confidence, no claim beyond what the ledger supports).
- **Counter-Evidence Review** — an explicit, adversarial pass: what is the strongest evidence against the mechanism, and has it been fairly represented? This stage is repeated for each new revolution added to the Validation Matrix, not performed once and reused.
- **Cross-Cycle Comparison** — the Validation Matrix (§3) is updated against the newly available revolution(s), applying §6 where conflicts arise.
- **Promotion Decision** — a formal decision to move the Pattern's status, recorded with the same discipline as any other decision in `governance/DECISIONS.md`.

**Promotion authority remains with the Research Architect and Investment Committee.** The Research Lead may recommend a promotion decision but may not execute one unilaterally; movement to `active` or `stable` requires their joint sign-off, consistent with the roles defined in `governance/AGENTS.md`.

---

## 9. Relationship to Existing Governance

This framework operationalizes, and does not replace, the Phase 3 entry gate in `governance/RESEARCH_SCOPE.md` requiring "at least 5 cross-cycle validated Patterns." A Pattern counts toward that gate only once it has reached `active` under this framework — `draft`, `validated-in-one-cycle`, and `cross-cycle-candidate` Patterns do not count. This framework also inherits, rather than restates in full, the evidence-classification and traceability rules of `governance/OPERATING_PRINCIPLES.md`; where the two documents overlap, `OPERATING_PRINCIPLES.md` governs individual claims and this framework governs Pattern-level promotion.

This document defines methodology only. No AI-era company, sector, technology, or investment conclusion is discussed here, and none should be added in a future edit without a corresponding scope decision in `governance/DECISIONS.md`.
