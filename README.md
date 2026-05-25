<!-- Replace this with your banner image -->
<p align="center">
<img width="3360" height="1890" alt="STOCK DEEP DIVER (2)" src="https://github.com/user-attachments/assets/e10fc109-4400-4d54-a51c-b9bc59326fe6" />
</p>

<p align="center">
  <strong>Institutional-grade stock research for Claude Code.</strong><br>
  No made-up numbers, no price predictions — just decisive analysis with the right framework for every sector.
</p>

<p align="center">
  <a href="#installation"><img src="https://img.shields.io/badge/install-30%20seconds-brightgreen" alt="Install" /></a>
  <a href="#license"><img src="https://img.shields.io/badge/license-MIT-blue" alt="License" /></a>
  <a href="#"><img src="https://img.shields.io/badge/built%20for-Claude%20Code-orange" alt="Built for Claude Code" /></a>
  <a href="#"><img src="https://img.shields.io/badge/no%20price%20predictions-by%20design-red" alt="No predictions" /></a>
</p>

---

## What it does

Fathom turns Claude into a junior equity analyst who actually does the work. You ask a stock question — it pulls live filings, applies the right framework for the sector, pressure-tests your thesis, and gives you the structured answer a human analyst would build in 3-4 hours, in about 5 minutes.

It runs 13 research modes — from a 200-word snapshot to a full 4,000-word institutional report — and picks the right one based on what you ask.

---

## Why it's different

### 🎯 Honest ratings
How solid the analysis is — not buy/sell. Distressed names, VIE structures, and binary-outcome stocks get auto-capped at "Speculative" regardless of how clean the bull case looks.

### 🏗️ Sector-smart
Standard P/E is wrong for banks, REITs, biotech, oil & gas. Fathom detects the sector and applies the right lens — P/B + NIM + CET1 for banks, P/FFO + AFFO yield for REITs, risk-adjusted pipeline NPV for biotech.

### 🛡️ Anti-bias
Detects bullish or bearish lean in your prompt and pushes back. If you sound like you're already in love with the stock, the bear case gets weighted harder, not softer.

### 🔬 Zero fabrication
Never invents numbers. Never predicts prices. Only scenario-conditioned ranges — *"if margin reaches 35% and multiples re-rate, framework implies $X"* — with the conditions attached.

---

## Quick examples

**Ask:** *"deep dive on NVDA"*
**Get:** Full report — snapshot, business + moat, financials with red-flag scan, valuation with implied-growth check, bull case, bear case, signals (insider/13F/short/options), and a decisive framework view with thesis breakpoints. ~2,500 words.

**Ask:** *"is BABA a good buy"*
**Get:** Same depth, plus a mandatory VIE structure warning at the top and Evidence Strength capped at Moderate because no business analysis can mitigate Chinese policy risk.

**Ask:** *"compare MSFT vs GOOGL"*
**Get:** Head-to-head with side-by-side metrics, dimension-by-dimension winners (lower risk / higher growth / better value / stronger moat / better balance sheet), and a framework view per ticker.

**Ask:** *"I own PYPL and I'm down 30% — what now?"*
**Get:** Position review with thesis-intactness check (is the reason you bought still true?), what's changed, cognitive-bias check, and three frameworks for deciding (would-you-buy-fresh-today, has-the-thesis-changed, opportunity-cost). No buy/hold/sell verdict — that depends on your tax situation, other holdings, and time horizon.

**Ask:** *"DCF on COST"*
**Get:** 10-year FCF projection with every assumption labeled and sourced, 3×3 sensitivity table (growth × discount rate), implied-growth check ("the market is pricing in X% — is that achievable?"), and explicit `[ASSUMED]` tags on any input that isn't from a primary source.

---

## All 13 modes

| Mode | When it fires | Output |
|---|---|---|
| **Snapshot** | "What's up with X" | 200-400 words |
| **Quick** | "Thoughts on X" | 300-600 words |
| **Full** | "Deep dive on X" | 1,800-4,000 words |
| **Compare** | Two tickers | 800-1,500 words |
| **Basket** | 3+ tickers | 1,200-2,500 words |
| **Position** | "I own X" | 1,000-1,800 words |
| **DCF** | "DCF on X" | 1,500-2,500 + tables |
| **Scenario** | "What if X happens" | 800-1,200 words |
| **Single-side** | Bull-only or bear-only | 1,200-2,000 words |
| **Short-side** | "Considering shorting X" | 1,200-1,800 words |
| **Cross-asset** | "X stock vs gold/BTC" | 800-1,200 words |
| **Claim-eval** | Pasted article/DD post | 800-1,500 words |
| **Risk-focus / ESG / Compress / Drill-down** | Targeted asks | Varies |

