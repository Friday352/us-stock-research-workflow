[SKILL.md](https://github.com/user-attachments/files/27474842/SKILL.md)
---
name: us-stock-research-workflow
description: "Comprehensive US stock research workflow covering full-stack value chain mapping, financial data queries, news & media tracking, analyst ratings analysis, risk assessment, earnings checklist, and capital fit evaluation. Outputs a structured MD report."
agent_created: true
---

# US Stock Research Workflow

## Purpose

When the user wants to research a US stock, systematically execute a complete analysis from industry understanding to final actionable recommendation. Ensures every research session covers the same dimensions with no key information missed.

## Trigger Conditions

The user says:
- "Research / analyze stock XXX"
- "How's this stock?"
- "Is XXX worth buying?"
- "Look into XXX"
- Or any context where the user asks for an in-depth analysis of a specific US stock

## Workflow

### Step 1: Full-Stack Value Chain Mapping

Based on the Reddit r/Stocks_Picks methodology:

1. **Identify the industry** — Which major sector does this stock belong to? (AI infrastructure, financials, biotech, energy, etc.)
2. **Break down the value chain** — List the complete chain from upstream to downstream
3. **Identify the bottleneck** — Which link has the tightest supply, highest tech barrier, hardest substitution?
4. **Locate the company** — Where in the chain does it sit? Is it at the bottleneck or not?

Output format:
```
Industry: XX

Value Chain: Upstream(A) → Midstream(B) → Downstream(C)
Bottleneck: [Bottleneck name] — Why
Company Position: [Position description]
Core Moat: [Competitive advantage]
```

### Step 2: Fundamental Data Fetching

Use `neodata-financial-search` to query the following:

1. **Trading Data**
   - Current price, 52-week range, YTD return
   - Market cap, average daily volume, turnover rate

2. **Financial Data**
   - Revenue & growth rate (last 4 quarters + YoY)
   - Gross margin, net margin
   - EPS & growth rate
   - Free cash flow / burn rate
   - Cash & equivalents (solvency check)

3. **Valuation Metrics**
   - Forward P/E / P/B / P/S
   - vs industry peers (cheap or expensive)

4. **Analyst Ratings**
   - Buy/Hold/Sell ratio
   - Mean price target & range
   - Recent rating changes direction

### Step 3: News & Media Search

Run at least two rounds of searches:

1. **Company-specific News**
   - Latest earnings summary
   - Product/technology progress
   - Management changes
   - Legal/regulatory events

2. **Industry Trend News**
   - Current macro trends in the sector
   - Competitive landscape changes
   - Policy/regulatory movements

3. **Reddit/Social Media Sentiment (optional)**
   - If the user mentions Reddit discussions, fetch hot posts
   - Assess discussion quality (reasoned analysis vs baseless pumping)

### Step 4: Risk Assessment

| Risk Dimension | Assessment Question | Level (Low/Med/High) |
|--------------|-------------------|---------------------|
| Industry Risk | Is this sector growth or cyclical? | |
| Valuation Risk | Where is the current valuation vs history? | |
| Capital Fit | Is the share price suitable for the user's capital? (infer from context) | |
| Position Risk | What % of total capital would this position be? | |
| Catalyst Risk | Is the next catalyst clear? What if it disappoints? | |
| Liquidity Risk | Is daily volume sufficient? | |

### Step 5: Capital Fit Assessment

Determine the user's capital from conversation context (e.g., memory files, prior discussion, or ask if unknown). Then generate a 3-tier position sizing plan:

| Price Range | Position Sizing Logic | Assessment |
|-----------|----------------------|-----------|
| < 5% of capital per share | Can buy many shares, diversified | Good for building a position |
| 5-10% per share | Can buy several shares | Acceptable |
| 10-30% per share | Can buy few shares, concentrated | Caution — single stock dominates |
| > 30% per share | 1 share or fractional only | Not recommended — unable to diversify |

Always show a conservative/neutral/aggressive plan with specific share counts and dollar amounts based on the user's actual capital.

### Step 6: Earnings Checklist (if earnings are upcoming)

1. Earnings date and time
2. Market expectations (EPS consensus, revenue consensus)
3. Last earnings performance (beat or miss? by how much?)
4. Key metrics to watch (customers, ARPAC, gross margin, etc.)
5. Post-earnings scenario analysis:
   - Beat → How much might it rise?
   - In-line → Digest or slight up?
   - Miss → How much might it fall?

### Step 7: Output Structured MD Report

The final report contains the following chapters:

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
