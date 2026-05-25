# Data Sources — Priority Order

Where to look for each type of data. **Primary sources beat secondary every time.** Never rely on a summary when the source is one click away.

---

## Source authority hierarchy (always apply in this order)

1. **SEC filings** (EDGAR) — the legal record. Numbers here are final.
2. **Company IR site** — press releases and decks. Same numbers as filings, more accessible.
3. **Earnings call transcripts** — Motley Fool, Seeking Alpha, Benzinga, company IR. Useful for qualitative tone and management Q&A. Verify any number against the actual filing.
4. **Aggregators** — Yahoo Finance, Stockanalysis.com, Finviz, Macrotrends. Fast and convenient. Treat as derived; verify if pivotal to thesis.
5. **News wires** — Reuters, Bloomberg, WSJ for corporate events.
6. **Retail platforms** — Reddit, X, Stocktwits. Sentiment signal only, not facts. Treat extreme bullishness as contrarian.

If sources conflict: primary wins. Show the conflict — don't smooth it over.

---

## Primary: SEC filings

| Filing | What it is | When to use |
|---|---|---|
| **10-K** | Annual report | Risk Factors (Item 1A), MD&A (Item 7), full financials. Most material info lives here. |
| **10-Q** | Quarterly | Lighter than 10-K but with current-quarter detail. Often more useful than the 10-K because it's fresher. |
| **8-K** | Material events | Acquisitions, leadership changes, guidance updates, breach disclosures |
| **DEF 14A** | Proxy statement | Executive comp, board details, related-party transactions, shareholder proposals |
| **Form 4** | Insider transactions | Filed within 2 business days of trade |
| **13F** | Institutional holdings | Filed quarterly with 45-day lag |
| **13D / 13G** | >5% stakes | Activist (13D) or passive (13G) large positions |
| **S-1 / F-1** | IPO prospectus | Pre-IPO research |
| **20-F** | Foreign private issuer annual | Same purpose as 10-K for foreign companies, including most Chinese ADRs |

---

## Aggregators (fast lookups when filings are overkill)

**Free:**
- Yahoo Finance — `finance.yahoo.com/quote/[TICKER]` — basics, key stats, analyst ratings, holders
- Stockanalysis.com — clean financial statements
- Finviz.com — visual screening, insider trades, news
- Macrotrends.net — 10+ year charts
- Simply Wall St — visual snapshot

**Paywalled (try free article allotment):**
- Seeking Alpha, Bloomberg, FactSet, Refinitiv

---

## Specific data → best source

| Data needed | Best source |
|---|---|
| Latest filings | SEC EDGAR |
| 10-K full text | SEC EDGAR or company IR |
| Earnings call transcript | Motley Fool, Seeking Alpha, company IR |
| Insider trades | SEC Form 4, openinsider.com, finviz |
| Institutional holders | SEC 13F, fintel.io, whalewisdom.com |
| Short interest | nasdaq.com short-interest data, marketbeat.com |
| Analyst PTs | Yahoo Finance, MarketBeat, TipRanks |
| Options activity | Barchart unusual activity, marketchameleon |
| Comparable companies | Stockanalysis.com, Finviz screener |
| Industry data | IBISWorld, Statista, trade associations |
| Macro data | FRED (St. Louis Fed), BEA, BLS, Census |
| Regulatory news | Agency websites, Reuters, Bloomberg |
| Geopolitical exposure | Company 10-K Item 1A, recent news |
| Patents | Google Patents, USPTO |
| Litigation | PACER (paid), Reuters Legal, news |
| Employee sentiment | Glassdoor, layoffs.fyi |
| Customer reviews | G2, Trustpilot, App Store, Amazon |
| Retail sentiment | r/stocks, r/investing, r/wallstreetbets (contrarian) |

---

## Search query patterns that work

Use the **current year** (from system context) — never the model's training-data year.

**Earnings:**
- `[TICKER] Q[N] [YEAR] earnings results`
- `[COMPANY] earnings call transcript Q[N] [YEAR]`
- `[COMPANY] earnings surprise revenue beat`

**Financials:**
- `[COMPANY] revenue breakdown segment [YEAR]`
- `[COMPANY] 10-K [YEAR] risk factors`
- `[COMPANY] gross margin trend`

**Sentiment:**
- `[TICKER] short interest [current month/year]`
- `[COMPANY] insider trading recent`
- `[TICKER] 13F holders [current quarter]`
- `[TICKER] analyst upgrade downgrade [current month/year]`

**Macro / sector:**
- `[SECTOR] outlook [current year]`
- `[COMPANY] [country] revenue exposure`
- `[INDUSTRY] regulation [current year]`

**Catalysts:**
- `[COMPANY] news last 30 days`
- `[COMPANY] guidance update`
- `[COMPANY] activist investor`

**Risks:**
- `[COMPANY] lawsuit investigation`
- `[COMPANY] competitor [name] vs`
- `[COMPANY] customer concentration`

---

## Fetching long documents in Claude Code

Use **`WebFetch`** with a **focused prompt** rather than dumping the whole document. The prompt extracts only what you need.

**Risk Factors from a 10-K:**
```
WebFetch(
  url="<10-K filing URL>",
  prompt="Extract Item 1A Risk Factors only. For each distinct risk, give a one-line summary and quote the most material sentence."
)
```

**MD&A from a 10-K:**
```
WebFetch(
  url="<10-K filing URL>",
  prompt="Extract Item 7 (MD&A). Summarize: revenue drivers, margin commentary, cash-flow narrative, and any forward-looking statements."
)
```

