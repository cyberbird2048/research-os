---
id: HIS-001-PLAN
type: execution-plan
title: HIS-001 Research Execution Plan — Steam, Railways, and Wealth Creation
status: draft
created: 2026-07-12
updated: 2026-07-14
owner: cyberbird
research_lead: claude-code
research_architect: chatgpt
review_date: 2026-08-01
confidence: low
sources: []
related:
  - HIS-001
  - REV-HIST-001
  - PAT-001
  - PAT-002
  - PAT-003
---

# HIS-001 Research Execution Plan

**Purpose.** This document is the first deliverable of HIS-001. It is a plan, not a research result. No historical conclusion in this document is asserted as established; all named sources are *proposed* inputs, not yet vetted evidence. Work stops after this plan until it passes Gate 1 (Research Design Review).

**Primary research question (from the brief, unchanged):**

> During the steam and railway eras, which actors captured durable economic value, which investors earned attractive returns, and under what conditions did infrastructure buildout lead to overinvestment, margin compression, or financial loss?

---

## 1. Research Question Tree

The tree reorganizes the brief's 25 sub-questions into 6 branches. Branch order is also execution order: later branches depend on earlier ones. AI-relevance questions (QT6) are deliberately last and may not be answered before Gates 2–3 pass.

```text
PQ  Who captured durable value, who earned attractive returns,
    and when did buildout destroy capital?
│
├── QT1  Technology & Cost Curves                     [brief Q1–Q4]
│   ├── QT1.1  Which technical changes made steam commercially useful
│   │          (Newcomen → Watt → high-pressure → locomotive)?
│   ├── QT1.2  Which unit costs fell, by how much, over what period
│   │          (coal transport cost/ton-mile, freight rates, passenger fares,
│   │          engine efficiency in coal/hp-hour)?
│   ├── QT1.3  Which complementary assets were prerequisites for scaling
│   │          (iron rails, coal supply, civil engineering, land assembly,
│   │          legal form: joint-stock authorization)?
│   └── QT1.4  Which bottlenecks persisted despite technical progress
│              (and who owned them)?
│
├── QT2  Capital Formation & Financing Structures      [brief Q5–Q8]
│   ├── QT2.1  How were canals and railways financed
│   │          (share calls, scrip, loans, preference shares, bonds)?
│   ├── QT2.2  What roles did banks, exchanges, promoters, engineers,
│   │          and Parliament/state policy play?
│   ├── QT2.3  How did speculative capital change buildout speed and route choice?
│   └── QT2.4  Which financing structures created fragility
│              (uncalled capital, leverage, guaranteed dividends paid from capital)?
│
├── QT3  Value Capture Across the Chain                [brief Q9–Q13]
│   ├── QT3.1  Which firm categories earned durable operating profits
│   │          (coal, iron, locomotive builders, operators, contractors)?
│   ├── QT3.2  Which categories produced strong shareholder returns —
│   │          and are QT3.1 and QT3.2 answers different?
│   ├── QT3.3  Did equipment suppliers outperform infrastructure operators?
│   ├── QT3.4  Did landowners and downstream users capture more value
│   │          than railway shareholders?
│   └── QT3.5  How did competition (parallel routes, rate wars, cartels/pools)
│              affect pricing power over time?
│
├── QT4  Bubble & Bust Mechanics                       [brief Q14–Q18]
│   ├── QT4.1  What caused Railway Mania (1844–1847)? Which explanations
│   │          compete (irrational mania vs. rational-bubble accounts)?
│   ├── QT4.2  Which observable indicators signaled excess
│   │          (authorizations vs. GDP, share premiums on scrip, deposit rates,
│   │          calls outstanding, dividend yields vs. consols)?
│   ├── QT4.3  How much investor capital was impaired, for whom
│   │          (by shareholder class, line vintage, region)?
│   ├── QT4.4  Which firms survived and why
│   │          (traffic density, route quality, balance sheet, amalgamation)?
│   └── QT4.5  What productive infrastructure remained after the crash,
│              and who exploited it?
│
├── QT5  Long-Term Economic Effects                    [brief Q19–Q21]
│   ├── QT5.1  How did railways change market size, logistics cost,
│   │          urbanization, and industry structure?
│   ├── QT5.2  Which downstream industries benefited most?
│   └── QT5.3  When did the largest productivity effects appear
│              relative to the investment boom (lag structure)?
│
└── QT6  AI Relevance — mapping candidates only        [brief Q22–Q25]
    ├── QT6.1  Which mechanisms structurally resemble AI data-center /
    │          semiconductor / networking / power investment?
    ├── QT6.2  Which differences make the analogy weak or dangerous
    │          (asset life, depreciation, fungibility, standards velocity)?
    ├── QT6.3  Which metrics would distinguish productive buildout
    │          from destructive overcapacity, then and now?
    └── QT6.4  Which layers may capture value after infrastructure
               costs decline?
```

