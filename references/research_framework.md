# Research Framework — Full Checklist

Load when running Full, Compare, Basket, or Position mode. This is the underlying analytical checklist; the section structure in `SKILL.md` is the output format.

---

## Section 1 — Snapshot data points

**Standard companies (use this set):**
- Ticker, exchange, GICS sector + sub-industry
- Market cap (with size category: mega / large / mid / small / micro / nano)
- Current price (date-stamped)
- 52-week high and low (with date of each)
- P/E TTM, Forward P/E
- Revenue TTM, YoY revenue growth (most recent quarter)
- Net margin (TTM), Free cash flow yield
- Dividend yield (if applicable), Payout ratio
- Beta (5Y)
- Short interest % of float, days to cover
- Insider ownership %, Institutional ownership %
- Analyst consensus rating, mean / median / high / low PT, number of analysts

**Sector-specific overrides** — see `sector_frameworks.md`:
- Banks: P/B, P/TBV, ROTCE, NIM, Efficiency ratio, CET1
- REITs: P/FFO, AFFO yield, Dividend coverage, Same-store NOI, Occupancy
- Biotech (pre-revenue): EV, Cash position, Months of runway, Pipeline stage
- Insurance: P/B, Combined ratio, Float growth
- Oil & gas E&P: EV/EBITDA, Breakeven oil price, Reserve life

---

## Section 2 — Business & Moat checklist

**Revenue breakdown:**
- By segment / product line
- By geography (US, EMEA, APAC, LATAM, China specifically)
- By customer type (enterprise / SMB / consumer / government)
- Recurring vs one-time

**Customer concentration (from 10-K):**
- Top customers as % of revenue
- Largest single customer
- Government revenue %
- Contract durations and renewal cycles

**Moat types — name only what genuinely applies:**
- **Network effects** — value rises with users (Visa, Meta)
- **Switching costs** — painful to leave (Salesforce, Oracle, deep ERP installs)
- **Scale economies** — costs drop faster than peers (Costco, hyperscalers)
- **Intangible assets** — patents, FDA approvals, regulatory licenses
- **Brand** — pricing power from trust (LVMH, premium consumer)
- **Cost advantage** — structurally cheaper inputs (low-cost producers)
- **Counter-positioning** — incumbent can't copy without cannibalizing
- **Process power** — institutional knowledge competitors can't easily replicate (TSMC fab process)

Don't claim a moat that isn't there. "No durable moat — competes on price/execution" is a valid finding.

**Strategic moves (last 24 months):**
- M&A with dollar amounts
- C-suite changes (especially CEO, CFO, CTO)
- Buyback announcements + execution rate
- Dividend initiations or cuts
- Major partnerships, contract wins
- Capacity expansions or layoffs

---

## Section 3 — Financials deep dive

**Income statement (last 4 quarters + 5 years):**
- Revenue, Gross profit, Gross margin
- Operating income, Operating margin
- Net income, Net margin
- Diluted EPS, Share count trend (dilution check)

**Cash flow:**
- Operating cash flow
- Free cash flow (OCF − CapEx)
- **FCF conversion** = FCF / Net Income (~100% is clean reporting)
- Stock-based comp (treat as real expense; check SBC / revenue ratio)
- Working capital trends (AR, inventory, AP)

**Balance sheet:**
- Cash & equivalents, Short-term + long-term debt, Net debt
- Debt / EBITDA, Interest coverage (EBIT / interest)
- Current ratio, Quick ratio
- Goodwill as % of assets (impairment risk)
- Inventory turnover, DSO

**Capital allocation (most under-analyzed area in retail research):**
- Buybacks: dollars deployed, **net of SBC dilution**
- Dividends: total paid, growth rate, sustainability
- Reinvestment: R&D %, CapEx %
- M&A: total deployed, value-creating vs destroying
- **ROIC vs WACC** — anything below WACC is value-destroying. State the spread.

