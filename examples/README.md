# Example outputs

Real outputs from real test runs of Fathom. Use these to see what the skill actually produces, not just what the README claims.

Each file follows the naming convention `[ticker]-[mode].md` so you can scan for the case closest to what you want to try.

## Current examples

| File | What it tests | Notable behaviors |
|---|---|---|
| [`baba-full-deep-dive.md`](baba-full-deep-dive.md) | Full mode on a Chinese ADR | VIE detection fires; mandatory warning block at top; Evidence Strength auto-capped at Moderate; source-variance handling on market cap ($300-338B reported across aggregators) |

## Test cases the skill has run that aren't yet in this folder

- **MSFT** — megacap baseline, Evidence Strength: Strong, no special-case sections needed
- **BYND** — distressed test, Speculative floor fired (Altman Z = −3.52, debt restructuring, negative book value)
- **CRWV** — recent IPO + 67% customer concentration in Microsoft, Speculative floor via new sub-clause

Open a PR if you'd like to add your own test output here. See [CONTRIBUTING.md](../CONTRIBUTING.md) for the format.
