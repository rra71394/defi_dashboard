# Connector Catalog

What each connector actually covers, mapped to the fund's asset classes (equities, options, futures, crypto, precious metals) and to the three analyst functions (research / briefing / monitoring). Written from direct use in the September 4, 2026 market wrap — gotchas below are things that actually happened, not speculation.

**Tool naming note:** the `mcp__<server>__<tool>` prefix is session-dependent (see `CLAUDE.md` rule 7). This doc refers to tools by their stable suffix only.

## Coverage matrix

| Asset class | Primary connector(s) | Supporting | Known gap |
|---|---|---|---|
| **Equities** | Twelve Data (quotes, technicals, fundamentals), Bigdata.com (tearsheet, news, filings, sentiment) | Quartr (primary-source filings/transcripts), Alpha Vantage (technicals, insider/institutional holdings, congress trades, news sentiment) | Twelve Data's market-movers/screener endpoint needs a paid plan tier (hit this wall directly — see below) |
| **Options** | Alpha Vantage — the *only* connector with options data | — | No other connector has any options coverage at all. No Greeks/IV surface beyond what Alpha Vantage's endpoints return. |
| **Futures** | Alpha Vantage (commodity futures/curves: WTI, Brent, natural gas, broad commodities index), Bigdata.com (tearsheet commodities section) | — | **No connector covers equity-index futures (ES/NQ/YM) or rates futures by name.** What's covered is physical/commodity futures only. Treat this as an open gap, not a covered asset. |
| **Crypto** | Bigdata.com (tearsheet crypto section + news), Twelve Data (spot prices), Alpha Vantage (daily/weekly/monthly digital-currency series, intraday) | Blockscout (on-chain: wallet balances, token transfers, contract inspection — the only connector that verifies actual on-chain state rather than just price) | — |
| **Precious metals** | Alpha Vantage (spot + historical gold/silver, broader commodity futures), Bigdata.com (tearsheet metals section) | — | Platinum/palladium are covered via Bigdata's tearsheet but not as first-class Alpha Vantage endpoints |
| **Macro / rates (context, not a position)** | Alpha Vantage (Treasury yield curve, Fed funds rate, CPI, real GDP, unemployment, nonfarm payrolls, retail sales, durables), Bigdata.com (tearsheet yields section + macro news) | Twelve Data (FX pairs) | — |

---

## Bigdata.com

News, filings, transcripts, research-report search, plus structured tearsheets. The single best "what happened and why" source, and the fastest way to get a cross-asset snapshot in one call.

**Branding requirement (from the connector itself): always write "Bigdata.com" exactly, with a link to https://bigdata.com, whenever you cite it.**

Key tools:
- `bigdata_market_tearsheet` — one call returns a full cross-asset snapshot: global equity ETFs by country, US sectors, major indexes worldwide, fixed income, the full Treasury yield curve, commodities (energy/metals/ag), fiat + crypto currencies, and equity factors, each with 1D/5D/1M/3M/6M/YTD/1Y change. **Start every briefing here.**
- `bigdata_search` — the news/narrative engine. Two modes: `smart` (natural language, resolves entities/dates itself — default) and `fast` (explicit filters, for retries). **Discipline that matters: one topic, one time period, one aspect per call.** A mixed query like "what's driving oil and crypto this week" should be two or three separate calls, not one. Add `"context": "search the open web"` to smart mode to reach open-web results (blogs, regulator sites, anything outside the licensed financial index) instead of just the indexed corpus.
- `bigdata_company_tearsheet`, `bigdata_sentiment_tearsheet`, `bigdata_events_calendar` — all require an `rp_entity_id`. Call `find_securities` first to resolve a ticker/name to one; don't guess IDs.
- `bigdata_etf_tearsheet`, `bigdata_country_tearsheet`, `bigdata_portfolio_tearsheet` — same entity-resolution rule.
- `find_securities` / `get_securities` — entity resolution. `find_securities` for name/ticker/domain lookups (including batch-resolving several tickers — fire them in parallel, one call per ticker); `get_securities` when you already have an exact ISIN/CUSIP/SEDOL.
- `bigdata_fetch_document`, `bigdata_list_documents` — pull a full document (filing, transcript, article) once search has surfaced its ID.
- `bigdata_list_connectors` — enumerates the user's *private* content connectors (email, proprietary research feeds), if any are ever attached to this fund's account. Not the same thing as this catalog.

