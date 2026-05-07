[README.md](https://github.com/user-attachments/files/27473760/README.md)
# US Stock Research Workflow

> One research session, seven dimensions, one complete report. Turns your AI assistant into a systematic equity analyst.

---

## Table of Contents

- [What This Is](#what-this-is)
- [Supported Platforms](#supported-platforms)
- [Workflow Overview](#workflow-overview)
- [Step-by-step Output Templates](#step-by-step-output-templates)
  - [1️⃣ Value Chain Mapping](#1-value-chain-mapping)
  - [2️⃣ Core Financials](#2-core-financials)
  - [3️⃣ Valuation Analysis](#3-valuation-analysis)
  - [4️⃣ Analyst Consensus](#4-analyst-consensus)
  - [5️⃣ News & Trends](#5-news--trends)
  - [6️⃣ Risk Assessment Matrix](#6-risk-assessment-matrix)
  - [7️⃣ Capital Fit & Conclusion](#7-capital-fit--conclusion)
- [Full Report Structure: 10-Chapter Template](#full-report-structure-10-chapter-template)
- [Usage Examples](#usage-examples)
  - [Example 1: NU Full Research Output](#example-1-nu-basic-research)
  - [Example 2: MU with Earnings Scenario](#example-2-mu-with-earnings-scenario)
  - [Example 3: CADL Small-cap Risk Assessment](#example-3-cadl-small-cap-risk-assessment)
- [Dependencies](#dependencies)
- [License](#license)

---

## What This Is

A structured US equity research workflow. When you say "research stock XXX", the AI systematically runs through seven analysis dimensions and outputs a **complete 10-chapter MD report** — from industry positioning to actionable buy/sell advice. Nothing gets skipped.

---

## Supported Platforms

| Platform | Installation |
|----------|-------------|
| **WorkBuddy** | Drop into `~/.workbuddy/skills/us-stock-research-workflow/` |
| **CodeBuddy** | Drop into `~/.workbuddy/skills/us-stock-research-workflow/` |
| **Codex CLI** | Into the corresponding skill directory |
| **Claude Code** | Load via MCP or skill directory |
| **Cursor** | Into `.cursor/skills/` |
| **Windsurf** | Into `.windsurf/skills/` |
| Any platform with YAML-frontmatter Skills support | Place SKILL.md into the corresponding skills directory |

---

## Workflow Overview

| Step | What It Does | Output Format |
|:----|:------------|:-------------|
| **1. Value Chain Mapping** | Break down industry, identify bottlenecks, locate the company | Chain diagram + positioning statement |
| **2. Core Financials** | Revenue, profit, growth, cash flow, margins | Data table (last 4 quarters + YoY) |
| **3. Valuation Analysis** | PE/PB/PS/EV-EBITDA, historical percentile, peer comparison | Valuation table + cheap/expensive call |
| **4. Analyst Consensus** | Rating distribution, price target range, trend changes | Rating table + target range |
| **5. News & Trends** | Company news + industry macro + optional Reddit sentiment | Event timeline + trend assessment |
| **6. Risk Assessment** | 6-dimension matrix (industry/valuation/capital/position/catalyst/liquidity) | Risk matrix (🟢🟡🔴) |
| **7. Capital Fit & Conclusion** | Position sizing for your budget + actionable next steps | Conclusion paragraph + trade plan |

---

## Step-by-step Output Templates

### 1️⃣ Value Chain Mapping

```
Industry: Latin American Digital Banking / Fintech

Value Chain Structure:
  Upstream (infrastructure) → Midstream (platform) → Downstream (end users)
  Payment networks, cloud computing, regulatory licenses → BaaS, risk engines → Individuals, merchants

Bottleneck: [Name of bottleneck]
  Why: Why this link is hardest to replicate / highest barrier

Company Position: [Company name] sits at [link]
  Moat: [Technology / User scale / Regulatory barrier / Brand]
  Competitive Landscape: [Main competitors, market share]

Chain Analysis:
  ✅ At the bottleneck / ⚠️ Not at bottleneck but fast-growing / ❌ In a red ocean
```

### 2️⃣ Core Financials

| Metric | Latest Q | Prior Q | YoY Change | Trend |
|:------|:--------|:-------|:----------|:-----|
| **Revenue** | $X.XB | $X.XB | +XX% | 📈/📉 |
| **Net Income** | $X.XB | $X.XB | +XX% | 📈/📉 |
| **EPS** | $X.XX | $X.XX | +XX% | 📈/📉 |
| **Gross Margin** | XX% | XX% | +XX pp | 📈/📉 |
| **Net Margin** | XX% | XX% | +XX pp | 📈/📉 |
| **Free Cash Flow** | $X.XB | $X.XB | +XX% | 📈/📉 |
| **Cash & Equivalents** | $X.XB | — | — | — |

> Key observations: [Call out any anomalies here]

### 3️⃣ Valuation Analysis

| Metric | Current | Industry Median | 5Y Range | Current %ile | Call |
|:------|:-------|:--------------|:--------|:-----------|:----|
| **Forward P/E** | XX.x | XX.x | X - XX | XX% | High / Fair / Low |
| **P/B** | X.x | X.x | X.x - X.x | XX% | High / Fair / Low |
| **P/S** | X.x | X.x | X.x - X.x | XX% | High / Fair / Low |
| **EV/EBITDA** | XX.x | XX.x | XX - XX | XX% | High / Fair / Low |

**Valuation Conclusion**:
- vs Industry: High / Fair / Low
- vs Own History: High / Fair / Low
- Composite: Fair value range $XX - $XX, current price $XX sits at [position]

### 4️⃣ Analyst Consensus

| Rating | Count | % |
|:------|:-----|:--|
| **Buy** | XX | XX% |
| **Hold** | XX | XX% |
| **Sell** | XX | XX% |

- Price Target Range: $XX - $XX (median $XX)
- Current Price vs Median Target: Discount / Premium of XX%
- Recent Rating Changes: Upgrades [X] / Downgrades [X] / Initiations [X]
- **Consensus Bias**: Bullish / Neutral / Bearish

### 5️⃣ News & Trends

Events organized as a timeline:

```
[2026-XX-XX] Event title / summary
  → Direction: Positive ❇️ / Neutral ➖ / Negative 🔻
  → Magnitude: Major / Moderate / Minor
  → Source: [URL]

[2026-XX-XX] ...
```

**Industry Trend**: Assessment of the sector's outlook (Positive / Neutral / Negative)
**Company-specific Catalysts**: List of clear catalysts in the next 3-6 months

### 6️⃣ Risk Assessment Matrix

| Risk Dimension | Assessment | Level | Notes |
|:-------------|:----------|:----|:-----|
| **Industry Risk** | [Description] | 🟢🟡🔴 | Cyclicality, competition, regulatory |
| **Valuation Risk** | [Description] | 🟢🟡🔴 | Current vs history vs peers |
| **Capital Fit** | [Description] | 🟢🟡🔴 | Does the share price fit your budget? |
| **Position Concentration** | [Description] | 🟢🟡🔴 | % of total portfolio after purchase |
| **Catalyst** | [Description] | 🟢🟡🔴 | Is the next catalyst clear and near? |
| **Liquidity** | [Description] | 🟢🟡🔴 | Daily volume, bid-ask spread |

**Composite Risk Level**: Low 🟢 / Medium 🟡 / High 🔴

### 7️⃣ Capital Fit & Conclusion

**Your Capital**: ~$1,400 principal (~¥10,000)

| Plan | Shares | Investment | % of Capital |
|:----|:------|:----------|:-----------|
| **Conservative** (recommended) | X shares | ~$XX | XX% |
| **Neutral** | X shares | ~$XX | XX% |
| **Aggressive** | X shares | ~$XX | XX% |

**Summary**:
```
✅ BUY / ⏸️ WAIT / ❌ DON'T BUY

Rationale:
1. [Reason 1]
2. [Reason 2]
3. [Reason 3]

Trade Plan:
- Entry: Limit order / Market order
- Target entry range: $XX - $XX
- Stop-loss: $XX (downside XX%)
- Profit-taking watch: $XX (upside XX%)

Watchlist:
- Next earnings: 2026-XX-XX
- Key metrics to monitor: [metric 1], [metric 2]
- Exit conditions: [description]
```

---

## Full Report Structure: 10-Chapter Template

The final report follows this structure:

```
# [Ticker] Deep Research Report — [Date]

## 1. Company Snapshot
## 2. Industry Value Chain Positioning (with full-stack map)
## 3. Core Financials (4 quarters + YoY trends)
## 4. Valuation Analysis (peer comparison + historical percentiles)
## 5. Analyst Consensus (rating distribution + price target range)
## 6. News & Trend Analysis (event timeline)
## 7. Risk & Reward Assessment (6-dimension matrix)
## 8. Capital Fit Recommendation
## 9. Watchlist Triggers (take-profit / stop-loss / add position)
## 10. Summary: Actionable Next Steps
```

---

## Usage Examples

### Example 1: NU (Basic Research)

**User:**
> Research NU (Nu Holdings). How's the stock?

**AI executes the full 7-step workflow and outputs:**

```
# NU (Nu Holdings) Deep Research Report — 2026-05-07

## 1. Company Snapshot

| Field | Value |
|:----|:-----|
| Company | Nu Holdings (NYSE: NU) |
| Industry | Latin American Digital Banking / Fintech |
| HQ | São Paulo, Brazil (incorporated in Cayman Islands) |
| Business | Nubank digital bank: credit cards, debit, savings, investments, insurance, crypto |
| Users | ~105M (Q4 2025) |
| Current Price | $14.48 |
| YTD Return | -14.2% |
| Market Cap | ~$64B |

## 2. Industry Value Chain Positioning

Industry: Latin American Fintech

Value Chain:
  Infrastructure (payment networks/regulatory) → Platform (risk engine/UX) → Endpoint (individuals/merchants)

Bottleneck: **Low-cost acquisition + high-engagement user base**
  → NU's digital marketing and 100M+ users create a dual moat

Company Position: Platform + Endpoint (vertically integrated)
  Moat: Scale effect in Brazil/Mexico/Colombia, low NPL (<4%), high brand recognition

## 3. Core Financials

| Metric | Q4 2025 | Q3 2025 | YoY | Trend |
|:-----|:-------|:-------|:--|:----|
| Revenue | $3.18B | $2.92B | +37% | 📈 |
| Net Income | $0.75B | $0.62B | +51% | 📈 |
| EPS | $0.15 | $0.12 | +50% | 📈 |
| Gross Margin | 45.1% | 43.8% | +1.3pp | 📈 |
| Net Margin | 23.5% | 21.2% | +2.3pp | 📈 |
| Active Users | 105M | 101M | +14% | 📈 |

> Revenue and profit both growing at high speed. Profitability consistently improving.

## 4. Valuation Analysis

| Metric | Current | Industry Median | 5Y Range | %ile | Call |
|:-----|:-------|:-------------|:--------|:---|:----|
| Forward P/E | 17.5x | 22.3x | 12-35x | ~35% | Low ✅ |
| P/B | 1.8x | 2.5x | 1.5-4.0x | ~30% | Low ✅ |
| P/S | 5.2x | 6.1x | 3.8-10x | ~25% | Low ✅ |

**Valuation Conclusion**: NU trades below its own historical averages and below industry medians. At 17x P/E with 30%+ growth, it's attractive for the LatAm fintech space.

## 5. Analyst Consensus

| Rating | Count | % |
|:-----|:-----|:--|
| Buy | 17 | 86% |
| Hold | 2 | 10% |
| Sell | 1 | 4% |

- Price Target Range: $16.50 - $22.00 (median $19.76)
- Current $14.48 vs Median Target $19.76: **36% upside**
- Recent Changes: 3 upgrades, 1 downgrade

## 6. News & Trends

[2026-04-XX] NU announces Mexico user base surpasses 30M
  → Direction: Positive ❇️ | Magnitude: Moderate

[2026-04-XX] Brazil central bank holds rate at 11.75%, benefiting fintech NIM
  → Direction: Positive ❇️ | Magnitude: Moderate

Industry Trend: LatAm digital banking penetration still below 40%, wide growth runway.

Catalysts: Q1 2026 earnings (~mid-May), Mexico credit card market share gains.

## 7. Risk Assessment

| Dimension | Assessment | Level |
|:---------|:----------|:----|
| Industry | Fintech is regulatory-sensitive, but LatAm has low penetration & strong growth | 🟡 |
| Valuation | Near historical lows, limited downside | 🟢 |
| Capital Fit | $14.48/share, easily multi-share for your budget | 🟢 |
| Concentration | Recommend max 30% allocation | 🟢 |
| Catalyst | Q1 earnings upcoming, near-term catalyst is clear | 🟢 |
| Liquidity | ~30M shares/day, highly liquid | 🟢 |

**Composite Risk**: Low 🟢

## 8. Capital Fit

Capital: ~$1,400 principal

| Plan | Shares | Investment | % of Capital |
|:----|:------|:----------|:-----------|
| Conservative | 25 shares | ~$362 | ~26% |
| Neutral | 40 shares | ~$579 | ~42% |
| Aggressive | 55 shares | ~$796 | ~58% |

## 9. Watchlist

- Add on dip: if post-earnings pullback to $12-13
- Stop-loss: $10.50 (down ~28%)
- Take-profit watch: $20+ (up ~38%)

## 10. Summary

NU is in a reasonable undervalued zone. The LatAm digital banking thesis has strong growth visibility, and current valuation provides a margin of safety. Recommend phased entry via limit orders, stop-loss at $12.50.
```

### Example 2: MU (with Earnings Scenario)

**User:**
> Analyze MU (Micron Technology). Should I buy?

**Key sections from the AI output:**

```
## 3. Core Financials

| Metric | Q1 2025 (FQ2) | YoY | Trend |
|:-----|:-------------|:--|:----|
| Revenue | $8.92B | +81% | 📈 |
| Net Income | $2.65B | +317% | 📈 |
| Adj. EPS | $2.33 | +313% | 📈 |

## 5. Valuation Analysis

Current Price: $666.59
Forward P/E: ~26x → Historical median ~15x — elevated

## 7. Risk Assessment

| Dimension | Level |
|:---------|:----|
| Valuation Risk | 🔴 Up 128% YTD, good news fully priced in |
| Capital Fit | 🔴 $666/share, you can only buy 1-2 shares (50%+ of capital) |

## 8. Capital Fit

| Plan | Shares | Investment | % of Capital |
|:----|:------|:----------|:-----------|
| Conservative | 1 share | ~$666 | ~48% |
| Aggressive | 2 shares | ~$1,332 | ~95% |

📌 **Note**: Even the conservative plan puts nearly half your capital into one stock.

## 10. Summary

Great company, bad price. After a 128% YTD run, valuation is stretched. At $666/share it's a terrible fit for small capital. Add to watchlist, consider buying if it pulls back below $500.
```

### Example 3: CADL (Small-cap Risk Assessment)

**User:**
> What about CADL? Is this biotech stock worth it?

**Risk assessment section from the AI output:**

```
## 7. Risk Assessment

| Dimension | Assessment | Level |
|:---------|:----------|:----|
| Industry | Biotech: binary outcome (home run or zero) | 🔴 |
| Valuation | No revenue, no profit — traditional valuation doesn't apply | 🔴 |
| Capital Fit | $7.63/share, easily affordable | 🟢 |
| Catalyst | BLA submission Q4 2026, still 6 months out | 🟡 |
| Liquidity | Small cap, low daily volume | 🟡 |

**Composite Risk**: High 🔴

## 10. Summary

High-risk speculative play. If you must, allocate no more than 5-10% of capital (~$70-140) and be prepared for a total loss.
```

---

## Dependencies

This skill requires the following capabilities (typically built into AI tools):

- **neodata-financial-search** or equivalent financial data query capability (real-time prices, financials, analyst ratings)
- **WebSearch** and **WebFetch** capabilities (news and media search)
- Ability to output structured Markdown reports

If financial data query capabilities are unavailable, alternative public data sources:
- **Yahoo Finance** — prices + financials
- **TradingView** — technicals + valuation comparison
- **MarketBeat** — analyst ratings + price targets
- **Finviz** — screening + visualization
- **SEC EDGAR** — 10-K / 10-Q filings

---

## License

MIT

---

## Author

Originally created May 2026.
Methodology references frameworks from Reddit (r/Stocks_Picks, r/stockstobuytoday) and standard equity analysis practices.
