# DCF Valuation Model: [TICKER]

*Built {DATE} · Evidence Strength: {Strong / Moderate / Limited / Speculative}*

> **What this is:** A discounted-cash-flow model estimating intrinsic value per share based on projected future free cash flows, discounted to present.
>
> **What this is NOT:** A price prediction. A DCF is a **framework for testing what the market is pricing in**, not a target. The fair value range is sensitive to small changes in growth and discount rate — see sensitivity table.
>
> **Every assumption is stated explicitly so you can adjust them.** If an input came from analyst consensus or company guidance, that's cited. If it's an inference where no clean source exists, it's labeled `[ASSUMED]` and stress-tested in the sensitivity table.

---

## Model Setup

### Base assumptions

| Assumption | Value | Source / Rationale |
|---|---|---|
| Current revenue (TTM) | $X B | Latest 10-Q [cite] |
| Current FCF (TTM) | $X B | Latest 10-Q [cite] |
| Current shares outstanding (diluted) | X B | Latest 10-Q [cite] |
| WACC (discount rate) | X% | Risk-free [X%] + equity risk premium [X%] × beta [X] = X%. [show source for each component] |
| Terminal growth rate | X% | GDP-like assumption (2-3% typical) |
| Terminal method | Gordon Growth / Exit Multiple | |
| Net cash (debt) position | $X B | Latest 10-Q [cite] |

**Inputs marked `[ASSUMED]`** (no clean source — values stress-tested below):
- [List each one explicitly. Do not bury assumed inputs as if they were known.]

### Growth assumptions by phase

| Period | Revenue growth | FCF margin | Source / Reasoning |
|---|---|---|---|
| Y1 (next 12 mo) | X% | X% | Analyst consensus / company guidance [cite] |
| Y2-3 | X% | X% | Sector growth + share gain assumption |
| Y4-5 | X% | X% | Maturation phase |
| Y6-10 | X% | X% | Approaching terminal |
| Terminal | X% | X% | Long-term economy growth |

---

## 10-Year FCF Projection

| Year | Revenue ($B) | FCF Margin | FCF ($B) | Discount Factor | PV of FCF ($B) |
|---|---|---|---|---|---|
| 1 | | | | | |
| 2 | | | | | |
| 3 | | | | | |
| 4 | | | | | |
| 5 | | | | | |
| 6 | | | | | |
| 7 | | | | | |
| 8 | | | | | |
| 9 | | | | | |
| 10 | | | | | |
| **Sum PV (Y1-10)** | | | | | **$X B** |

---

## Terminal Value

Gordon Growth:
```
Terminal Value = FCF_Y10 × (1 + g) / (WACC − g)
               = $X × (1 + X%) / (X% − X%)
               = $X B
```

Discounted to present:
```
PV of Terminal = Terminal / (1 + WACC)^10 = $X B
```

---

## Intrinsic Equity Value

| Component | Value ($B) |
|---|---|
| PV of FCF Y1-10 | |
| PV of Terminal Value | |
| + Net Cash (− Net Debt) | |
| **= Equity Value** | |
| ÷ Diluted Shares | |
| **= Fair Value per Share** | **$X** |

---

## Sensitivity Analysis

Fair value per share at different growth × discount rate combinations:

| | WACC 8% | WACC 10% | WACC 12% |
|---|---|---|---|
| **Growth low (−2%)** | $X | $X | $X |
| **Growth base** | $X | **$X** | $X |
| **Growth high (+2%)** | $X | $X | $X |

---

## Comparison to Current Price

- **Current price:** $X
- **Base case fair value:** $X
- **Implied upside / downside:** ±X%

| Scenario | Fair value | vs Current |
|---|---|---|
| Bear (low growth, high discount) | $X | −X% |
| Base case | $X | ±X% |
| Bull (high growth, low discount) | $X | +X% |

---

## Reality Check on Assumptions

The base case requires:

1. **Revenue growth averaging X% over next 10 years.** Credibility:
   - Current TAM and saturation: [...]
   - Historical company growth rate: [...]
   - Competitive landscape: [...]
   - Verdict: **[reasonable / aggressive / requires-belief]**

2. **FCF margin expanding to X% by Y5.** Credibility:
   - Current trajectory: [...]
   - Operating leverage potential: [...]
   - Competitive pressure: [...]
   - Verdict: **[reasonable / aggressive / requires-belief]**

3. **Terminal growth of X%.** Implies the company grows in perpetuity at this rate. Credibility check: is the company's TAM still expanding at terminal? Most should converge to GDP-like (2-3%) — anything higher needs justification.

4. **WACC of X%.** Reasonable for current rate environment and company beta? Re-check if rates shifted recently.

---

## What the market is pricing in (the most useful output)

Working backwards from current price, the **implied long-term FCF growth** is approximately X%. The market is therefore **[more / less / similarly] optimistic** than this base case.

**This is the cleanest valuation question:** is the implied growth achievable? If yes, current price is rational; if no, the market is either wrong or pricing something the model isn't capturing (M&A optionality, regime shift, etc.).

---

## Critical caveats

- DCF models are highly sensitive to small assumption changes. A 1% change in WACC or terminal growth can shift fair value by 15-30%.
- Projections beyond 2-3 years are increasingly speculative.
- DCF ignores near-term sentiment, technical factors, and short-term mispricing.
- This model assumes the business survives 10 years — survival risk not modeled.
- Margin assumptions assume no major industry disruption.

The fair value range here is a **framework output** for pressure-testing the current price, not a target.

---

*Research, not financial advice. Data current as of date stamp; markets move daily. Do your own due diligence and consult a licensed financial advisor before any investment decision.*