**Gotchas hit in practice:** none — this was the most reliable connector in the seed session. Its main cost is discipline: violate the one-focus-per-call rule and result quality drops.

## Twelve Data

Real-time and historical quotes, 60+ technical indicators, fundamentals, ETF/fund data, company news, market cap, analyst ratings, and regulatory data (SEC filings, insider transactions, institutional holdings), across stocks, ETFs, forex, and crypto.

**Explicitly not supported (per the connector's own documentation):** market indices directly (S&P 500, Nasdaq Composite, Dow, etc. — use an ETF proxy: SPY, QQQ, DIA, IWM), options, bonds.

Key tools: `get_quote`, `get_price` (single or comma-separated multi-symbol), `get_time_series`, `get_technical_indicator`, `get_market_movers`, `get_market_state`, `search_symbol`.

**Gotcha hit in practice:** `get_market_movers` returned a hard error — *"available exclusively with pro or ultra or venture or enterprise plans"* — on the connected key. Confirm plan tier before building anything that depends on this endpoint (watchlist screening, gainers/losers scans); until upgraded, treat it as unavailable and use Bigdata.com's tearsheet or Alpha Vantage's `TOP_GAINERS_LOSERS` (also gated — see below) as a fallback, or fall back to per-symbol `get_quote` calls against a known list.

**Second gotcha, hit live 2026-09-05:** the free tier caps at **8 API credits/minute**. A single batched `get_price` call across 15 crypto symbols burns 15 credits in one shot and gets rejected outright (*"You have run out of API credits for the current minute"*) — it does not partially succeed. **Fix, in priority order, until the plan is upgraded:**
1. `bigdata_market_tearsheet` already returns "currencies incl. crypto" in its one call (see above) — check there FIRST for majors (BTC, ETH, and whatever else it carries) before ever calling Twelve Data for the same symbol. Don't spend a rate-limited call on a number you already have.
2. For the rest of a crypto watchlist, batch in groups of **≤6 symbols** per `get_price` call, not one giant batch — 15 symbols in groups of 6/6/3 is 3 calls inside the per-minute cap instead of 1 call that fails outright.
3. If still rate-limited mid-run, say so on that position's line (per step 7 of the watchlist-check playbook) rather than retrying in a hot loop — the cap resets on the next wall-clock minute, not on retry.

## Alpha Vantage

The deepest single bench: technical indicators, commodities (WTI, Brent, natural gas, gold/silver spot and history, a broad all-commodities index), Treasury yield curve, Fed funds rate, crypto (daily/weekly/monthly series plus intraday), FX, full fundamentals (income statement, balance sheet, cash flow, earnings, splits, dividends), insider transactions, institutional holdings, **congressional trading disclosures**, news sentiment, top gainers/losers, and — uniquely — **options** (historical and realtime chains, options FMV, put/call ratios, volume/open-interest ratios). Also carries the core US macro releases: CPI, real GDP, unemployment, nonfarm payrolls, retail sales, durable goods.

This is the connector to reach for on **options** (nothing else covers it) and on **macro/rates context** (deepest bench of official series).

**Gotcha hit in practice:** `TOP_GAINERS_LOSERS` returned a rate-limit error — *"not yet entitled to 15-minute delayed US market data... subscribe to any premium plan"* — on the free-tier key. Alpha Vantage's free tier is generally aggressive on rate limits; expect to hit this on other endpoints too under real usage volume (e.g. a watchlist-check loop hitting several symbols per pass). Budget for a paid key before relying on this connector for monitoring.

**Second gotcha, hit live 2026-09-05:** the free key is capped at **25 requests/day, total, across every endpoint** — this is a hard daily ceiling, not a per-minute burst limit, so waiting a minute does not help once it's hit (confirmed: a single gold/silver spot check consumed the day's last credit mid-report). **Fix:** treat Alpha Vantage as **last resort, options and macro-series only** (the two things nothing else here covers) — `bigdata_market_tearsheet`'s one call already carries commodities (incl. metals) and crypto, so check there FIRST for anything Bigdata also covers, and never spend a daily-capped Alpha Vantage credit re-confirming a number the tearsheet already gave you.

