# Crypto Project Deep Research

**Evidence-first crypto research, from protocol fundamentals to token value capture.**

English · [简体中文](README.zh-CN.md)

A reusable Agent Skill for researching crypto projects, protocols, tokens, blockchains, DeFi, infrastructure, and crypto companies. It guides an agent through source verification, protocol economics, growth quality, supply dilution, valuation, and risk—then evaluates the protocol and token separately.

The central question: **What creates value, who pays for it, who captures it, and what could make the thesis wrong?**

## What it covers

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

Natural-language requests work too. Add an official URL or chain and contract address when the project name is ambiguous.

You can specify the research cutoff, output language, valuation horizon, currency, and output directory. Defaults are the current cutoff, Chinese output, USD, and a 12-month valuation horizon. For an English report, append `Write the report in English.`

**Language:** the executable instructions and reference documents are currently written in Chinese. These README files are bilingual; the skill instructs the agent to follow the requested report language.

## Research output

The [report template](references/report-template.md) contains **31 modules**, including:

1. Executive summary, core thesis, product, market, and protocol economics.
2. Fundamental metrics and growth quality over 30D, 90D, 180D, and 1Y where data exists.
3. Tokenomics, value capture, sell-pressure scenarios, funding, and treasury.
4. Competition, moat, decentralization, security, governance, and regulatory risk.
5. Relative, historical, and scenario valuation; catalysts; risks; and opposing theses.
6. An 11-dimension scorecard, answers to 12 concluding questions, separate protocol/token verdicts, confidence, and sources.

Reports include an **evidence ledger**, a **discrepancy/data-gap table**, and **calculation workpapers**, either in appendices or accompanying Markdown/CSV files. Non-applicable sections are explained rather than filled with invented numbers.

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
│   ├── analysis-methods.md          # Economics, supply, treasury, valuation formulas
│   ├── sector-metrics.md            # Metrics tailored to different business models
│   ├── report-template.md           # Complete 31-module report framework
│   └── scoring.md                   # Scorecard, verdicts, confidence
├── README.md
└── README.zh-CN.md
```

## Requirements and limitations

This is an **instruction-based skill**, not a market-data service, trading bot, or standalone executable. Live research requires browsing, public APIs, blockchain explorers, or connectors supplied by the host agent. Paid datasets are optional; inaccessible sources must be disclosed. No wallet signature or transaction is required for the research workflow.

Structure, internal links, metadata, and worked calculation examples have been checked. A complete real-project research run has **not yet been validated**. The installer command is provided for distribution and has not been end-to-end tested in this environment. Research quality depends on source availability and the executing agent; output still requires review.

Scores and scenario valuations are research tools, not investment advice, price guarantees, legal opinions, or smart-contract audits.
