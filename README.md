# Crypto Project Deep Research

**Discover crypto projects, research their fundamentals, and turn the findings into full Chinese/English reports and bilingual social-media posts.**

English · [简体中文](README.zh-CN.md)

A reusable Agent Skill for researching crypto projects, protocols, tokens, blockchains, DeFi, infrastructure, and crypto companies. It guides an agent through source verification, protocol economics, growth quality, supply dilution, valuation, and risk—then evaluates the protocol and token separately.

**Discover** distinguishes rising attention from improving fundamentals and selects what to research next. It produces research candidates, not buy recommendations, and does not automatically run full research on the shortlist.

The central question: **What creates value, who pays for it, who captures it, and what could make the thesis wrong?**

## What you get

By default, each research run delivers four separate Markdown files:

| File | Deliverable |
| --- | --- |
| `report.zh-CN.md` | Complete Chinese research report for the selected mode. |
| `report.en.md` | Complete English report with the same evidence, scope, and conclusions. |
| `social-post.zh-CN.md` | Standalone Chinese social-media post built around the key findings. |
| `social-post.en.md` | English editorial version of the same post, adapted for English readers. |

Reports share an evidence ledger, a discrepancy/data-gap table, and calculation workpapers. Posts retain material risks, assumptions, dates, and direct sources. The default is one general-purpose long-form post per language; specify a platform, length, or thread format when needed. Posts are delivered as drafts and are not published automatically. Explicit requests for one language or only certain deliverables take precedence.

## What it covers

- **Candidate discovery:** recent signals, disclosed data coverage, independent attention/fundamentals assessments, and research prioritization.
- **Identity verification:** official domains, chains, contracts, versions, migrations, and similarly named assets.
- **Business fundamentals:** user needs, products, market size, competition, and structural moats.
- **Economic reality:** fees versus protocol revenue, supply-side revenue, incentives, and organic growth evidence.
- **Token analysis:** value capture, allocation, vesting, and cumulative supply changes over 3, 6, 12, and 24 months.
- **Valuation:** market cap and FDV, comparable and historical multiples, and bear/base/bull scenarios with explicit supply assumptions.
- **Control and risk:** team, funding, treasury, governance, decentralization, security, regulation, and liquidity.
- **Research judgment:** strongest bull and bear cases, catalysts, red flags, variant perception, thesis invalidation, and confidence.

The framework distinguishes **protocol quality, business quality, token quality, and token valuation**. A successful protocol does not necessarily create value for its token holders.

## Install