## Blockscout

Multi-chain on-chain explorer. This is what turns "crypto" from a price feed into verifiable on-chain fact: wallet balances and holdings, transaction history, token transfers, NFT holdings, contract ABI/source inspection, `read_contract` calls, ENS resolution, block/transaction lookups, and a general `direct_api_call` escape hatch.

Use it to: verify a counterparty or protocol's actual on-chain exposure before relying on a headline number, track a specific wallet (a whale, a protocol treasury, the fund's own custody address if applicable), or audit a DeFi contract before treating a yield/TVL claim as fact.

**Before heavy on-chain work, load the connector's own bundled skill** — it ships operating rules and a curated `direct_api_call` endpoint reference at `blockscout-mcp://skill/SKILL.md` (fetch via MCP resources, or `GET /skill/SKILL.md` over HTTP if only the raw server is reachable). Don't reinvent that reference; read it first.

## Quartr

Primary-source public-company data: filings, earnings-call transcripts, investor decks, events, and standardized financials, each deep-linked to source. Best equities connector for going *below* the headline number into the actual filing or transcript language.

Key tools: `search_companies` first to resolve a `companyId` (never guess one), then `get_company`, `get_financials`, `list_documents`/`search_documents`, `read_document`, `read_transcript`, `list_events`/`get_event`/`get_event_summary`.

Also carries its own portfolio primitives — `create_watchlist`, `add_to_watchlist`, `create_workspace`, `tag_company_to_workspace` — which is a legitimate alternative to the flat-file `analyst/watchlist.yaml` in this repo if the fund would rather the watchlist live inside Quartr itself. See `ARCHITECTURE.md` for the tradeoff.

**Citation rule (from the connector itself):** always cite Quartr data with the exact URL the tool returns, as an inline markdown link on the figure or phrase itself — never present a number as Quartr data without that link.

## GitHub

Not a market-data connector — this is the tooling for maintaining *this repository* (the analyst's own codebase): PRs, CI, issues, branches. Don't route research questions here.

---

## Adding a genuinely different data source (not just working around a rate limit)

Confirmed live 2026-09-05 (debugging a separate Telegram-delivery issue): when this
skill runs as a *scheduled cloud routine*, it executes in a sandboxed environment with
a strict network allowlist — outbound calls only reach Anthropic's own APIs, package
registries, and whichever MCP connectors are explicitly attached to that routine.
A plain `curl` to any other domain (a free public API like CoinGecko, for instance)
is rejected the same way `api.telegram.org` was (`connect_rejected`, org policy) —
this is not Telegram-specific, it's how the sandbox's egress works in general.

**Practical consequence:** a real 6th data source (not a workaround using the 5 above)
has to be a proper MCP connector, added at https://claude.ai/customize/connectors —
the founder's own action, same as connecting the original 5. It is not something a
prompt or playbook change here can add on its own. Interactive (non-scheduled) Claude
Code sessions on the trading_agent droplet do NOT have this restriction — a plain
`requests` call to a free public API works fine there (see the meme-scanner project's
`meme_scanner.py`/`meme_verify.py`, which do exactly this).

## What's not covered by anything

- **Equity-index and rates futures** (ES, NQ, YM, ZN, ZB, etc.) — only physical/commodity futures are covered (Alpha Vantage).
- **A live options Greeks/IV surface beyond what Alpha Vantage's endpoints natively return.**
- **Any execution or order-routing capability, anywhere.** Every connector here is read-only market/research data. That's a feature, not a gap — see `GUARDRAILS.md`.
- **A delivery channel to the CEO** (email, Slack, etc.). Output today lands as a file in this repo plus, optionally, a published dashboard link.