**Earnings call transcript Q&A:**
```
WebFetch(
  url="<transcript URL>",
  prompt="Extract the Q&A section. List each analyst question with management's response. Note any deflections, evasions, or unusually direct statements."
)
```

This approach avoids blowing context on 200-page filings.

---

## EDGAR fallback chain

EDGAR direct URLs sometimes return minimal content (JavaScript-heavy pages). Fall through this chain in order:

**Level 1 — EDGAR full-text search (most reliable):**
```
https://efts.sec.gov/LATEST/search-index?q=%22[search-term]%22&forms=10-K&ciks=[CIK]
```
Returns JSON with filing locations. Better than scraping HTML pages.

**Level 2 — EDGAR company filing browser:**
```
https://www.sec.gov/cgi-bin/browse-edgar?action=getcompany&CIK=[TICKER]&type=10-K&dateb=&owner=include&count=40
```
Lists recent 10-K filings.

**Level 3 — Yahoo Finance SEC Filings tab:**
```
https://finance.yahoo.com/quote/[TICKER]/sec-filings
```
Curated list, often cleaner than EDGAR directly.

**Level 4 — Company IR site:**
```
investor.[company-domain].com  OR  ir.[company-domain].com
```
Often the cleanest path, especially for foreign issuers.

**Level 5 — Google scoped to SEC.gov:**
```
WebSearch: "site:sec.gov [COMPANY] 10-K [year]"
```
When all else fails. Search snippets often contain the specific section.

---

## Earnings transcript sources (priority)

1. **Motley Fool** — fool.com/earnings/call-transcripts — usually fastest, free
2. **Seeking Alpha** — paywall after a few articles
3. **Benzinga** — increasing coverage
4. **The Globe and Mail** — free transcripts for US stocks
5. **Company IR site** — sometimes uploads them directly

Full transcripts are 15-30k tokens. Use `WebFetch` with a focused prompt rather than fetching whole.

---

## When sources disagree

Common and expected. Apply rules in order:

1. **Primary wins** — SEC filing beats analyst report beats news article
2. **Recent wins** — newer earnings supersedes older
3. **Explicit wins** — "Q3 2025 revenue was $4.218B" beats "Q3 revenue was around $4B"
4. **Aggregator-vs-aggregator tie-breaker** (when no primary source available):
   - Prefer the source closest to the current date stamp (Yahoo Finance > a 2-week-old Morningstar quote)
   - If both equally fresh, prefer the source that shows methodology (Stockanalysis.com explains share-count convention; raw quote sites don't)
   - For market cap specifically: the most common conflict is ADS-equivalents vs ordinary-share counts for foreign issuers. State the discrepancy and explain it (e.g., "Sources vary $300-338B; variance reflects ordinary-share-count vs ADS-equivalent assumptions")
5. **Still conflicting** — show all, cite all, explain *why* they differ rather than picking one silently

---

## What to ignore (don't burn search budget)

- Stock-prediction sites promising returns
- Penny-stock promotion newsletters
- "AI score 0-100" sites without methodology
- YouTube hot-stock thumbnails without earnings analysis
- Sponsored content disguised as research

---

## When data isn't available

Flag the limitation prominently and proceed with what you have:

- **Pre-IPO** — only S-1 data, founder history, recent funding
- **SPAC** — focus on de-SPAC announcement, sponsor track record, redemptions
- **OTC / pink sheet** — extra skepticism, flag liquidity and disclosure gaps
- **Foreign / ADR** — pull home-country filings if US coverage is sparse
- **Recently public (<2 years)** — limited history, comparison harder

Add a note: "Data coverage is limited because [reason]. Evidence Strength adjusted accordingly."

---

## 🌍 Non-US data sources by exchange

For stocks without US ADRs, US sources have minimal coverage. Use the local primary regulator/exchange.

| Exchange / Country | Primary source |
|---|---|
| Tokyo (TSE) — Japan | **EDINET** at disclosure.edinet-fsa.go.jp (English versions often on company IR) |
| London (LSE) — UK | **RNS** via londonstockexchange.com/news; Companies House for entity data |
| Hong Kong (HKEX) | **HKEX news** at www1.hkexnews.hk (most large issuers file in English) |
| Shanghai / Shenzhen — China | **CNINFO** at cninfo.com.cn (Chinese); use HK/US dual-listing if available |
| Saudi Arabia (Tadawul) | **tadawul.com.sa** announcements (English usually available) |
| Singapore (SGX) | **sgx.com** Company Announcements (English) |
| Australia (ASX) | **asx.com.au** Announcements (English) |
| Toronto (TSX) — Canada | **SEDAR+** at sedarplus.ca |
| Frankfurt — Germany | **bundesanzeiger.de** + company IR sites |
| Euronext (Paris, Amsterdam, Brussels) | AMF / FSMA filings, company IR |
| Mumbai (NSE/BSE) — India | NSE / BSE Corporate Filings + SEBI |
| São Paulo (B3) — Brazil | B3 company filings + CVM |
| Mexico (BMV) | Emisnet system (Spanish) |

Also useful for foreign coverage:
- **Bloomberg / Reuters** news (often the only English coverage of smaller foreign names)
- **Financial Times** and **Nikkei Asia** for Asia-Pacific
- **Bloomberg ticker format**: `[TICKER] [country code]` (e.g., 7203 JT for Toyota, 0700 HK for Tencent)

For any foreign stock, add a prominent note: "US disclosure coverage is limited. Data drawn from [exchange] filings and English-language press coverage; some metrics may lag US-listed peers."
