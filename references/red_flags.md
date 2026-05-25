# Red Flags — Dirty Laundry Checklist

Things that should make you stop and dig deeper. Not all are dealbreakers — but all are worth surfacing in the report with severity rating.

## Accounting & financial red flags

### Critical (call out prominently)
- **Going concern language** in audit opinion
- **Auditor change** in last 3 years, especially mid-cycle
- **Earnings restatement** in last 5 years
- **Late filing** of 10-K or 10-Q
- **Negative book value** (liabilities exceed assets)
- **Negative working capital trend** in non-asset-light business
- **Material weakness** in internal controls disclosed in 10-K

### Serious (investigate further)
- Revenue growth significantly outpacing receivables in the wrong direction (channel stuffing)
- Inventory growing faster than revenue 2+ quarters (demand softening)
- DSO climbing (collection problems)
- Goodwill >30% of total assets with no recent impairment (delayed write-down coming)
- Recurring "one-time" charges every quarter (real expense being hidden)
- EBITDA add-backs growing (debt covenant manipulation)
- Stock-based comp >15% of revenue with no buybacks to offset
- FCF / Net Income <70% consistently (low-quality earnings)
- Operating cash flow < net income repeatedly (cash isn't matching reported profits)

### Worth noting
- Capitalized expenses growing faster than revenue (R&D, software dev, CAC)
- Frequent acquisitions with goodwill build-up (rollup risk)
- Heavy use of non-GAAP metrics that exclude items the company calls real costs
- Frequent guidance revisions (visibility problem or sandbagging)

## Governance red flags

### Critical
- CEO + Chairman same person without lead independent director
- Dual-class share structure giving founders >50% control with <50% economics
- Related-party transactions with significant dollar value
- Recent SEC enforcement action
- CFO turnover twice in 3 years
- Board lacks majority independents (NYSE/NASDAQ require it for most listings)

### Serious
- Insider selling cluster — 3+ executives selling significant amounts in same window
- Executive comp rising while stock declining
- Performance metrics in comp plan are easy to hit (low bar = misalignment)
- Departing board members citing disagreements (rare and material)
- No insider buying ever (insiders not putting their own money on the line)

## Business red flags

### Critical
- Single customer >20% of revenue without long-term contract
- Government revenue >30% with administration change pending
- One-product company facing patent expiry
- Operating in country with capital controls
- Pending product recall or safety investigation
- Active class action with credible damages

### Serious
- Customer churn rising (where disclosed)
- Net revenue retention <100% for SaaS
- Competitors taking market share in recent quarters
- Patent cliff within 5 years for pharma
- Cyclical exposure at end of cycle
- Brand damage event in last 24 months
- Key-person dependency (founder-led, no clear succession)

## Capital structure red flags

### Critical
- Debt maturity wall >30% of debt in next 18 months
- Interest coverage <2x
- Debt / EBITDA >5x for non-utility, non-infrastructure
- Recent refi at materially higher rate
- Convertible notes with looming conversion that would massively dilute

### Serious
- Floating-rate debt >50% with rates elevated
- FX-denominated debt mismatched with revenue currency
- Cross-default provisions in credit agreements
- Cash declining quarter-over-quarter without explanation
- Buybacks funded with debt while FCF is negative

## Macro / external

- Sector ETF down 20%+ while target stock flat (overdue catch-down)
- Insider buying ratio in sector below 1-year average
- Yield-curve inversion + cyclical business
- Currency exposure to weakening currencies
- Geopolitical exposure to escalating conflicts

## Penny-stock-specific (only when SEC penny-stock criteria met: price <$5 AND not on a major exchange — both required)

- Reverse split in last 12 months (often precedes more declines)
- Pump-and-dump indicators — sudden volume spikes, paid newsletter mentions
- Constant share issuance to fund operations
- No real revenue with all "potential" / "milestones"
- OTC listing rather than major exchange (lower disclosure standards)
- Recent name change (rebranding to escape history)

(A sub-$5 price on NYSE/NASDAQ during a drawdown is NOT a penny stock by SEC Rule 3a51-1. Don't mislabel quality names trading cheaply.)

## Pre-IPO / SPAC

- Sponsor with poor de-SPAC track record
- Public float <20% post-deal
- Heavy redemptions in trust account
- Aggressive forward projections in proxy
- Founder selling at IPO rather than reinvesting
- Insider lockup expiring soon

## Sector-specific (load with `sector_frameworks.md`)

### Banks
- Loan loss reserves declining while loan growth is high
- CRE concentration in current environment
- Held-to-maturity securities marked above market
- Uninsured deposit concentration

### Biotech / pharma
- Single drug pipeline with binary readouts
- Phase 3 trial design departures from FDA guidance
- Generic / biosimilar exposure
- Pricing pressure from PBMs

### Semiconductors
- Inventory days expanding (cycle peak warning)
- Single-fab concentration in Taiwan
- China revenue at risk from export controls
- Customer concentration in single end market

### Real estate
- Office REIT in current environment
- Floating-rate debt + maturity wall
- Tenant concentration
- Geographic concentration in declining markets

### Retail
- Same-store sales declining
- E-commerce growth slower than category
- Inventory growth outpacing sales
- Mall-based exposure

### Software / SaaS
- NRR <110%
- Customer count growth slowing while revenue holds (price-led growth)
- Rule of 40 declining
- High CAC without LTV proof

## How to surface red flags in the report

Don't bury them. In Section 3 (Financials) and Section 6 (Bear case), explicitly list any red flags found with severity and source.

Format:
> ⚠ **Red flag — [Critical / Serious / Note]:** [What was found]
> Source: [Where]
> Why it matters: [Implication for thesis]