Cross-cutting requirement applied to QT2–QT4: every answer must separate **promoters / companies / shareholders (by class) / bondholders / suppliers / workers / landowners / downstream businesses** (brief Challenge A), and must distinguish **technological importance / social value / operating profit / bondholder return / shareholder return / long-term excess return**.

---

## 2. Evidence Required per Branch

| Branch | Required evidence | Minimum sufficiency to pass Gate 2 |
|---|---|---|
| QT1 Technology & cost | Engine efficiency series; freight/passenger rate series; construction cost per mile; coal price series | ≥2 independent quantitative series on cost decline; at least one primary or near-primary |
| QT2 Capital formation | Authorized vs. paid-up capital; call schedules; share of national investment; role of provincial exchanges; parliamentary authorization data | Quantified capital-formation picture for 1830s–1850s Britain; at least one financing-fragility mechanism documented from primary/near-primary records |
| QT3 Value capture | Dividend records by company category; operating ratios; locomotive-builder and iron-producer profitability; land value evidence | Operating profit and shareholder return documented **separately** for at least: operators, one supplier category, and one non-railway beneficiary category |
| QT4 Bubble & bust | Railway share price indices 1843–1850; scrip premium data; capital impairment estimates; bankruptcy/abandonment records; post-1847 dividend collapse data | A quantified estimate (or bounded range) of investor loss with an explicit method; ≥2 competing scholarly interpretations of the Mania recorded |
| QT5 Long-term effects | Social savings estimates and their critiques; freight cost vs. GDP; urbanization/market-integration studies | The social-savings debate documented with at least two opposing positions and their assumptions |
| QT6 AI relevance | No new evidence collected in HIS-001; uses outputs of QT1–QT5 plus already-held AI-cycle facts flagged as orientation | All entries classified as `ai-era analogy`; each mapping candidate has stated critical differences |

Every ledger row must carry a claim classification: `historical fact` / `quantitative estimate` / `scholarly interpretation` / `research inference` / `ai-era analogy`.

---

## 3. Proposed Primary-Source Categories

Categories, not yet a vetted list. Access approach is governed by Gate 1 decision U5 (open-access-first; see §12).