Using the [Skills CLI](https://skills.sh/):

```bash
npx skills add gezi71/crypto-project-deep-research --skill crypto-project-deep-research
```

Follow the installer prompts to select your agent and installation scope. This command requires Node.js/npm and network access.

Alternatively, clone the repository and ask your agent to read `SKILL.md`:

```bash
git clone https://github.com/gezi71/crypto-project-deep-research.git
```

Keep the complete directory: the entrypoint links to the files in `references/`. You can also place the folder in the skill directory supported by your agent.

## Use

In Codex, explicitly invoke the skill with a project and mode:

```text
$crypto-project-deep-research Analyze: Aave
```

| Mode | Example | Behavior |
| --- | --- | --- |
| Analyze | `Analyze: Aave` | Full research across all applicable modules. |
| Deep Dive | `Deep Dive: Ethereum` | Adds implementation evidence, metric provenance, sensitivity analysis, and stronger counter-evidence. |
| Compare | `Compare: Aave vs Morpho` | Applies the same framework, dates, definitions, and valuation assumptions to each project. |
| Update | `Update: Aave` | Compares against a dated prior report and reassesses the thesis. Without a baseline, creates current research and discloses that changes cannot be established. |
| Discover | `Discover: Trending crypto projects in the past 7 days` | Builds a disclosed, source-limited candidate pool, verifies signals, and prioritizes further research. |

Natural-language requests work too. Add an official URL or chain and contract address when the project name is ambiguous.

You can specify the research cutoff, output language, valuation horizon, currency, and output directory. Defaults are the current cutoff, USD, and a 12-month valuation horizon. Each run produces separate Chinese and English reports plus a social-media post in each language. Explicit requests for one language, reports only, posts only, or a particular platform/length take precedence.

For example, request platform-specific posts alongside the full bilingual reports:

```text
$crypto-project-deep-research Analyze: Zama https://www.zama.org/
Keep both complete reports. Write the Chinese and English social posts as X threads.
```

### Discover: find research candidates

```text
$crypto-project-deep-research Discover: DeFi projects worth researching in the past 30 days
Discover: Trending crypto projects in the past 7 days
Discover: Projects with improving fundamentals but relatively low market attention
```

Optional filters: time window, sector, chain, token-issued/unissued status, circulating market-cap range, excluded projects, candidate count, and output language. Defaults: **past 30 days, all sectors and chains, issued and unissued projects, no market-cap filter or exclusions, 10 candidates, separate Chinese and English reports and posts**. The output discloses the cutoff and actual data coverage; it never claims to scan the entire market.

For a narrower screen, specify the conditions in natural language:

```text
$crypto-project-deep-research Discover: DeFi projects in the past 7 days.
Chains: Ethereum and Base. Issued tokens only.
Circulating market cap: USD 100 million–5 billion. Exclude Aave.
Return up to 5 research candidates. Write the output in English.
```

If the evidence supports fewer candidates, the result explains the shortfall. Unissued projects or projects with unknown market cap cannot be assumed to pass a numeric market-cap filter.

Candidates can carry multiple labels: **Attention-driven**, **Fundamentals-improving**, **Catalyst-driven**, and **Potential divergence**. Low attention alone is not undervaluation; a price rally is not investment merit. Growth uses the previous equal-length window and shows absolute scale and change, with checks for low bases, incentives, Sybil activity, wash trading, price effects, and one-off events.

The output includes a candidate table, separate **Attention / Fundamentals / Catalyst / Research Priority / Confidence** assessments, up to three leading research cards, source/data-gap workpapers, and copyable Analyze/Deep Dive prompts. Research Priority is not an investment rating or expected return; missing data stays N/A and may prevent ranking. Cross-sector ordering must be explained. See [the Discover workflow](references/discover.md).

**Language:** the executable instructions and reference documents are written in Chinese. Deliverables default to both Chinese and English; the English report is complete, not an abridged summary. Progress messages follow the user's language.

## Research output

For full research, the [report template](references/report-template.md) contains **31 modules**, including:

1. Executive summary, core thesis, product, market, and protocol economics.
2. Fundamental metrics and growth quality over 30D, 90D, 180D, and 1Y where data exists.
3. Tokenomics, value capture, sell-pressure scenarios, funding, and treasury.
4. Competition, moat, decentralization, security, governance, and regulatory risk.
5. Relative, historical, and scenario valuation; catalysts; risks; and opposing theses.
6. An 11-dimension scorecard, answers to 12 concluding questions, separate protocol/token verdicts, confidence, and sources.

Reports include an **evidence ledger**, a **discrepancy/data-gap table**, and **calculation workpapers**, either in appendices or accompanying Markdown/CSV files. Non-applicable sections are explained rather than filled with invented numbers. Discover uses its own concise output rather than the full report or investment verdicts; Analyze, Deep Dive, Compare, and Update retain their existing behavior.

Both full reports preserve the selected mode's required coverage. Social posts develop a clear argument from that research instead of compressing every chapter; an English summary does not replace the complete English report. See [bilingual delivery and social editing](references/delivery-and-social.md).

## Evidence and calculation rules

- Prefer primary sources and attempt independent cross-verification of important metrics.
- Separate `Fact`, `Estimate`, `Interpretation`, and `Assumption`.
- Attach observation dates or measurement periods to changing data. Disclose conflicts and missing information.
- Distinguish addresses from people, fees from holder income, and unlocks from actual sales.
- Do not invent maximum supply for uncapped assets or token valuations for companies without a token.
- Match valuation rights, metric definitions, and supply denominators; avoid double-counting treasury, buybacks, or burns.
- Test how protocol revenue reaches token holders instead of assuming that it does.

## Repository structure

```text
.
├── SKILL.md                         # Entrypoint, workflow, modes, delivery checks
├── agents/openai.yaml               # Display metadata and default invocation
├── references/
│   ├── evidence.md                  # Sources, timestamps, verification, workpapers
│   ├── discover.md                  # Candidate discovery, screening, prioritization
│   ├── analysis-methods.md          # Economics, supply, treasury, valuation formulas
│   ├── sector-metrics.md            # Metrics tailored to different business models
│   ├── report-template.md           # Complete 31-module report framework
│   ├── delivery-and-social.md       # Bilingual reports and social-media posts
│   └── scoring.md                   # Scorecard, verdicts, confidence
├── README.md
└── README.zh-CN.md
```

## Requirements and limitations

This is an **instruction-based skill**, not a market-data service, trading bot, or standalone executable. Live research requires browsing, public APIs, blockchain explorers, or connectors supplied by the host agent. Paid datasets are optional; inaccessible sources must be disclosed. No wallet signature or transaction is required for the research workflow.

Discover does not trade, create scheduled tasks, or require paid services. Without reliable recent data it discloses the limitation instead of inventing a trending list.

Structure, internal links, metadata, and worked calculation examples have been checked. A source-limited Zama Analyze run was completed on **2026-10-22**, covering the 31-module framework, evidence/data-gap workpapers, and conditional supply calculations. It did not establish fully verified live economics or contract state. The new four-file bilingual delivery has **not yet been tested end to end**. The installer command has not been end-to-end tested in this environment. Research quality depends on source availability and the executing agent; output still requires review.

Discover was exercised on a live 30-day DeFi request on **2026-10-21**, including equal-window recomputation, source limitations, unranked watchlist entries, and exclusion of misleading signals. This bounded screening run does not validate exhaustive coverage or complete project research.

Scores and scenario valuations are research tools, not investment advice, price guarantees, legal opinions, or smart-contract audits.
