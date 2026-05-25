# Changelog

All notable changes to Fathom for Claude.

The format follows [Keep a Changelog](https://keepachangelog.com/en/1.1.0/).

---

## [1.0.0] — Initial public release

First public release after five rounds of adversarial review and live testing on diverse cases (megacap, Chinese ADR, distressed, recent IPO).

### Added

- **13 research modes:** Snapshot, Quick, Full, Compare, Basket, Position, DCF, Scenario, Single-side, Short-side, Cross-asset, Claim-eval, plus auxiliary modes (Risk-focus, ESG, Compress, Drill-down)
- **Sector-specific frameworks** for banks, REITs, biotech, insurance, oil & gas, midstream, dividend-focused, Chinese VIE, SOE, distressed, SPAC, ESG, and ETF sub-categorization
- **Mandatory Evidence Strength floors** that auto-cap analysis credibility for binary-outcome stocks, distressed names, VIE structures, customer-concentrated companies, recent IPOs, OTC listings, and thinly-covered names
- **VIE-suspicion check** with two-path confirmation (search-snippet or full 20-F WebFetch)
- **Gap-fill loop** that scans drafts for data gaps and runs targeted searches to close them before shipping
- **Anti-bias detection** that flags directional lean in prompts and leans against, not with
- **Snapshot triage** that aborts Snapshot mode and kicks to Quick/Full when distress, concentration, or VIE signals appear

### Design rules (hard-coded, non-negotiable)

- No price predictions
- Never fabricate data
- Refuse on claimed MNPI
- Sector-aware analysis
- VIE warning mandatory for Chinese ADRs
- Distressed framework for distressed stocks
- Surface conflicts between sources
- Single disclaimer at bottom
- Refuse stale analysis if WebSearch is unavailable

### Built for

- Claude Code (uses native `WebSearch`, `WebFetch`, inline hyperlink citations)

---

## Future / roadmap

- Additional sector frameworks (defense/aerospace, infrastructure, specialty REITs, maritime, reinsurance, tobacco/spirits)
- More mandatory floor coverage (product-sunset binary outcomes, credible short-seller reports, reverse mergers)
- Real-world test case library
- Optional integration with structured financial data providers (when MCP servers become available)
