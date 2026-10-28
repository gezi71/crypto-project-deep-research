# Crypto Project Deep Research

**Crypto research engine first, publishing layer second: stable research discipline, optional articles, charts when useful.**

English · [简体中文](README.zh-CN.md)

A reusable Agent Skill for researching crypto projects, protocols, tokens, blockchains, DeFi, infrastructure, and crypto companies. It guides an agent through source verification, protocol economics, growth quality, supply dilution, valuation, and risk—then evaluates the protocol and token separately.

**Discover** distinguishes rising attention from improving fundamentals and selects what to research next. It produces research candidates, not buy recommendations, and does not automatically run full research on the shortlist.

The central question: **What creates value, who pays for it, who captures it, and what could make the thesis wrong?**

## What you get

Analyze, Deep Dive, Compare, and Update default to a **Research Package**: research notes, evidence ledger, discrepancy/data-gap table, calculation workpapers, data/source tables, thesis, bull/base/bear analysis, valuation, risks, unresolved questions, and confidence. Research completion does not imply publication generation.

Only an explicit article or publication request activates the publishing layer. These outputs remain available on request:

| File | Deliverable |
| --- | --- |
| `article.zh-CN.md` | Publishable Chinese research article with a clear argument and narrative. |
| `article.en.md` | Full English article with equivalent reasoning, evidence, and counterarguments. |
| `social-post.zh-CN.md` | Standalone Chinese short post focused on one important finding. |
| `social-post.en.md` | English short post expressing the same finding and material limits. |

Requested articles retain the same writing standards: a worthwhile question, evidence, causal reasoning, counterarguments, judgment, and what to watch next. Generate only the requested languages and formats; a general article request uses the conversation language and long form. Discover defaults to a Candidate Shortlist and verification workpapers, then stops; publishing also requires an explicit request.

Research and articles may contain zero, one, or several charts. There is no chart quota: use charts only when they materially improve understanding, validation, comparison, or communication. Sources, dates/periods, units, denominators, CSV data, reproducible scripts, and visual checks remain required for generated charts. Nothing is published automatically.

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

You can specify the research cutoff, output language, valuation horizon, currency, and output directory. Defaults are the current cutoff, USD, and a 12-month valuation horizon. Full research stops at the Research Package unless you explicitly request publishing output. For example, `Analyze: Aave` produces research only; `Analyze: Aave + write an English long-form article` adds only `article.en.md`. Natural language works; no fixed syntax is required. Explicit requests for a due-diligence report or a particular platform take precedence.

For example, explicitly request both long articles and short versions as X threads:

```text
$crypto-project-deep-research Analyze: Zama https://www.zama.org/
Generate both long articles. Format the Chinese and English short posts as X threads.
```

### Discover: find research candidates

```text
$crypto-project-deep-research Discover: DeFi projects worth researching in the past 30 days
Discover: Trending crypto projects in the past 7 days
Discover: Projects with improving fundamentals but relatively low market attention
```

Optional filters: time window, sector, chain, token-issued/unissued status, circulating market-cap range, excluded projects, candidate count, and output language. Defaults: **past 30 days, all sectors and chains, issued and unissued projects, no market-cap filter or exclusions, and a Candidate Shortlist in the conversation language**. There is no fixed candidate count; user-specified counts are upper limits. The output discloses the cutoff and actual data coverage; it never claims to scan the entire market.

For a narrower screen, specify the conditions in natural language:

```text
$crypto-project-deep-research Discover: DeFi projects in the past 7 days.
Chains: Ethereum and Base. Issued tokens only.
Circulating market cap: USD 100 million–5 billion. Exclude Aave.
Return up to 5 research candidates. Write the output in English.
```

Fewer credible candidates are better than a full list padded with weak ideas. If only three qualify under an upper limit of five, return three. Zero qualified candidates is valid: state “no sufficiently strong candidates” and explain the checked scope and exclusions. Unissued projects or projects with unknown market cap cannot be assumed to pass a numeric market-cap filter.

Candidates can carry multiple labels: **Attention-driven**, **Fundamentals-improving**, **Catalyst-driven**, and **Potential divergence**. Low attention alone is not undervaluation; a price rally is not investment merit. Growth uses the previous equal-length window and shows absolute scale and change, with checks for low bases, incentives, Sybil activity, wash trading, price effects, and one-off events.

Discovery is a research prioritization workflow, not a publishing workflow. Each candidate includes project/sector, a dated Why Now and concrete evidence, fundamental signal, token/value-capture relevance, main uncertainty, key research question, priority, confidence, and recommended next action. Tables, cards, or prose are all acceptable. “Popular,” price gains, narrative strength, and social attention are leads rather than sufficient fundamental evidence.