1. **UK parliamentary and regulatory records** — Railway Returns to the Board of Trade; select committee reports on railway acts; authorization statistics (miles authorized vs. built).
2. **Contemporary security price records** — *Course of the Exchange*; contemporary newspaper share tables (including provincial exchanges: Manchester, Liverpool, Glasgow); railway share indices reconstructed by modern scholars from these tables (near-primary).
3. **Company records** — published railway company accounts, dividend declarations, reports of shareholder meetings; known caveat: pre-1868 railway accounting was weakly standardized and sometimes manipulated (itself evidence for QT2.4).
4. **Contemporary press and reference works** — *The Economist* (from 1843), *Railway Times*, Bradshaw's railway manuals/shareholders' guides; used as evidence of contemporaneous perception and as data carriers, not as interpretation.
5. **Failure records** — bankruptcy court records digests, lines abandoned or never built after authorization, receivership data; for the US: railroad receivership statistics after the panics of 1857/1873/1893 (e.g., Poor's Manual of Railroads as near-primary).
6. **US quantitative compendia** — Poor's Manual, ICPSR historical railroad datasets, Historical Statistics of the United States (near-primary compilations).

## 4. Proposed Academic / Institutional Source Categories

1. **Railway Mania financial economics** — modern quantitative work on Mania share prices, investor returns, and the rational-bubble debate (e.g., Campbell & Turner; Odlyzko). These directly serve QT4 and are the most investment-relevant literature.
2. **Long-run UK asset returns** — reconstructed 19th-century UK equity/bond return series (e.g., Acheson–Campbell–Turner–Ye; Grossman) to benchmark railway returns against the market and consols. Serves the excess-return separation in §10.
3. **Social savings / counterfactual literature** — Fogel (US), Fishlow (US), Hawke (UK), Leunig (UK) and critiques; this is the canonical "social value vs. investor value" battleground and supplies the required competing interpretations. Serves QT5, H2.
4. **Steam power and GPT diffusion economics** — Crafts; von Tunzelmann on steam power diffusion and its productivity timing. Serves QT1, QT5.3.
5. **Business/financial history of railway companies** — company histories, amalgamation studies, railway accounting history (Arnold & McCartney on returns and accounting manipulation). Serves QT3, QT4.4.
6. **Official statistics compendia** — Mitchell, *British Historical Statistics*; Bank of England "A Millennium of Macroeconomic Data". Serves all quantitative branches.
7. **Synthesis (orientation only)** — Perez, *Technological Revolutions and Financial Capital*; Chandler on US railroads. Explicitly barred from being load-bearing evidence per OPERATING_PRINCIPLES; may suggest hypotheses and framing.

Brief minimums this plan must hit: ≥3 primary/near-primary quantitative sources (§3 items 1, 2, 5/6), ≥5 academic/institutional sources (§4 items 1–6), ≥2 competing interpretations (Mania: rational vs. irrational; social savings: Fogel vs. Fishlow/Hawke).

## 5. Search & Evidence Acquisition Strategy

Staged; each stage ends by updating the source register before any ledger rows cite it.

- **Stage A — Orientation (bounded, ≤1 session).** Map the literature landscape using surveys and bibliographies (EH.net encyclopedia entries, handbook chapters). Output: candidate source list in `HIS-001_SOURCE_REGISTER.md` with reliability ratings. No claims yet.
- **Stage B — Academic acquisition (open-access-first).** Locate open-access versions (author pages, SSRN/NBER/university repositories, scholars' published datasets, Mitchell's compendia) of the §4 core papers before considering any paid source. Record access path per source. Where only abstracts are accessible, mark the source `partial-access` and treat derived numbers as lower-confidence until verified. **Paid-access request trigger (Gate 1 decision U5):** escalate a specific, named paid-access request to the User only when (a) the source is load-bearing for a Gate 2 minimum-sufficiency requirement in §2, and (b) no open-access equivalent or substitute dataset exists after this stage's search. Do not silently substitute a lower-quality source for an inaccessible load-bearing one — log the gap instead.
- **Stage C — Quantitative backbone.** Extract the key series (share indices, dividends, authorized capital, cost series) into ledger rows with exact citations (table/page). Prefer series already digitized by scholars over hand-collected numbers; record the scholar's own source chain.
- **Stage D — Counter-evidence sweep.** Deliberate search pass for failures, dilution, weak regions, and anti-narrative findings (search terms oriented to "losses", "abandoned", "receivership", "calls", "unprofitable"). This stage is mandatory and has its own ledger section; it may not be skipped for time.
- **Stage E — Dispute documentation.** For each of the two required competing-interpretation pairs, write a neutral statement of both positions, their data, and what would decide between them.

Tooling: web search + fetch from this environment; everything cited must record URL/DOI and access date in the source register. If a load-bearing source proves inaccessible, that becomes an explicit gap in the Gap Review rather than a silently weaker claim.

## 6. Planned Repository Files

Per the brief §9; no files outside this list without a scope change approved at review.

| File | Created at | Gate |
|---|---|---|
| `knowledge/industrial-revolutions/HIS-001_RESEARCH_EXECUTION_PLAN.md` | now (this file) | Gate 1 |
| `knowledge/industrial-revolutions/HIS-001_SOURCE_REGISTER.md` | Stage A | Gate 2 |
| `knowledge/industrial-revolutions/HIS-001_EVIDENCE_LEDGER.md` | Stage C | Gate 2 |
| `knowledge/industrial-revolutions/REV-HIST-001_STEAM_AND_RAILWAYS.md` | after Gate 2 | Gate 3 |
| `patterns/PAT-001_INFRASTRUCTURE_BOTTLENECK_CAPTURE.md` | only if evidence supports | Gate 3→4 |
| `patterns/PAT-002_SOCIAL_VALUE_VS_INVESTOR_RETURN.md` | only if evidence supports | Gate 3→4 |
| `patterns/PAT-003_CAPITAL_CYCLE_OVERBUILD.md` | only if evidence supports | Gate 3→4 |
| `patterns/PAT-004_PROFIT_POOL_MIGRATION.md` | only if evidence supports | Gate 3→4 |
| `research/ai-revolution/MAP-001_RAILWAY_MANIA_AND_AI_INFRASTRUCTURE.md` | after Gate 3 | Gate 4 |
| `THS-001` | **not in HIS-001** | Gate 5, Phase 3 |

Patterns are capped at `draft` status within HIS-001 (Gate 1 decision U8; see §12). A hypothesis found unsupported is recorded as a `rejected` verdict row in the evidence ledger's hypothesis-verdict section (§7.4); this does not, by default, create a new pattern file. A pattern file is created only for a candidate mechanism judged recurring and evidence-backed enough to document, per Step 6 of `workflows/RESEARCH_WORKFLOW.md`.

> **Outcome annotation (added Sprint 0.1, 2026-07-14 — the table above is left as originally planned, not rewritten).** The four planned Pattern rows above were superseded by evidence-driven Pattern drafting. The Patterns actually created are `patterns/PAT-001_SOCIAL_VALUE_INVESTOR_RETURN_DIVERGENCE.md`, `patterns/PAT-002_CAPITAL_CYCLE_OVERBUILD.md`, and `patterns/PAT-003_ENTRY_TIMING_AND_FINANCING_STRUCTURE.md`. **Infrastructure Bottleneck Capture** was not promoted — insufficient supplier-side evidence (coal, iron, landowners). **Profit Pool Migration** remained undecidable and was not promoted. **Social Value vs. Investor Return** and **Capital Cycle Overbuild** were both drafted, under `PAT-001`/`PAT-002` respectively rather than `PAT-002`/`PAT-003`. **Entry Timing and Financing Structure**, not in this original table, emerged as `PAT-003` from the Evidence Ledger's cohort/leverage claims and the Historical Synthesis. `MAP-001` was authorized once, then withdrawn (`DEC-009`) before any file was created — no Mapping file exists. `THS-001` remains out of scope, as originally planned.

## 7. Claim-to-Evidence Workflow

1. Every major claim gets a ledger row with ID `C-###` **before** it may appear in any narrative file.
2. Ledger row = claim, evidence, exact source (register key + location), claim type, confidence (low/medium/high), counter-evidence (searched-and-found or searched-and-none, never blank-by-omission), notes.
3. Narrative text in `REV-HIST-001` cites claims as `[C-014]`. A narrative sentence with no ledger backing must be phrased as an open question or removed.
4. Hypotheses H1–H5 each get a verdict row at the end: supported / partially supported / rejected / undecidable-with-available-evidence, citing the ledger rows that decide it.
5. Confidence downgrades propagate: if a source is later found unreliable, all dependent claims are downgraded in the same commit.
6. Every substantive change updates `governance/WORK_BOARD.md` and `CHANGELOG.md`.

## 8. Major Risks and Likely Biases

1. **Hindsight/narrative bias** — the "railways obviously mattered" story pre-frames value capture. Control: hypotheses stated with rejection criteria before evidence collection (this plan).
2. **Confirmation bias toward the AI analogy** — the project *wants* railways to explain AI. Control: QT6 sequenced last; Challenge B (analogy breakers) has dedicated ledger space; Gate 4 requires falsifiable mapping.
3. **Survivorship bias** — see §9.
4. **Digitization bias** — successful, large, London-listed companies are better digitized; weak provincial lines underrepresented. Control: explicitly seek provincial-exchange and abandoned-line evidence; note coverage limits in Gap Review.
5. **Accounting anachronism** — applying modern profit concepts to pre-1868 railway accounts that lacked depreciation standards and sometimes paid dividends out of capital. Control: treat reported dividends as a distinct measure from economic profit; document accounting-quality caveats per period.
6. **Aggregation bias** — sector-average returns hide dispersion between trunk lines and speculative branches; averages could "prove" either narrative. Control: report distributions/cohorts (by authorization vintage, region) where data allows, not only means.
7. **Nominal-vs-real confusion** — the mid-19th-century price level was not stable. Control: state deflator choice per series; prefer real or benchmark-relative returns (see §10).
8. **Secondary-source laundering** — a popular book's number cited via an academic paper acquires false authority. Control: source register records each number's original chain where determinable.

## 9. Survivorship-Bias Controls

1. **Cohort-based sampling**: where feasible, take *all* railway securities listed in a given year's share tables (e.g., 1845) as the cohort and follow them forward — including delisted, absorbed, and failed lines — rather than sampling companies known today.
2. **Authorized-but-never-built tracking**: compare parliamentary authorizations (miles, capital) against completed mileage; the gap is a direct measure of capital committed to projects that died.
3. **Failure quota**: the evidence ledger must contain a dedicated failure section covering at minimum: failed/abandoned companies, shareholders ruined by calls, post-Mania dividend collapses, overbuilt duplicate routes, and at least one weak-return region — before Gate 2 can pass.
4. **US panics as out-of-sample check**: UK Mania findings tested against **at most two** of the US receivership waves (1857/1873/1893) to ensure mechanisms aren't one-country artifacts. Scope is capped to financing-fragility and receivership-outcome evidence only — not a parallel full study of US value capture. (Gate 1 decision U3 — see §12.)
5. **Winner-independent sourcing**: source register flags every source that conditions on success (company centenary histories, hagiographies) and caps their evidential weight.

## 10. Separating Investor Returns from Social Value and Operating Profit

Each concept gets its own measurement, its own evidence, and its own ledger rows; conflation between them is treated as an error to be corrected in review.

| Concept | Measure | Evidence base |
|---|---|---|
| Technological importance | Diffusion and capability metrics (mileage, tonnage, speed, engine efficiency) | QT1 series |
| Social value creation | Social savings estimates and their critiques; consumer surplus from rate declines; market-integration effects | §4.3 literature, both sides |
| Enterprise operating profit | Operating ratio, net revenue, return on paid-up capital, by company category and period | Company accounts, Railway Returns |
| Bondholder return | Yields, default incidence, recovery in reorganizations | Price records, failure records |
| Shareholder return | Total return (price + dividends) on cohort basis; **at least one representative cohort computed as a full cash-flow-aware (money-weighted) return accounting for installment-call timing** (Gate 1 decision U2); other cohorts may use scholarly time-weighted returns with qualitative money-weighted caveats | Reconstructed share indices, dividend records |
| Long-term excess return | Shareholder return minus benchmark — **primary benchmark: reconstructed broad UK equity index; secondary: consols** (Gate 1 decision U1) — over matched windows; **benchmark-relative framing is primary, real/deflated framing secondary**, using the Bank of England "A Millennium of Macroeconomic Data" series as the primary deflator plus one sensitivity check against an alternative contemporary price index where available (Gate 1 decision U6) | §4.2 series |

Explicit rule: national productivity gains (H2's "social value" side) may never be cited as evidence of investor return, and vice versa. The final asset must be able to state, separately and with sources: *who created value, who captured profit, who earned returns, who lost money* — and where these were different people.

## 11. Stopping Conditions

Stopping conditions are staged to match the workflow sequence in `workflows/RESEARCH_WORKFLOW.md`. A later-stage condition (e.g. mapping quality) is never a precondition for an earlier stage to conclude (Gate 1 decision, Required Revision 11).

### 11.1 Evidence Collection Exit Criteria (enables Historical Draft — Gate 2)

1. QT1–QT5 branches each meet their Gate 2 sufficiency row in §2.
2. The two required competing-interpretation pairs are documented with a decision criterion.
3. Investor-return evidence covers: at least one boom cohort, at least one bust cohort, the cash-flow-aware cohort requirement (U2), and benchmark-relative framing (U1).
4. Failure quota (§9.3) is met.

### 11.2 Historical Draft Completion Criteria (Gate 3)

5. H1–H5 each have a verdict row (including "rejected" or "undecidable" as acceptable outcomes), citing the ledger rows that decide it.
6. Remaining gaps are listed and judged non-critical at Gap Review.

### 11.3 Full Sprint Completion Criteria (Gate 4, downstream of the historical draft)

7. At least two candidate patterns are supported **or rejected** on evidence (capped at `draft` status within HIS-001 — U8).
8. MAP-001's critical-differences section is non-empty and falsifiable.

Condition 8 governs only when the *full* HIS-001 program is considered complete. It must never be read as blocking evidence collection (§11.1) or the historical draft (§11.2), which conclude independently and earlier — MAP-001 is not created until after Gate 3 (`workflows/RESEARCH_WORKFLOW.md`, Step 7).

Anti-goals that also stop work (failure conditions from brief §13): work drifting into general history summary; conclusions resting mainly on popular synthesis; AI mapping crowding out historical analysis; new revolutions being introduced; untraceable claims. Any of these triggers a pause and a redesign request, not silent continuation.

## 12. Resolved Design Decisions (Gate 1)

Ruled by the Research Architect at Gate 1 (`governance/HIS-001_GATE_1_REVIEW.md`, verdict: PASS WITH CONDITIONS). These are binding decisions, not open questions; U1–U8 numbering is preserved for traceability to the original questions.

- **U1 — Excess-return benchmark (RESOLVED).** Primary benchmark for long-term excess return is a reconstructed broad UK equity index; consols are reported as a secondary, contemporary-realistic benchmark. Both appear in every excess-return calculation, with the broad index labeled primary.
- **U2 — Return metric under call-based financing (RESOLVED).** At least one representative cohort must have a full cash-flow-aware (money-weighted) return calculation accounting for installment-call timing. Other cohorts may use scholarly time-weighted returns with qualitative money-weighted caveats.
- **U3 — Depth of US treatment (RESOLVED).** UK remains the primary case. US treatment is capped to **at most two** of the three panic episodes (1857/1873/1893), scoped only to financing-fragility and receivership-outcome evidence — not a parallel full study.
- **U4 — Canals (RESOLVED).** One bounded ledger section on canal-mania returns only; no dedicated narrative chapter.
- **U5 — Source access constraints (RESOLVED).** Open-access-first is the sourcing rule (author pages, SSRN/NBER/repositories, scholars' published datasets, Mitchell's compendia). A paid-access request to the User is triggered only when (a) a source is load-bearing for a Gate 2 minimum-sufficiency requirement in §2, and (b) no open-access equivalent or substitute dataset is found after the Stage B search (§5). Requests must name the specific source and the specific requirement it would satisfy.
- **U6 — Real vs. nominal (RESOLVED).** Benchmark-relative returns are the primary framing. Real (deflated) returns are secondary, using the Bank of England "A Millennium of Macroeconomic Data" series as the primary deflator, with one sensitivity check against an alternative contemporary price index (e.g., Feinstein or Clark cost-of-living series) where available.
- **U7 — Guaranteed-return structures (RESOLVED).** Excluded from HIS-001 entirely, including as a bounded ledger item. Colonial state-guaranteed railway cases (e.g., India) may be considered for a future sprint but are out of scope here.
- **U8 — Pattern promotion threshold (RESOLVED).** Confirmed: within HIS-001 alone, all candidate patterns are capped at `draft` status. Promotion to `active` requires cross-cycle validation from a second historical revolution (HIS-002/003), which has not started.

## 13. Research-Budget Guardrail

If a comparative or bounding module — the US panic-episode comparison (§9.4) or the canal ledger section (U4) — begins to consume research time disproportionate to the core UK steam/railway analysis, the comparative module is cut back or dropped first. The Sprint timeline is not extended to accommodate it. Any cut is logged in the evidence ledger's Notes column and reported at the next gate review rather than silently absorbed.

---

*Gate 1 status: Research Design Review completed — PASS WITH CONDITIONS (`governance/HIS-001_GATE_1_REVIEW.md`). The 12 required revisions are implemented in this revision of the plan. Next step: STOP. Await Research Architect confirmation that all 12 revisions are correctly implemented before Stage A (source-register orientation) begins.*
