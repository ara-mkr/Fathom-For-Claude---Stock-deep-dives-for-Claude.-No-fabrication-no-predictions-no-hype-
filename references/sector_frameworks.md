# Sector-Specific Frameworks

Standard equity analysis (P/E, EV/EBITDA, FCF) produces **misleading results** for certain sectors. Always check sector first; use the right framework.

**Detection over hardcoded lists.** Sector membership shifts and tickers come and go. Each section describes how to detect the relevant framework via the company's GICS sector, balance-sheet structure, or business model — not by a fixed ticker list. Example names below are illustrative, not authoritative.

---

## 🏦 BANKS & Diversified Financials

**Detect when:** GICS sector = Financials; sub-industry = Diversified Banks, Regional Banks, Investment Banking & Brokerage, or Asset Management.

### Why standard framework fails
- Banks borrow at one rate and lend at another. "Revenue" and "cost of goods" don't really apply.
- Net income includes provisions for future loan losses that may or may not materialize.
- 10-15x leverage means small NIM changes drive huge ROE swings.
- P/E ignores book value — the actual asset base.

### Use these metrics

| Metric | What it measures | Healthy range |
|---|---|---|
| **P/B** | Market vs net assets | 1.0-1.5 normal, >2.0 premium, <1.0 distressed |
| **P/TBV** | Same, stripping goodwill | Most relevant for value investors |
| **ROE** | Profitability on equity | 10%+ healthy, 15%+ excellent |
| **ROTCE** | ROE adjusted for goodwill | Best apples-to-apples bank comparison |
| **NIM** | Loan yield minus deposit cost | 2.5-3.5% typical; trend matters more than level |
| **Efficiency ratio** | OpEx / revenue | <60% good, >70% weak |
| **CET1** | Regulatory capital cushion | 4.5% minimum; banks target 11-13% |
| **Loan-loss reserves / loans** | Cushion for future credit losses | Watch trend, not absolute |
| **NPL ratio** | Loans 90+ days past due | <1% excellent, >2% concerning |
| **Net charge-offs / avg loans** | Realized losses | Compare to reserves |

### Bank-specific red flags
- Loan-loss reserves declining while loan growth is high (under-reserving)
- CRE concentration >25% in current environment
- CET1 declining toward regulatory minimum
- Held-to-maturity securities marked above market (this is the SVB pattern)
- Uninsured deposit concentration
- Loan growth significantly above industry (usually means lower credit standards)
- Net charge-offs rising while reserves flat (losses outpacing cushion)

### Valuation section content
- P/B vs sector median + own 5-year average
- ROE × P/B implied (rough fair value)
- Sensitivity to interest rates (10Y yield correlation)

---

## 🏢 REITs

**Detect when:** GICS sector = Real Estate, or company elects REIT tax status (90% of taxable income distributed).

### Why standard framework fails
- Buildings depreciate massively on the income statement even when they appreciate in value → P/E meaningless
- REITs trade on yield, not earnings multiples
- Standard FCF doesn't separate maintenance from growth capex

### Use these metrics

| Metric | What it measures | How to read |
|---|---|---|
| **FFO** | Net income + depreciation − gains on sales | The REIT version of earnings |
| **FFO per share** | FFO / share count | Compare to dividend |
| **AFFO** | FFO − recurring maintenance capex | Most accurate cash flow |
| **P/FFO** | Price / FFO per share | REIT version of P/E. 15-20x typical. |
| **AFFO yield** | AFFO per share / price | Compare to bond yields |
| **Dividend coverage** | AFFO / dividend per share | >1.0 sustainable, >1.2 healthy |
| **Same-store NOI growth** | YoY on properties held >1 year | Best organic growth measure |
| **Occupancy** | % leased | 92%+ industrial/multifamily, 85%+ office (current environment) |
| **WALT** | Weighted avg lease term | Longer = more income visibility |
| **Debt / Total Assets** | REIT leverage | 30-45% typical |
| **Debt maturity ladder** | When debt comes due | Avoid clustering in rate-up periods |
| **Implied cap rate** | NOI / property market value | Compare to interest rates |