The output includes a candidate shortlist, separate **Attention / Fundamentals / Catalyst / Research Priority / Confidence** assessments, up to three leading research cards, source/data-gap workpapers, and copyable Analyze/Deep Dive prompts. Research Priority means “worth investigating next,” not “expected investment return.” It is not an investment rating; missing data stays N/A and may prevent ranking. Cross-sector ordering must be explained. Discover asks what deserves deeper research; Analyze builds the full research and investment thesis. Discovery-level checks do not establish Buy/Sell/Avoid, undervaluation, overvaluation, or a clear winner. Next actions can be Research, Watch, Low Priority, or Drop, with reasons and unresolved questions; no Analyze is executed automatically.

Discover completion does not imply publication generation. Publishing after Discover is optional and request-driven: `Discover DeFi projects + write an English article` first completes the shortlist, then adds only `article.en.md`. Charts are unnecessary by default and appear only when they materially help candidate comparison or judgment; there is no mandatory count. See [the Discover workflow](references/discover.md).

**Language:** the executable instructions and reference documents are written in Chinese. Research workpapers follow the conversation language. Publication languages and formats follow the request; when both long articles are requested, the English version has equivalent depth rather than summarizing the Chinese version. Discover shortlists also follow the conversation language unless otherwise requested. Progress messages follow the user's language.

## Research output

For full research, the [research workpaper framework](references/report-template.md) contains **31 modules**, including:

1. Executive summary, core thesis, product, market, and protocol economics.
2. Fundamental metrics and growth quality over 30D, 90D, 180D, and 1Y where data exists.
3. Tokenomics, value capture, sell-pressure scenarios, funding, and treasury.
4. Competition, moat, decentralization, security, governance, and regulatory risk.
5. Relative, historical, and scenario valuation; catalysts; risks; and opposing theses.
6. An 11-dimension scorecard, answers to 12 concluding questions, separate protocol/token verdicts, confidence, and sources.

The 31 modules are a **coverage and audit framework, not a mandatory reasoning sequence**. Identify the core economic question and thesis-critical variables, investigate them and their causal chains, then audit coverage and fill material gaps. Research depth is asymmetric: critical modules receive deep coverage, relevant ones standard coverage, low-materiality ones brief coverage, non-applicable ones explicit N/A with reasons, and unavailable data explicit gaps. Notes may follow the project’s logic rather than 31 fixed sections; a coverage matrix maps every module to its actual location or status.

The full framework is covered in `research-notes.md`, with an **evidence ledger**, a **discrepancy/data-gap table**, and **calculation workpapers** in accompanying Markdown/CSV files. Missing or non-applicable items are explained there. Discover keeps its own screening framework without full-project verdicts. Public articles are organized around their argument, not these module headings. A conventional module-by-module due-diligence report is available when explicitly requested.

The 11 integer dimension scores remain diagnostic aids. Summaries prioritize a qualitative profile of protocol/business quality, token value capture, growth, valuation, dilution/governance risk, and confidence. Overall Score is optional, secondary, and rounded to an integer rough diagnostic; existing evidence gates still apply. It cannot substitute for the thesis or valuation, determine Buy/Avoid automatically, or serve as the sole ranking criterion. Compare dimensions rather than small aggregate differences. Old research packages and decimal totals remain readable without migration.

When requested, both long articles retain the central argument, decisive evidence, counterarguments, and material uncertainty. Short posts develop one independently readable finding; they do not squeeze every research module into a sentence. Clear writing never upgrades an unverified claim into a fact. See [bilingual long- and short-form writing](references/delivery-and-social.md).

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
│   ├── report-template.md           # Complete 31-module research workpapers
│   ├── delivery-and-social.md       # Bilingual long articles and short posts
│   ├── scoring.md                   # Scorecard, verdicts, confidence
│   └── data-charts.md               # Need-based charts, data and reproducibility
├── README.md
└── README.zh-CN.md
```

## Requirements and limitations

This is an **instruction-based skill**, not a market-data service, trading bot, or standalone executable. Live research requires browsing, public APIs, blockchain explorers, or connectors supplied by the host agent. Paid datasets are optional; inaccessible sources must be disclosed. No wallet signature or transaction is required for the research workflow.

Discover does not trade, create scheduled tasks, or require paid services. Without reliable recent data it discloses the limitation instead of inventing a trending list.

Structure, internal links, metadata, and worked calculation examples have been checked. A source-limited Zama Analyze run was completed on **2026-10-22**, covering the 31-module framework, evidence/data-gap workpapers, and conditional supply calculations. It did not establish fully verified live economics or contract state. The Research First workflow has passed structural/link checks and manual instruction walkthroughs, but has **not yet been tested end to end**. There is no existing automated research test suite in this repository. The installer command has not been end-to-end tested in this environment. Research quality depends on source availability and the executing agent; output still requires review.

Discover was exercised on a live 30-day DeFi request on **2026-10-21**, including equal-window recomputation, source limitations, unranked watchlist entries, and exclusion of misleading signals. This bounded screening run does not validate exhaustive coverage or complete project research.

Scores and scenario valuations are research tools, not investment advice, price guarantees, legal opinions, or smart-contract audits.