---

## Installation

**Prerequisites:** [Claude Code](https://www.anthropic.com/claude-code) with WebSearch enabled.

```bash
# Clone into your global skills directory
git clone https://github.com/[your-username]/fathom ~/.claude/skills/fathom
```

That's it. The skill auto-loads in every Claude Code session.

**Verify it's installed:**
```bash
ls ~/.claude/skills/fathom/
# Should show: SKILL.md  references/  templates/
```

---

## How to use it

Just talk to Claude Code like you would a research analyst. Some examples:

```
deep dive on NVDA
compare MSFT vs GOOGL vs AMZN
is BABA a good buy given Chinese tech policy
I own PYPL and I'm down 30% — what now
DCF on COST with current consensus inputs
short-side analysis on TSLA
what would happen to AAPL if China revenue dropped 50%
```

Or invoke explicitly via slash command if you want to be sure it fires:

```
/stock-deep-dive-pro
```

---

## What's in the box

```
fathom/
├── SKILL.md                          # The main skill instructions
├── references/
│   ├── research_framework.md         # 8-section analytical checklist
│   ├── data_sources.md               # Source hierarchy + EDGAR recipes
│   ├── red_flags.md                  # Accounting, governance, capital-structure flags
│   └── sector_frameworks.md          # Bank, REIT, biotech, insurance, oil & gas, VIE, SPAC, ETF
└── templates/
    ├── report_template.md            # Full institutional report
    ├── quick_template.md
    ├── compare_template.md
    ├── basket_template.md
    ├── position_template.md
    ├── cross_asset_template.md
    └── dcf_template.md
```

The skill loads references **on demand** — Quick mode doesn't pay the token cost for sector frameworks, Full mode loads what it needs based on the sector flag that fires.

---

## What it deliberately won't do

- **Predict prices.** Scenario-conditioned ranges only — never "I think NVDA will hit $300."
- **Tell you to buy or sell.** That depends on your tax situation, other holdings, risk tolerance, time horizon — stuff the skill can't know.
- **Fabricate numbers.** If a number isn't in search results or filings, it says so. Gaps are flagged, not filled with plausible fiction.
- **Continue on claimed MNPI.** If you tell it your friend at the company leaked earnings, it refuses to research that ticker further (Rule 10b-5 exposure).
- **Run without web access.** Stock data goes stale fast — Fathom refuses to produce reports from training data alone.

These aren't limitations — they're the entire point. Tools that confidently predict prices and rate stocks Buy/Hold/Sell are noise that gets people hurt.

---

## How it's built

- **Built for Claude Code** — uses native `WebSearch` and `WebFetch` tools, no custom infrastructure
- **Mandatory floors enforced in SKILL.md** — distressed names, VIE structures, customer concentration, recent IPOs, OTC listings all get auto-capped at the appropriate Evidence Strength level regardless of which references are loaded
- **Source hierarchy** — SEC filings > company IR > earnings call transcripts > aggregators (with explicit tie-breakers when sources conflict)
- **Gap-fill loop** — every Full-mode report scans its own draft for data gaps and runs targeted searches to close them before shipping
- **Battle-tested** — 5 rounds of adversarial review + live test cases (megacap, distressed, Chinese ADR, recent IPO) before public release

---

## Limitations (the honest ones)

- **DCF math can't be externally verified inside an LLM context.** Fathom labels every assumed input explicitly, but the user should drop assumptions into a spreadsheet for real model building.
- **Day-trade decisions need order-book and options-flow data Fathom doesn't pull.** If you ask for a day-trade view, the skill tells you it's out of scope and gives you news/catalyst flow instead.
- **Foreign issuers with non-English primary disclosure** get Evidence Strength capped at Moderate, because Fathom can only read what's translated.
- **Coverage of OTC / pink-sheet stocks is limited** — search returns thin data for these names and the skill correctly flags that rather than padding.

---

## License

MIT. Use it, fork it, modify it. If you ship improvements, a PR would be appreciated but isn't required.

---

## Contributing

PRs welcome. The highest-value contributions:
- New sector frameworks (specialty REIT types, infrastructure, defense)
- Additional mandatory floors for risk patterns the current list misses
- Real test cases — running the skill on a stock and reporting what it got right/wrong

---

## Acknowledgments

Built on [Claude Code](https://www.anthropic.com/claude-code) by Anthropic. Inspired by every junior analyst who's ever been told their report "isn't decisive enough" and every senior PM who's been burned by overconfident sell-side predictions.

---

<p align="center">
  <em>Research, not financial advice. Do your own due diligence. Consult a licensed financial advisor before any investment decision.</em>
</p>
