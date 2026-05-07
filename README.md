# us-stock-research-workflow

A comprehensive US stock research workflow skill for WorkBuddy / CodeBuddy. Systematically analyzes individual stocks through a 7-step process: industry value chain mapping, fundamental financial analysis, news & media scanning, analyst rating tracking, risk assessment, earnings checklist, and capital suitability evaluation.

## Features

- **Full-Stack Value Chain Mapping** — Map the complete industry supply chain, identify bottlenecks, and locate the company within it (methodology adapted from Reddit r/Stocks_Picks)
- **Financial Data Analysis** — Pull real-time financial metrics via neodata-financial-search (revenue, EPS, margins, FCF, PE, analyst ratings)
- **News & Media Tracking** — Search company-specific and industry-wide news to stay ahead of catalysts
- **Risk Assessment** — Six-dimension risk scoring: industry cyclicality, valuation position, capital fit, position concentration, catalyst clarity, liquidity
- **Earnings Checklist** — Pre-earnings analysis with scenario modeling (beat, meet, miss)
- **Capital Suitability** — Personalized position-sizing advice based on portfolio size (designed for small capital accounts, ~$1,400)
- **Structured MD Output** — Every analysis outputs a 10-section formatted report

## Installation

1. Copy `SKILL.md` to your WorkBuddy/CodeBuddy skills directory:
   - **Windows**: `%USERPROFILE%\.workbuddy\skills\us-stock-research-workflow\`
   - **macOS/Linux**: `~/.workbuddy/skills/us-stock-research-workflow/`

2. Or install via the skills marketplace once published.

## Usage

Simply mention the stock you want to research:

> "帮我分析一下 NU（Nu Holdings）"
> "研究一下 MU 这个股票"
> "RUN the research workflow on RDDT"

The skill triggers automatically when you ask for stock analysis.

## Prerequisites

This skill works best with the **neodata-financial-search** plugin enabled (built into WorkBuddy). For news and media searching, the standard `WebSearch` and `WebFetch` tools are used.

## Workflow Steps

| Step | Description |
|------|-------------|
| 1. Value Chain Mapping | Map industry structure, find bottlenecks, locate the company |
| 2. Financial Data | Pull price, market cap, revenue, EPS, PE, analyst targets |
| 3. News & Media | Company news + industry trends + optional Reddit sentiment |
| 4. Risk Assessment | Score 6 risk dimensions (high/medium/low) |
| 5. Capital Fit | Position sizing based on account size |
| 6. Earnings Checklist | Pre-earnings scenario analysis (if applicable) |
| 7. Report Output | Generate structured 10-section MD report |

## License

MIT

## Author

Created with WorkBuddy, May 2026. Methodology draws from Reddit community frameworks (r/Stocks_Picks, r/stockstobuytoday) and standard financial analysis practices.
