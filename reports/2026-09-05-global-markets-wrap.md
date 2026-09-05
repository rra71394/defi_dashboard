# Global Markets Wrap — September 5, 2026

*Compiled from Bigdata.com (market tearsheet + news search) and Alpha Vantage. Data as of ~05:10-05:13 UTC, September 5, 2026, unless otherwise noted.*

## TL;DR

Today is Saturday, September 5 — US, European, and most Asian equity, rates, futures, and metals markets are closed, so there is no new session to report. The most recent available levels for those asset classes are Friday, September 4's close, which is the same session already covered in yesterday's archived wrap (`reports/2026-09-04-global-markets-wrap.md`): the August nonfarm payrolls beat drove Fed rate-hike odds higher, lifting yields and the dollar while gold, crypto, and gold-miner/crypto-proxy equities sold off. Nothing in that picture has changed since. The one market that trades through the weekend — crypto — is essentially flat over the last 24 hours, with one exception: **Litecoin (LTC), a fund watchlist position, is up 3.65%** on no single dominant catalyst identified in available news. The US-Iran standoff over the Strait of Hormuz remains unresolved and is the key overhang heading into next week (Sunday's OPEC+ meeting, next week's CPI/PPI, and the September 15-16 FOMC).

**Read this as a thin, weekend-shaped update, not a full daily wrap.** There is no "why did markets move today" story for equities/rates/commodities because those markets didn't trade today.

---

## What's actually live: crypto (weekend, 24/7)

*Source: Bigdata.com market tearsheet (sourced from FMP), as of September 5, 2026 05:10 AM UTC. Cross-checked BTC/USD against Alpha Vantage's realtime exchange-rate endpoint, which returned $79,482.09 at 05:12:35 UTC — within 0.04% of Bigdata's $79,514.98, i.e., the two sources agree closely.*

| Asset | Price | 1D change |
|---|---|---|
| Bitcoin (BTC) | $79,514.98 | -0.20% |
| Ethereum (ETH) | $2,448.64 | -0.31% |
| BNB | $722.52 | +0.17% |
| Solana (SOL) | $101.76 | -0.18% |
| XRP | $1.40 | -0.08% |
| Cardano (ADA) | $0.21 | -0.22% |
| Dogecoin (DOGE) | $0.08 | -0.16% |
| Avalanche (AVAX) | $7.41 | +0.26% |
| Chainlink (LINK) | $11.65 | +0.14% |
| **Litecoin (LTC)** | **$52.63** | **+3.65%** |
| Polygon (MATIC, not on watchlist) | $0.28 | +3.51% |

Most majors are within a quarter-point of flat — consistent with a quiet weekend session and with the broader picture from Bigdata.com's news search: coverage through early September describes bitcoin consolidating in the high-$70,000s/low-$80,000s after August's ~25% rally, with the next real catalysts being the September 11 core PCE print, the September 15 CLARITY Act Senate procedural vote, and the September 15-16 FOMC meeting — none of which land this weekend. **I did not find a specific news item explaining Litecoin's and Polygon's outsized weekend moves**; a `bigdata_search` scoped to "weekend of September 5-6" returned only cached results from September 1, suggesting the news index hasn't yet caught up with anything from the last 24 hours. Treat the LTC move as observed-but-unexplained rather than attach a causal story to it.

---

## Geopolitical overhang: US-Iran / Strait of Hormuz (unresolved, ongoing)

*Source: Bigdata.com news search, aggregating CNN, CNBC, Reuters-sourced Alliance News, FXStreet, MT Newswires, The Washington Post, and Ynetnews, various timestamps September 1-5, 2026.*

The freshest item available (Ynetnews, September 5, 2026, 03:09 AM UTC) reports that US intelligence assesses Iran's leadership is "determined to continue" the conflict and may be weighing a broader escalation rather than negotiating; US officials see little sign Tehran will make concessions on the Strait of Hormuz before the US midterm elections. This sits on top of a week of confirmed escalation already reflected in Friday's close: new US strikes on Iranian targets, Iranian missile/drone retaliation against US bases in Kuwait, Jordan, and the UAE, the EU joining the US "Operation Economic Outcast" sanctions campaign, and South Korea weighing a military role protecting Hormuz shipping. WTI closed Friday at $91.48/bbl (+0.20% on the day) and Brent at $96.28/bbl (+0.80%), both still carrying a geopolitical risk premium. No new oil-market data point exists for today since futures markets are also closed over the weekend.

This is a real, live tail risk for the fund's cross-asset book (energy, gold, and the broader risk-sentiment complex all key off it) — flagging it here rather than treating Friday's already-reported numbers as the end of the story.

---

## Friday's close, for reference (already reported — not new)

The levels below are unchanged since Friday and are the same ones covered in depth in `reports/2026-09-04-global-markets-wrap.md`. Repeating only the headline figures here so this report is self-contained; see that file for the full causal narrative (nonfarm payrolls, the FOMC repricing, and the sector/regional breakdown).

*Source: Bigdata.com market tearsheet (FMP), "as of September 4, 2026, 08:00-09:15 PM UTC."*

| | Level | 1D (Friday) |
|---|---|---|
| S&P 500 | 7,718.60 | -0.38% |
| Dow Jones Industrial Avg | 53,414.25 | -0.51% |
| Nasdaq Composite | 26,506.99 | -0.29% |
| VIX | 14.53 | +1.47% |
| 10-Year Treasury yield | 4.78% | +0.21% |
| Gold | $4,476.60/oz | -1.39% |
| Silver | $66.75/oz | -1.41% |
| WTI Crude | $91.48/bbl | +0.20% |