**Quality checks (each is a binary pass/fail):**
- Revenue growth > AR growth ✓
- Revenue growth > Inventory growth ✓
- FCF conversion > 80% ✓
- Operating margin trend (expanding / flat / compressing)
- Insider net buying in last 6 months
- Audit firm consistent for 5+ years

---

## Section 4 — Valuation

**Multiples (vs sector + own 5Y history):**
- P/E TTM, Forward P/E
- EV/Sales (especially unprofitable growth)
- EV/EBITDA, EV/FCF
- P/B (banks, real estate, asset-heavy)
- P/Sales (early stage)

**Growth-adjusted:**
- PEG (P/E / growth rate): <1.0 cheap for growth, >2.0 expensive
- Rule of 40 (SaaS): revenue growth % + FCF margin %
- LTV/CAC where available

**Implied-growth check (the key analytical move):**
- At current price + a sensible discount rate (10% default for equity, adjust for sector), what FCF growth rate is the market pricing in for the next 10 years?
- Is that higher than the company has ever achieved?
- Is the addressable market large enough to support it?
- **This is the single most useful valuation lens** — turns "expensive/cheap" into a testable question.

**Comparable companies:**
- 3-5 direct comps
- Table: company, market cap, P/E, EV/Sales, growth, op margin
- Identify where target trades at premium/discount and **explain why** (not just note the gap)

---

## Section 5 — Bull case checklist

Specific catalysts. Each should be:
- Named (not "AI tailwinds" → "Hyperscaler capex announcements indicating $X in 2026 capex")
- Quantifiable (dollar revenue impact, margin point impact)
- Dated where possible (next earnings, FDA PDUFA date, product launch)

Categories to scan:
- TAM expansion (with dollar size and source)
- Margin expansion (which specific cost line is compressing, why)
- Product roadmap (named upcoming releases)
- Geographic expansion (specific markets, timelines)
- M&A target potential (who could buy, at what premium)
- Multiple re-rating (what would change market view)
- Sum-of-parts undervaluation (conglomerates)
- Activist involvement or board pressure
- Spin-off or split potential

---

## Section 6 — Bear case checklist

Each risk needs proof, not assertion:
- Customer concentration with named at-risk accounts
- Competitive threats with named competitors and their advantages
- Margin compression with specific cost pressure (inputs, labor, FX)
- Regulatory: name the legislation, agency, timeline
- Litigation with damage estimates
- Refinancing: maturity wall and current rate environment
- Geopolitical: China revenue %, Taiwan exposure, sanctions risk
- Disruption: named technology/competitor that could obsolete
- Cycle exposure: where are we in the cycle (semis, housing, autos, advertising)
- SBC dilution > buybacks (net dilution)

---

## Section 7 — Signals checklist

**Insider trading (Form 4, last 12 months):**
- Net insider buying $ vs net insider selling $
- Cluster behavior (3+ distinct buyers or sellers in same window)
- CEO and CFO specifically
- 10b5-1 plans (scheduled — weaker signal) vs discretionary (stronger)

**Institutional positioning (most recent 13F):**
- Top 10 holders and recent position changes
- Initiations or exits by recognized institutional investors (Berkshire, Bridgewater, Pershing Square, etc.)
- Quarter-over-quarter direction matters more than absolute level

**Short interest:**
- Current % of float
- Days to cover (short ratio)
- 6-month trend
- Cost to borrow if findable

**Options market:**
- Implied volatility, IV rank
- Put/call ratio (>1 bearish positioning)
- Open interest concentration at strikes near current price
- Unusual options activity last 30 days

**Analyst activity:**
- Upgrades / downgrades last 90 days
- EPS estimate revisions (direction matters more than level)
- Top-ranked analyst reiterations

**Sentiment / qualitative:**
- Earnings call tone — confident, defensive, evasive (specific quotes)
- Management language changes vs prior calls
- Reddit / X chatter (contrarian indicator at extremes)
- Glassdoor employee sentiment trend
- Customer-facing review trends (G2, App Store, etc.)

**Macro / sector:**
- Sector ETF performance vs market
- Rate environment impact on this specific company
- FX exposure if international revenue >30%
- Commodity input sensitivity

