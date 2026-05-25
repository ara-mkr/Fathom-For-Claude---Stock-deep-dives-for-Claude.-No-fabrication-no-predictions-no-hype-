# Contributing to Fathom

Thanks for considering a contribution. Fathom is opinionated by design — it deliberately refuses to do certain things (predict prices, recommend buy/sell, fabricate data). Contributions that strengthen the core design philosophy are welcome. Contributions that erode it will be politely declined.

---

## What's high-leverage to contribute

### New sector frameworks
The current `references/sector_frameworks.md` covers banks, REITs, biotech, insurance, oil & gas, VIE, SPAC, distressed, ESG, and ETFs. Genuinely useful additions:

- **Defense / aerospace** — backlog dynamics, government contract cycles, program risk
- **Infrastructure / utilities** — rate base, allowed ROE, regulatory lag
- **Specialty REITs** — data centers (different from industrial), self-storage (different from residential)
- **Maritime shipping** — day rates, fleet age, IMO regulation
- **Reinsurance** — combined ratio dynamics differ from primary insurance
- **Tobacco / spirits** — pricing power vs volume decline frameworks

For each new framework, follow the existing pattern:
1. *Detect when:* clear principle-based detection (not hardcoded tickers)
2. *Why standard framework fails:* explain why P/E or EV/EBITDA is misleading
3. *Use these metrics instead:* table of sector-specific metrics with healthy ranges
4. *Sector-specific red flags*
5. *What to put in the valuation section*

### Additional mandatory Evidence Strength floors
The current list (in `SKILL.md` under "Mandatory Evidence Strength floors") covers distress, binary outcomes, data trust, and data coverage. If you can identify a binary-outcome pattern the list misses, that's high-value. Examples worth considering:

- Companies where >50% of revenue comes from a single product version facing a known sunset (drug going generic, single-platform tech)
- Stocks with active short reports from credible short-sellers (Muddy Waters, Citron, Hindenburg) that haven't been refuted
- Recent material reverse mergers (different from SPACs)

### Real test cases
The skill was tested against megacap (MSFT), Chinese ADR (BABA), distressed (BYND), and recent IPO (CRWV). More test diversity is valuable:

- A foreign issuer without an ADR
- A specialty REIT
- A pre-revenue biotech with a near-term Phase 3 readout
- An SOE (state-owned enterprise)
- A meme/squeeze candidate

For each test case, document: which flags fired, which Evidence Strength label landed, what the skill got right, and what it got wrong.

### Bug reports from live use
The single most valuable contribution: run the skill on a stock you actually research and report what it did well and badly. Open an issue with the prompt, the output, and your professional opinion of where it went wrong.

---

## What probably won't be merged

- **Anything that adds price predictions** — this is a core design rule, not a missing feature
- **Anything that adds buy/sell/hold ratings** — same
- **"Confidence scores" that look like ratings** — Evidence Strength is deliberately named to avoid this
- **Removing mandatory floors** — these exist because the underlying risk is uninsurable by analysis
- **Adding tickers to hardcoded lists** — the skill detects by principle, not by list, because lists rot

---

## Style guide

- **No `<claim>` tags or other custom markup** — inline hyperlinks only
- **Inline citations on every quantitative claim** — never present synthesis as cited fact
- **Direct quotes only for load-bearing language** (regulatory text, FDA letters, court rulings)
- **Decisive over hedged** — wishy-washy analysis is worse than nothing
- **Adult-to-adult tone** — not preachy, not condescending
- **No emojis in skill output unless explicitly requested by the user**

---

## How to submit

1. Fork the repo
2. Make your changes
3. Test by running the skill on at least one stock that exercises your change
4. Open a PR with: what you changed, why, and the test case output

For larger contributions (new sector framework, new mandatory floor), open an issue first to discuss the approach.

---

## Code of conduct

Be useful, not clever. Be specific, not vague. Be honest about limits.

The skill is designed around the idea that good research surfaces sharper questions, not more confident answers. Contributions in that spirit are welcome.