### REIT-specific red flags
- AFFO declining while dividend flat (coverage eroding)
- Office REIT in current environment (sector-wide concern)
- Floating-rate debt + maturity wall in next 12-24 months
- Tenant concentration — top 10 >40% of revenue
- Same-store NOI declining (even with stable occupancy)
- mREITs: book value per share declining (rate sensitivity)

### Valuation section content
- P/FFO vs similar REIT types (don't compare residential to industrial)
- AFFO yield vs 10Y Treasury (spread = relative value)
- NAV estimate vs market price
- Implied cap rate vs private-market transactions

---

## 🧬 BIOTECH / Pharma Pipeline Companies

**Detect when:** Pre-revenue or revenue dominated by 1-2 drugs; pipeline value drives most of market cap; binary trial outcomes loom.

### Why standard framework fails
- Many biotechs have zero revenue and burn cash for years
- A single Phase 3 readout can wipe 60-80% of value overnight
- Pipeline value isn't on the balance sheet
- P/E is undefined; EV/Sales doesn't capture drug economics

### Framework

**1. Pipeline table:**

| Drug | Phase | Indication | Readout date | Peak sales est. | Probability of approval |
|---|---|---|---|---|---|

Base-rate approval probabilities by phase:
- Phase 1: ~10%
- Phase 2: ~30%
- Phase 3: ~60%
- NDA/BLA filed: ~80%

(Adjust for indication — oncology lower, infectious disease higher.)

**2. Cash runway (critical for pre-revenue):**
- Current cash position
- Quarterly burn rate
- Months of runway at current burn
- Most recent dilution (secondary, ATM offering)
- If runway <12 months, dilution is essentially guaranteed → model it in.

**3. Risk-adjusted NPV per drug:**
Peak sales × probability of approval × patent life × margin = approximate per-drug value. Sum across pipeline. Compare to market cap. If market cap >> sum, market is pricing optimistic probabilities.

**4. Biotech red flags:**
- Single-drug company facing Phase 3 readout (binary)
- Trial design departing from FDA guidance
- Generic / biosimilar exposure for top sellers (patent cliff)
- PBM pricing pressure
- Recent FDA Form 483 observations or warning letters
- Insider selling clustered before readouts

**5. Catalysts to watch:**
- FDA PDUFA dates
- Trial readout dates (often guided to specific quarters)
- Investor R&D days
- Conference presentations (ASCO, ASH, AHA, JPMHC)

### Valuation section content
- Sum-of-parts: cash + risk-adjusted pipeline value + commercial drug value
- Implied probability vs base rates — is market pricing higher or lower probability than the standard table above?
- Sensitivity: if Drug X fails, what's the floor (cash + remaining pipeline)?

---

## 🛡️ INSURANCE

**Detect when:** GICS sub-industry = Insurance (Property & Casualty, Life & Health, Reinsurance).

### Why standard framework fails
- "Revenue" = premiums; profit comes from underwriting AND float investment income
- Float (money held for future claims) is a free or negative-cost source of leverage when underwriting is profitable
- One catastrophic event can erase a year of profits

### Use these metrics

| Metric | What it measures | Healthy |
|---|---|---|
| **Combined ratio** | (Losses + Expenses) / Premiums | <100% = underwriting profit |
| **Loss ratio** | Claims / Premiums | Sub-component of combined |
| **Expense ratio** | OpEx / Premiums | Sub-component |
| **P/B** | Insurance trades on book, like banks | Sector-dependent |
| **ROE** | 10%+ healthy | Varies by subsector |
| **Investment yield** | Yield on float portfolio | Rising rates = bullish |
| **Float growth** | YoY float growth | Indicates underwriting volume + retention |
| **Reserves vs claims** | Adequate? | Under-reserving = death spiral |

### Insurance red flags
- Combined ratio >100% for multiple quarters
- Adverse reserve development (had to add to prior-year reserves)
- Catastrophe-exposed (FL/CA homeowners, hurricane belt)
- Long-duration bond portfolio during rising rates
- Auto insurers: rising loss costs from EV repair complexity

---

## 🛢️ OIL & GAS / E&P

**Detect when:** GICS sub-industry = Oil & Gas Exploration & Production, Integrated Oil & Gas, or Oil & Gas Refining & Marketing. Midstream (pipelines, storage) is a separate sub-framework below.

### Why standard framework fails
- Earnings move with commodity prices, not business quality
- Reserves are the asset base, not buildings
- CapEx is enormous and continuous; standard FCF analysis fails without breakeven analysis

### Use these metrics

| Metric | What it measures |
|---|---|
| **Breakeven oil price** | WTI needed for profitability |
| **Production (boe/d)** | Barrels of oil equivalent per day |
| **Reserve life** | Proven reserves / annual production |
| **Reinvestment rate** | CapEx / OCF |
| **EV/EBITDA** | Better than P/E for cyclical commodity earnings |
| **EV/Reserves** | EV per barrel of reserves |
| **FCF at $X oil** | Sensitivity at different price scenarios |
| **Dividend coverage at $X oil** | At what oil price does the dividend get cut? |

### E&P red flags
- Reserve replacement ratio <100% (running down resource base)
- Breakeven approaching current WTI
- Maturity wall during low oil prices
- Jurisdictions with regulatory risk
- Environmental liability

### Midstream specifics
- Pipeline contracts (fixed fee vs commodity-exposed)
- Distribution coverage ratio
- Throughput volumes

---

## 💰 DIVIDEND-FOCUSED ANALYSIS

**Apply when user asks "is X a good dividend stock?" or signals income focus.**

| Metric | What it measures | Target |
|---|---|---|
| **Yield** | Annual dividend / price | 2-5% typical; >7% = elevated risk |
| **Payout ratio** | Dividends / earnings | <60% sustainable; >80% caution |
| **FCF coverage** | FCF / dividends paid | >1.2x healthy |
| **Dividend growth (5Y CAGR)** | Recent trajectory | Inflation+ is meaningful |
| **Years of consecutive growth** | Aristocrat (25+) / King (50+) | Track record matters |
| **Capital allocation balance** | Div + buybacks vs reinvestment | Excessive dividends = underinvesting |
| **Sustainability through cycles** | Did they cut in 2008? 2020? | Cuts are catastrophic for income investors |

### Dividend red flags
- Yield significantly above peers (cut-risk signal)
- Payout ratio >100% (paying from balance sheet or debt)
- FCF declining while dividend grows
- Sector in secular decline
- Recent dividend cut announcement

---

## 🇨🇳 VIE (Variable Interest Entity) — Chinese ADRs

**Detect when:** Company is incorporated in Cayman Islands / BVI, operates primarily in mainland China, and uses contractual structure (per 20-F Item 4) rather than direct equity ownership of the Chinese operating entity.

This applies to **almost any US-listed mainland-China business**. Verify via the company's most recent 20-F filing; don't rely on a hardcoded ticker list.

### What a VIE is

When you buy a US-listed Chinese stock, you're not buying equity in the Chinese operating company. **Chinese law prohibits foreign equity ownership in many sensitive sectors** (internet, education, media, telecom).

What you actually buy:
1. A Cayman Islands shell (the listed entity)
2. The shell has **contracts** with the Chinese operating company
3. Those contracts entitle the shell to the operating company's economics
4. **Chinese courts have never definitively ruled VIE contracts enforceable**

### Why this is a massive risk
- The CCP could declare VIEs unenforceable → US shareholders get nothing
- CSRC and SEC have both flagged VIE risks (Holding Foreign Companies Accountable Act)
- Multiple Chinese ADRs have been delisted or moved to HK listings
- A Chinese ride-hailing company was forced to delist days after IPO
- The Chinese tutoring sector lost ~90% of value overnight via 2021 policy change

### Mandatory warning text

For any Chinese VIE, include in Section 1.7:

> **⚠️ VIE STRUCTURE WARNING**
>
> [TICKER] uses a Variable Interest Entity (VIE) structure typical for US-listed Chinese companies. **US investors do not own equity in the Chinese operating business.** They own shares of a Cayman Islands shell company with contractual claims to the operating company's economics.
>
> **Specific risks:**
> - VIE contracts have never been definitively upheld in Chinese courts
> - The CCP could declare the structure unenforceable
> - Chinese regulators (CSRC, CAC) can override decisions affecting foreign investors
> - The HFCAA could force delisting if PCAOB audit access is restricted
> - **The biggest variable for these stocks is Chinese policy direction, not business performance.**

This warning is non-negotiable for any Chinese VIE analysis.

---

## 🏛️ STATE-OWNED ENTERPRISES (SOEs)

**Detect when:** A government entity holds >30% of shares, or controls via golden share, or appoints majority of board.

### Why standard framework fails
- Float is tiny (often 1-10% of shares outstanding)
- Dividend policy is political, not economic
- Government as residual controller can override management
- Strategic priorities may conflict with minority shareholder returns

### "State Ownership Dynamics" section content
- Government ownership % (which government entity)
- Float as % of total shares
- Recent dividend history — any cuts driven by government priorities?
- Strategic mandates that affect economics (e.g., a national oil company's role in production-quota policy)
- Geopolitical exposure — sanctions, capital controls, asset seizure
- Minority shareholder rights vs majority owner

---

## 🚀 META-FRAMEWORKS

### Crypto-related stocks (BTC and ETH proxies)

**Detect when:** A meaningful share of enterprise value is balance-sheet crypto holdings (Bitcoin treasury companies, miners with large coin treasuries), OR the company's revenue depends primarily on crypto market activity (exchanges, custodians, mining-as-a-service).

Analyze as exposure vehicles, not operating companies:
- **Holdings per share** (BTC-per-share, ETH-per-share)
- **NAV premium/discount** — current market cap vs holdings value
- **Structural overhead** — corporate operating costs, share issuance, convertible-note maturity schedule
- **Comparison vehicles** — spot crypto ETF (lowest cost, no leverage), direct crypto (no counterparty), futures-based ETF (decay risk)

**Important nuance:** A company funding crypto purchases via convertible debt is **structurally levered in book terms**, but it does NOT have daily-reset decay like a leveraged futures ETF. Its beta to the underlying is amplified by capital structure — typically 1.5-2.5× for the largest Bitcoin-treasury companies — but it's not "leveraged" in the technical futures sense. Don't propagate that myth.

### Political / event-driven proxies

Companies whose price is dominated by political or single-event narratives rather than business fundamentals. Treat as event-driven trading vehicles, not investments. Quantify the fundamentals gap: revenue vs market cap.

### Highly cyclical (semis, housing, autos, advertising)

- Cycle position matters more than current quarter
- Inventory days expanding = late-cycle warning
- Customer end markets matter more than company itself
- Sensitivity to rates, GDP, end-market demand

---

## How to apply this reference

In Step 0f of SKILL.md, after asset class is confirmed as individual stock:

1. **Identify sector** from search results (GICS sector + sub-industry)
2. **If sector matches above** — add the appropriate flag to the report header, use sector framework for valuation, scan for sector-specific red flags, and use sector-appropriate metrics in the snapshot
3. **If multi-sector** (conglomerate, holding company) — sum-of-parts each segment

Standard framework still applies to most general-purpose stocks (tech, consumer, industrial, retail). The sector overrides exist because P/E and EV/EBITDA are wrong for the cases above.

---

## ⚠️ DISTRESSED / TURNAROUND STOCKS

**Detect when:** Any of the following — going-concern language in audit opinion, debt restructuring announced or rumored, Altman Z-score <1.8 (computable from balance sheet: working capital, retained earnings, EBIT, market cap of equity, sales), bankruptcy within 24 months, equity near-wiped.

**Altman Z-score formula** (for non-manufacturers, use Z″ variant; check formula appropriate to sector):
```
Z = 1.2(WC/TA) + 1.4(RE/TA) + 3.3(EBIT/TA) + 0.6(MVE/TL) + 1.0(Sales/TA)
```
Below 1.8 = distressed zone. Compute this explicitly when the flag is in play.

### Why standard framework fails
- P/E meaningless with negative earnings
- Standard FCF misses debt service crisis
- Net income dominated by one-time restructuring charges
- Equity holders may be wiped in bankruptcy regardless of business value

### Solvency assessment

| Metric | Measures | Critical thresholds |
|---|---|---|
| **Altman Z** | BK probability | <1.8 distressed, <1.1 high-BK risk |
| **Distance to default (Merton)** | Volatility-adjusted credit risk | Lower = closer to default |
| **Liquidity runway** | (Cash + credit) / monthly burn | <6 months critical |
| **Debt/EBITDA** | Leverage | >6x stressed for non-utility |
| **Interest coverage** | EBIT / interest | <1.5x can't service from ops |
| **FCF trajectory** | Improving or deteriorating | Inflection > level |
| **Debt maturity wall** | When debt comes due | Concentration = refi risk |

### Going-concern check
In latest 10-K/10-Q, look for:
- "Substantial doubt about ability to continue as a going concern"
- "Material adverse effect on liquidity"
- "Inability to refinance"
- Auditor's going-concern opinion

These are explicit warnings.

### Recovery value if bankruptcy likely
1. Secured creditors: 70-90%
2. Unsecured / bondholders: 20-50%
3. Preferred equity: 0-20%
4. **Common equity: usually $0**

If BK filing is likely, common equity is usually wiped. The trade isn't "is the business good" — it's "will the equity get anything in the restructuring."

### Turnaround signals (real vs dying)
- FCF inflection (negative → positive)
- Debt paydown from operations (not refi)
- Margin expansion 2+ consecutive quarters
- Same-store sales / volume growth resuming
- Operating leverage kicking in
- Activist investor or credible new management
- Asset sales reducing leverage

### Distressed-specific red flags
- Stock <$5 + declining revenue + rising debt = often terminal
- Multiple secondary offerings in 12 months (dilution death spiral)
- CFO or audit firm departures
- Litigation reserves growing
- Customer/supplier credit terms tightening
- 8-K filings about lender amendments

### Verdict framing — distressed stocks have BINARY outcomes

> **Probability-weighted outcomes:**
> - **Turnaround succeeds (~30-40%):** Stock could multi-bag
> - **Muddles through (~30-40%):** Range-bound, gradual dilution
> - **Bankruptcy / restructuring (~20-30%):** Common equity likely $0
>
> Expected value is asymmetric. Most distressed plays are speculation. Position sizing must reflect that capital can go to zero.

Always use **Speculative** Evidence Strength for distressed names regardless of how clean the thesis looks (mandatory floor — see SKILL.md).

---

## 🚀 SPAC FRAMEWORK

**Pre-deal SPAC** (still searching for target): trust holding ~$10/share in T-bills with optionality on future merger.

Key metrics:
- Trust value per share (~$10 at IPO)
- Current price vs trust value (premium = market expects good deal)
- Sponsor track record (prior SPACs' performance)
- Time remaining to find target (typically 18-24 months)
- Redemption rights (shareholders can redeem at trust before merger)
- Warrant structure (separate warrants trade with upside optionality)

Pre-deal SPAC = bond-like instrument with optionality. Downside limited by redemption right. Upside depends on deal quality.

**De-SPAC announcement** (deal pending):
- Redemption rate at announcement
- PIPE participation: who, at what price?
- Projections in proxy (SPACs lost some forward-looking safe-harbor protections; treat projections skeptically)
- Lockup periods for sponsor and PIPE
- Trust dilution from sponsor promote (typically 20%)

**Post-merger** (de-SPAC complete): regular stock, but with these flags:
- Lockup expirations (major price events)
- Cash burn (de-SPACs often go negative quickly)
- Forecast vs reality (compare actual to proxy projections)
- Sponsor exits (immediate selling = bad signal)

### SPAC red flags
- Sponsor with poor de-SPAC track record
- Heavy redemptions at announcement
- Aggressive forward projections (10x revenue in 5 years)
- Hot-cycle industry exposure
- Cash burn exceeding remaining trust

---

## 🌱 ESG ANALYSIS FRAMEWORK

For ESG-focus mode or when user asks E / S / G specifically.

### Environmental (E)
- Scope 1, 2, 3 emissions
- Net-zero commitments (interim target, or just "2050"?)
- Water usage and intensity
- Waste / circular economy
- Regulatory exposure: carbon tax, EU CBAM, mandatory disclosure
- Climate transition risk (stranded assets for fossil fuel cos)

### Social (S)
- Labor: union rate, turnover, wage transparency
- Supply chain: third-party audits, forced-labor exposure (UFLPA)
- Workforce diversity
- Customer privacy and data security incidents
- Community: tax contribution, local employment

### Governance (G)
- Board independence (% independent)
- Board diversity
- CEO/Chairman separation
- Executive comp structure (long-term vs short-term, performance metrics)
- Shareholder rights (one-share-one-vote vs dual-class)
- Related-party transactions
- Audit firm tenure
- Insider ownership and activity

### ESG rating sources (show the disagreement)
- MSCI ESG Ratings — most widely used
- Sustainalytics — risk-rating focus
- S&P ESG — used in S&P 500 ESG Index inclusion
- Refinitiv — academic / institutional

**Critical:** ESG ratings are NOT standardized. Same company can rate AAA at MSCI and "high risk" at Sustainalytics. Always show the disagreement; don't pick a single rating.

### ESG-specific red flags
- Recent controversies (spills, labor scandals, data breaches)
- Disclosure gaps vs sector peers
- Greenwashing accusations
- ESG fund exclusions
- Climate-related liability lawsuits

---

## 📊 ETF SUB-CATEGORIZATION

Identify the sub-type first. Different sub-types need different analysis.

### Index ETFs
- Expense ratio (compounds over time)
- Tracking error vs benchmark
- Liquidity (bid-ask spread)
- AUM (larger = more liquidity, less closure risk)

### Dividend ETFs
- Current and forward yield
- Yield growth (5Y CAGR of distributions)
- Quality screen — what filter?
- Sector concentration
- Qualified vs ordinary dividend mix

### Growth ETFs
- Sector concentration (often tech-heavy)
- P/E of holdings vs market
- Top 10 concentration
- Performance momentum

### Sector ETFs
- Pure sector or value-tilt?
- Top 5 holdings — often 30-50% concentrated
- Sub-industry weights
- When does this sector historically outperform?

### Thematic ETFs
- Theme integrity — does it actually deliver the theme?
- Expense ratio (themes often 0.50-0.75%)
- AUM (small thematic ETFs can close)
- Holdings concentration

### Bond ETFs
- Duration (rate sensitivity)
- Credit quality (IG vs HY)
- Yield to maturity
- Currency exposure (international)

### Commodity ETFs
- Structure: physical vs futures-based
- **Contango/backwardation risk** for futures-based — these lose to contango over time
- Expense ratio
- Tax treatment (some commodity ETFs taxed as collectibles)

### Inverse / Leveraged ETFs

**MANDATORY WARNING:**
> "Leveraged and inverse ETFs are designed for daily trading. The daily reset causes returns to diverge significantly from N× the underlying when held longer than days, due to volatility decay. Holding these long-term often produces losses even when the underlying moves favorably."

Surface this warning prominently — top of report, not buried.