**Data-quality note:** the same tearsheet pull flagged the Wilshire 5000 (^W5000) at -1.03% 1D but a nonsensical -10.00% for both the 5D and 1M columns alongside a +5.01% 1Y figure — internally inconsistent with a -10% move in the last week. This looks like a data artifact from the FMP feed via Bigdata.com rather than a real market move; flagging it rather than reporting it as fact, per the fund's no-fabrication rule.

---

## Portfolio read (`analyst/watchlist.yaml`)

**Equities (33 positions: AAPL, AMD, AMZN, AVGO, BABA, BAC, GOOG, GOOGL, HOOD, INTC, META, MSFT, MU, NFLX, NOK, NVDA, ORCL, PFE, PLTR, TSLA, TSM, SNDK, CHPT, AGCO, NRG, SOXL, MRVL, CEG, KLAC, RIOT, STX, KNX, FOUR, ENTG, VST) and index proxies ($SPX, SPY, QQQ):** no new session since Friday's close — these levels have not moved because US equity markets are closed today. I did not re-pull per-symbol Friday closes for this run (Twelve Data's `get_price` hit its per-minute rate limit twice — "ran out of API credits for the current minute," 8-credit limit on the connected key, per the plan-tier gap already documented in `analyst/CONNECTORS.md`), and re-stating Friday's already-published numbers as today's read would risk implying a new move that didn't happen. None of these positions has a live level to report as of this run.

**Precious metals context (no direct watchlist metals position, but relevant to the GEXC/options book via gold-miner-sensitive names):** unchanged from Friday's close above.

**Crypto (15 positions: BTC, ETH, XRP, SOL, DOGE, ZEC, LINK, ADA, XLM, BCH, LTC, HBAR, SUI, AVAX, SHIB):** live levels for 9 of 15 are in the table above via Bigdata.com's tearsheet (BTC, ETH, XRP, SOL, DOGE, LINK, ADA, AVAX, LTC). **ZEC, XLM, BCH, HBAR, SUI, and SHIB could not be retrieved this run** — Twelve Data's `get_price` batch call for those six symbols was rejected by the same per-minute rate limit noted above. None of the other four connectors (Bigdata.com's tearsheet, Alpha Vantage, Blockscout, Quartr) carry those six pairs as quoted spot prices in the calls made this run. **The one meaningful move in the retrievable set is Litecoin, +3.65%** (see above) — every other retrieved crypto position moved less than half a percent.

**No position breached a >3-5% alert threshold today except LTC**, which sits at the fund's crypto alert threshold (5% for the CRYPTO bot universe) — it did not clear that bar (+3.65% < 5%), so this would not have triggered a `/analyst-watchlist-check` flag, but it's the single largest move across the whole portfolio in this run and worth the CEO's attention given the "no explanatory news found" caveat above.

---

## Risks to watch (carried forward, unresolved)

- **US-Iran / Strait of Hormuz** — actively escalating per the freshest available reporting (September 5, 03:09 UTC); no sign of near-term de-escalation.
- **Sunday's OPEC+ meeting** (September 6) on October output policy — now tomorrow.
- **September 11 core PCE inflation print** and **September 15-16 FOMC meeting** — the next hard catalysts for both rates and crypto.
- **September 15 CLARITY Act Senate procedural vote** — a crypto-market-relevant regulatory catalyst flagged in Bigdata.com's news coverage; prediction markets put passage this year at roughly 13% per that coverage, so failure is the priced-in base case.
- Litecoin's unexplained weekend move — worth a scoped follow-up search once the news index catches up, to confirm there isn't a name-specific catalyst the fund should know about before Monday's open.

---

## Connector status this run

All five of the fund's named connectors (Bigdata.com, Twelve Data, Alpha Vantage, Blockscout, Quartr) were reachable and callable in this session. Two hit known, previously documented limits during this run:
- **Twelve Data**: `get_price` was rate-limited twice ("ran out of API credits for the current minute," an 8-credit/minute cap on the connected key) — the equity watchlist and six crypto pairs (ZEC, XLM, BCH, HBAR, SUI, SHIB) could not be re-quoted as a result.
- **Alpha Vantage**: `GOLD_SILVER_SPOT` hit the free-tier's 25-requests/day cap after the BTC cross-check call, so no independent gold/silver cross-check was available this run beyond the Bigdata.com/FMP figure already reported for Friday's close.

No data point in this report was filled in from general knowledge in place of a failed connector call.

---

## Sources

Market levels: [Bigdata.com](https://bigdata.com) market tearsheet (sourced from FMP), pulled September 5, 2026, ~05:10 UTC. Crypto cross-check: Alpha Vantage `CURRENCY_EXCHANGE_RATE`, September 5, 2026, 05:12:35 UTC. News and geopolitical context: Bigdata.com news search, aggregating CNN, CNBC, Reuters/Alliance News, FXStreet, MT Newswires, The Washington Post, Ynetnews, Benzinga, Yahoo! Finance, Bitcoin.com, and others, various timestamps September 1-5, 2026. Prior-session detail: `reports/2026-09-04-global-markets-wrap.md`.