**Geopolitical:**
- China revenue %
- Taiwan supply-chain exposure (semis, certain hardware)
- Russia/Ukraine exposure
- Sanctions risk
- Tariff exposure

---

## Section 8 — Verdict format

```
What the bulls need to be right:
1. [specific quantifiable thing]
2. [specific quantifiable thing]
3. [specific quantifiable thing — drop if only 2 hold]

What the bears need to be right:
1. [specific quantifiable thing]
2. [specific quantifiable thing]

What to watch (6-12 months):
- [Specific event with date — earnings, PDUFA, product launch]
- [Specific metric — track [X] crossing [threshold]]

Thesis breakpoints:
- Bull thesis breaks if: [specific trigger]
- Bear thesis breaks if: [specific trigger]

Framework view: [2-3 sentences. Decisive, evidence-based, not a price call.]
```

End with **one** Evidence Strength label: Strong / Moderate / Limited / Speculative. See SKILL.md for definitions and mandatory floors.

---

## ⚖️ Macro overlay (fold into Section 8, don't separate)

For every Full report, briefly cover:
- **Market regime:** Risk-on / risk-off. Rate environment expanding or compressing multiples.
- **Sector momentum:** Sector ETF leading, lagging, or middle vs market over 3 months.
- **Rate sensitivity:** This stock's correlation with 10Y yield changes (long-duration tech high, defensive consumer low).
- **FX exposure:** If international revenue >30%, DXY direction.
- **Commodity / input cost:** Specific to the business (oil for airlines, semis for hardware, ad spend for media).

One paragraph total. Don't make this its own section.

---

## 📚 Citation format

Inline footnote or hyperlink:
- `Revenue was $94B in Q1 FY27[^1]` (with `[^1]: [Source](url)` at bottom)
- Or hyperlinked: `Revenue was [$94B](https://www.sec.gov/...) in Q1 FY27`

**Never use `<claim>` tags or other non-standard markup.** They render as garbage text in most environments.

**Direct quotes:** avoid for ordinary analysis (always paraphrase). Use verbatim only when wording is load-bearing: regulatory orders, FDA letters, court rulings, exact 10-K risk-factor phrasing where the legal/clinical wording matters.

**Framework view:** when stating Claude's synthesis (not a cited fact), prefix with **"Framework view:"** so the reader can distinguish.

---

## 📈 Retail Dynamics section (meme/squeeze candidates only)

Trigger: short interest >20% of float, cost-to-borrow >50%, retail-attention spike, or user explicitly framing as squeeze candidate.

Place between Section 7 and Section 8. ~400-600 words.

**Short interest mechanics:**
- Current SI % of float, days to cover, 6-month trend, cost to borrow, utilization rate

**Options market gamma:**
- OI concentration at strikes near current price
- Call/put ratio, IV rank
- Gamma walls — large OI strikes that could trigger reflexive dealer hedging

**Retail sentiment indicators:**
- WSB / X / Stocktwits mention volume + tone (contrarian on extremes)
- Google Trends for ticker
- Robinhood/Webull holder data if findable

**Float dynamics:**
- Free float vs shares outstanding
- Recent issuance or buybacks affecting float
- Lockup expirations if recent IPO

**Squeeze scenario sketch:**
- Dollar volume needed to cover at current price
- Days of average volume needed
- Historical analogues — what squeezed, what didn't, why

**Explicit warning:**
> "Fundamentals can decouple from price in the short term. This name trades on positioning and sentiment as much as on business performance. Prices can move 20%+ on flow alone regardless of business reality."

---

## 🔗 Proxy stocks — naming what actually drives the price

Some stocks aren't priced as operating companies. They're priced as exposure to something else. Standard fundamental analysis is misleading without naming the real driver.

