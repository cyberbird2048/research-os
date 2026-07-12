---
type: governance
title: Environment Network Access Requirements
status: active
created: 2026-07-12
updated: 2026-07-12
---

# Environment Network Access Requirements

Operational note for the Claude Code remote environment running this repository. This is a **living allowlist** — extend it as new load-bearing sources appear (see "Adding domains as needed" below).

## Problem this solves

The environment is on the default **"Trusted"** network access level. Trusted allows GitHub and package registries (npm, PyPI, RubyGems, crates.io) and Anthropic-hosted services, and **blocks the general web**. That is why `git push` and `WebSearch` work but direct source fetching does not.

Confirmed by direct test on 2026-07-12 (`curl` + `WebFetch`):

| Reachable under Trusted | Blocked (403 at proxy, `connect_rejected`) |
|---|---|
| github.com, raw.githubusercontent.com | google.com, en.wikipedia.org |
| pypi.org | archive.org, fred.stlouisfed.org |
| code.claude.com | mpra.ub.uni-muenchen.de, www.bankofengland.co.uk |

Consequence: no HIS-001 academic or primary source can be opened, so no source can move past `access-failed` in `HIS-001_SOURCE_REGISTER.md`, and Stage C cannot cite exact pages/tables/datasets. This is an infrastructure constraint, not a research-design problem.

## How to fix (must be done by the User — cannot be changed from inside a session)

Edit the environment → **Network access** selector → keep the **Trusted** level and **add custom allowed domains** from the list below. (Docs: https://code.claude.com/docs/en/claude-code-on-the-web — "Network access".) A custom allowlist is preferred over switching to full outbound access, per the project discipline of not operating as a general web crawler.

After configuration, the Research Lead re-tests access and upgrades each affected Source Register row from `access-failed` to `verified-open` / `verified-partial` / `verified-paywalled`.

## Tier 1 — required now (8 domains, unlock core HIS-001 evidence)

| Domain | Unlocks | Serves |
|---|---|---|
| `archive.org` | Bradshaw's Railway Manual, Henry Tuck's Shareholder's Manual, Fogel (1964), Poor's Manual volumes, Railway Times | QT2/QT3/QT4/QT5, cash-flow candidate, US failure quota |
| `fred.stlouisfed.org` | NBER Macrohistory railway-mileage-authorized series | QT1, QT4 (overbuild) |
| `mpra.ub.uni-muenchen.de` | Campbell working papers (Greatest Bubble, Cross-Section, Myopic Rationality) | QT4 Mania interpretation |
| `papers.ssrn.com` | SSRN preprints (Deriving the Railway Mania; Odlyzko; Donaldson & Hornbeck) | QT4, QT5, both Gate 2 pairs |
| `www.bankofengland.co.uk` | "A Millennium of Macroeconomic Data" (consol yields, deflators) | Gate 1 U1/U6 benchmark |
| `babel.hathitrust.org` | Poor's Manual and other public-domain full-view volumes | US failure quota |
| `pureadmin.qub.ac.uk` | QUB repository (Dispelling the Myth; Deriving the Railway Mania; What Moved Share Prices) | QT4, benchmark |
| `api.parliament.uk` | Historic Hansard (1850 Railway Returns & Audit debate) | QT3 accounting/audit |

## Tier 1 — supplementary (broaden coverage; add with the above if convenient)

```
quceh.org.uk              # Before the Cult of Equity; Provincial Stock Markets
dspace.stir.ac.uk         # Rule Britannia! (Acheson/Hickson/Turner/Ye)
researchonline.lse.ac.uk  # Leunig social-savings survey
eprints.lse.ac.uk         # Leunig "Time is Money"; Crafts WP
wrap.warwick.ac.uk        # Bryer (1991); Mitchell/Chambers/Crafts
ageconsearch.umn.edu      # Mitchell/Chambers/Crafts WP
egrove.olemiss.edu        # Development of British Railway Accounting 1800-1911
orca.cardiff.ac.uk        # Bottomley (2025) steam-power reassessment
www-users.cse.umn.edu     # Odlyzko self-hosted papers
ideas.repec.org           # RePEc metadata/links
econpapers.repec.org      # RePEc metadata/links
econstor.eu               # Nuvolari/Verspagen/von Tunzelmann
scholarship.law.cornell.edu # Lubben (2004) railroad receiverships
dave-donaldson.com        # Donaldson & Hornbeck open copy
sites.socsci.uci.edu      # Bogart transport-revolution survey
www2.census.gov           # Historical Statistics of the US (free 1949/1960 eds.)
firstmonday.org           # Odlyzko "Bubbles, Gullibility"
www.railwaysarchive.co.uk # Board of Trade / railway documents
```

## Orientation-only (lower priority; never load-bearing evidence)

```
en.wikipedia.org          # pointers/cross-checks only
www.gracesguide.co.uk     # company-history pointers only
```
Per `governance/OPERATING_PRINCIPLES.md`, these may motivate a question but must never support a claim classified as historical fact or quantitative estimate.

## Known gotchas

- **archive.org file downloads redirect to numbered CDN hosts** (e.g. `ia*.us.archive.org`, `dn*.us.archive.org`). If item pages load but downloads fail, allow `*.archive.org` (wildcard) rather than only the bare domain.
- **HathiTrust** may serve assets from `babel.hathitrust.org` plus `catalog.hathitrust.org`; add both if needed.
- **Bank of England** dataset mirrors exist at `kaggle.com` and `datahub.io` if `bankofengland.co.uk` proves awkward.
- Some university repositories deliver PDFs from a separate assets subdomain; if a landing page loads but its PDF 403s, add that subdomain.

## Adding domains as needed

This list is not final. When a new load-bearing source surfaces during Stage C or later:

1. Add its domain here with a one-line "unlocks / serves" note (keep the table format).
2. Ask the User to add it to the environment allowlist.
3. Record the access re-test result in `HIS-001_SOURCE_REGISTER.md`.

Keep the allowlist minimal and justified — a domain earns a place only if it unlocks evidence that materially improves claim coverage, triangulation, counter-evidence, methodology, or bias control (per the Gate 1 research-budget guardrail).