**Detection (don't rely on hardcoded ticker lists — verify per query):**
- Operating business is a small fraction of enterprise value
- Earnings are dominated by mark-to-market on holdings
- Stock's beta to a non-equity asset (Bitcoin, oil, gold) is meaningfully higher than to the broad market
- A single binary catalyst (drug trial, single contract) drives most of the value

**Common patterns to look for** (verify each name's current status — do not assume):
- Bitcoin-treasury companies that hold large BTC balances funded partly by convertible debt — they trade as BTC proxies with structural overhead (corporate costs, share dilution, refi schedule) and amplified beta to BTC. Note: "amplified beta" — not technically leveraged in the futures sense; no daily reset decay.
- Crypto miners — BTC price minus production cost, very high operating leverage to BTC
- Pre-revenue biotechs with a single Phase 3 drug — binary outcome
- SPACs pre-deal — bond-like with optionality
- Holding companies dominated by one portfolio asset
- Highly-shorted names where retail flow dominates fundamentals

**How to write the Underlying Driver section:**
1. **Name the real driver** — what is this REALLY exposure to?
2. **Quantify the relationship** — beta to the underlying, NAV premium/discount, holdings per share
3. **What fundamentals can and can't tell you** — e.g., for a Bitcoin-treasury company, P/E is meaningless; relevant metrics are BTC-per-share, mNAV, convertible note maturity schedule
4. **Re-frame the user's question** — instead of "should I buy [proxy]," the question is "do I want this exposure, and is this the cleanest/cheapest vehicle?" Compare to the underlying (e.g., a spot BTC ETF) and to other vehicles.

Place this section between Snapshot and Business (Section 1.5). 200-400 words.

---

## 🩳 Section 7.7 — Shorting mechanics (short-side mode only)

Place between Section 7 and Section 8. ~400-600 words.

**Borrow availability and cost:**
- Available to borrow on standard brokers?
- Cost to borrow (annualized rate paid to lender)
- Hard-to-borrow flag (rates 50%+, or unavailable entirely)
- During squeezes, CTB can spike to 100-300%

**Days-to-cover risk:**
- DTC = short interest / avg daily volume
- High DTC (>5) amplifies squeeze risk
- Compare current DTC to historical range

**Max-loss profile:**
- Long max loss = 100% (stock → $0)
- **Short max loss = unbounded (stock can rise infinitely)**
- Implication: position sizing must be smaller; stop-loss discipline more critical

**Tax treatment (US):**
- All short-sale gains are short-term regardless of holding period
- Taxed as ordinary income (up to 37% federal)
- Dividends paid to lender = ordinary income, not qualified

**Margin requirements:**
- Initial: 150% of short value
- Maintenance: 30%+ (higher for volatile names)
- Margin calls during squeezes force closure at worst prices

**Squeeze mechanics & catalysts:**
- Positive earnings surprise, takeover bid, ETF inclusion, retail attention spike
- Gamma squeeze (dealer hedging accelerates moves)
- Low-float + high SI = worst-case setups

**Short-specific red flags (against the short):**
- Insider buying spike
- Recent dividend declaration
- Activist disclosure
- Index inclusion (forced buying)
- Buyback program announcement

---

## ⏱️ Time horizon adjustment

If user specified horizon (Step 0i), adjust weighting:

**Short-term (days-weeks):**
- **Be honest:** this skill doesn't have order-book data, options-flow, or real-time technicals. Offer near-term catalyst calendar + recent news flow, but state clearly that day-trade decisions need data this skill doesn't pull.

**Medium-term (months to 1 year):**
- Next 2-4 earnings expectations
- Sector rotation
- Specific catalysts in next 6-12 months
- Current valuation vs near-term earnings

**Long-term (5+ years):**
- Secular trends, TAM
- Moat durability through cycles
- Management capital-allocation track record (5-10 years)
- Industry structure

**Generational (20+ years):**
- All of long-term, plus:
- Regulatory disruption risk over decades
- Tech disruption risk
- Demographic trends affecting end markets
- Track record through multiple cycles (1970s inflation, 2000 crash, 2008 crisis, 2020 COVID)
- Founder control and succession planning

Time horizon tag at top of report: `Analyzing for [short / medium / long / generational] horizon.`
