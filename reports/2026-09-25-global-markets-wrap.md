# Global Markets Wrap — September 25, 2026

*Compiled from Bigdata.com (market tearsheet + news search) and Alpha Vantage (crypto pairs not carried by the tearsheet, a handful of equity quotes, and — after Alpha Vantage's daily quota was exhausted — most of the GEXC book pulled via Bigdata.com's company tearsheet instead). **Twelve Data was not available as a callable tool in this session at all** (it requires an interactive OAuth authorization this non-interactive scheduled run could not complete) — see Connector status for how the portfolio pass was rebuilt around that gap. Cross-asset levels from the Bigdata.com/FMP tearsheet as of ~8:00–9:33 PM UTC, September 25, 2026. **This is a draft for human review, not a trade recommendation** — see `analyst/GUARDRAILS.md`.*

## TL;DR

Markets caught a break from the week's dominant story. Iran's Foreign Minister Abbas Araghchi floated a conditional seven-day proposal to reopen the Strait of Hormuz and resume nuclear talks if Washington accepts its conditions, and oil fell roughly 2% on the relief (WTI −2.33% to $92.41, Brent −2.14% to $104.32, both per Barchart/MT Newswires prints matching the Bigdata.com/FMP tearsheet). That eased some of the inflation pressure that has driven Treasury yields to multi-decade highs all week — the 10-year, which touched a 19-year intraday high near 5.22–5.23% on Thursday, was "little changed" Friday (CNBC.com) while the front end and belly of the curve actually retreated (2-year −1.23% 1D) even as the 30-year pushed to a fresh 22-year high (5.49%, +0.37%). The VIX dropped sharply (−5.11% to 14.87) on the reduced risk premium. US equities closed higher and posted their first weekly gain in a month (S&P 500 +0.51%, Dow +0.93%, Nasdaq +0.48%) — the Dow snapped a three-week losing streak. The gains were led by Microsoft (+3.66%), which unveiled a major Copilot overhaul (a unified "Home" interface plus an always-on "Autopilot" agent) days after a Stifel upgrade to Buy, closing at its highest level since November. That offset a sharp reversal in Meta Platforms (−3.33%), which gave back much of this week's Muse-AI-agent rally after Goldman Sachs warned that AI hyperscalers (naming Meta, Microsoft, Alphabet, Amazon and Oracle) need roughly $300B/year in AI revenue just to break even on capex, and $1 trillion/year to be meaningfully profitable. Separately, the Trump–Xi summit wrapped with a two-month tariff-truce extension (through January 10, 2027) but no breakthroughs on AI export controls, Taiwan, or the Iran war — a "stability, not resolution" backdrop (Washington Post, Politico) rather than a fresh catalyst.

**Note on context:** this is the same rate-hike cycle flagged in every report since September 16 (the Fed's first hike since 2023, with 16 of 18 policymakers projecting at least one more this year). Today's story is a partial, oil-driven *relief* from that cycle's pressure — not a reversal of it. CME FedWatch odds for an October 28 hike ranged 58–75% across sources checked today (see Rates section for why), still elevated.

---

## The trigger: an Iran diplomatic overture cools oil, giving yields (and stocks) some room

*Source: MT Newswires (Global Energy and general), Hindustan Times/Reuters, Nasdaq/Barchart, The Sunday Guardian, CNBC.com, FXStreet News, all September 25, 2026.*

Iranian Foreign Minister Abbas Araghchi said on the sidelines of the UN General Assembly that Tehran is willing to reopen the Strait of Hormuz — a chokepoint for roughly a fifth of global oil flows — within seven days and resume nuclear talks, if Washington accepts its conditions (CNBC, via multiple wires). Reuters reported separately that US and Iranian negotiators in New York are exploring a Qatar-led, phased deal along similar lines. Oil sold off on the news: front-month WTI closed down 2.33% at $92.41 (Nasdaq/Barchart's settlement print, matching the Bigdata.com/FMP tearsheet exactly), Brent fell 2.14% to $104.32. Intraday prints varied by source and hour (WTI ranged roughly $92.09–$95.29 through the day per Barchart, MT Newswires and FXStreet), consistent with a volatile, headline-driven session rather than a clean move — and the relief was partial, not a resolution: Yemen's Houthi group launched fresh drone/missile attacks on Saudi Arabia's Riyadh and Aramco's Yanbu facility the same day (MT Newswires), and a separate Iranian security official vowed no return to Tehran's "pre-war diplomatic approach" until its conditions are met.

The lower oil print helped stabilize a bond market that had been selling off hard all week: Transport Topics/AP reported Brent's slide "helping stabilize Treasury yields near 5.18%... after oil-driven inflation concerns rattled financial markets" — consistent with the tearsheet showing most of the curve outside the very long end down on the day (see Rates). US stocks rose on the combination: the S&P 500 gained 0.3–0.5% depending on the intraday snapshot cited, closing out its first winning week in the last three (AP/Transport Topics).

**The cascade:** Iran's Hormuz overture → oil falls ~2% → inflation-risk premium eases → Treasury yields stabilize/retreat off this week's multi-decade highs (except the long end, which kept climbing on fiscal-supply and AI-capex financing concerns) → VIX drops sharply → equities rally, cushioned further by a distinct company-specific story (Microsoft's Copilot relaunch) that offset a reversal in the week's other big AI-trade name (Meta).

---

## Rates

*Source: Bigdata.com market tearsheet (FMP), as of September 25, 2026; cross-checked against same-day wire prints (CNBC.com, FXStreet, Benzinga, InfoQuanta, PubT/Fidelis Capital notes).*

| Maturity | Yield | 1D change |
|---|---|---|
| 1 Month | 4.04% | +0.75% |
| 2 Month | 4.20% | +0.48% |
| 3 Month | 4.24% | 0.00% |
| 6 Month | 4.33% | −0.23% |
| 1 Year | 4.50% | −0.22% |
| 2 Year | 4.81% | −1.23% |
| 3 Year | 4.94% | −1.00% |
| 5 Year | 4.98% | −0.99% |
| 7 Year | 5.06% | −0.78% |
| 10 Year | 5.17% | −0.19% |
| 20 Year | 5.54% | +0.18% |
| 30 Year | 5.49% | +0.37% |

*("1D change" is the relative change in the yield level per Bigdata.com/FMP, not basis points.)*

The tearsheet's snapshot shows the short end and belly of the curve pulling back modestly on the day (2-year −1.23%) while the long end (20s and 30s) kept climbing — FXStreet reported the 30-year touched its highest level in 22 years intraday. That's consistent with Friday's move being a partial *unwind* of the war-risk premium (which sits more in the front/belly, tied to near-term Fed and inflation expectations) rather than a change in the longer-run fiscal and AI-capex financing-cost story that's been pushing the long end up all month. The 10-year "closed little changed to end a volatile week" (CNBC.com) after touching a 19-year intraday high of 5.223–5.228% on Thursday. CME FedWatch-implied odds of an October 28 hike were reported inconsistently across sources checked today — 58% (FXStreet, early), 64% (CNBC.com, PubT), 71% (FXStreet, later), and 75% (one FXStreet gold piece) — a spread wide enough that it's worth flagging rather than picking one number; December-hike odds were reported at 92% (FXStreet). Mohamed El-Erian (via Benzinga) attributed the broader move to government borrowing and Fed signaling rather than a sudden shock. Separately, Benzinga/Ross Gerber flagged the 30-year mortgage rate at 7.45%, its highest since 2023, up 150bp in six months.

---

## Equities

### US: first weekly gain in a month, on a Microsoft-Meta split within the AI trade

*Source: Bigdata.com market tearsheet (FMP), as of ~8:00–9:05 PM UTC; corroborated by AP/Transport Topics, Straits Times, and The Korea Times same-day wire coverage of the US close.*

| Index | Level | 1D |
|---|---|---|
| S&P 500 | 7,743.41 | +0.51% |
| Dow Jones Industrial Avg | 51,828.62 | +0.93% |
| NASDAQ Composite | 27,068.72 | +0.48% |
| NASDAQ 100 | 30,608.13 | +0.42% |
| Russell 2000 | 2,837.55 | +0.07% |
| CBOE Volatility Index (VIX) | 14.87 | −5.11% |

The VIX's sharp drop reflects the oil-driven relief described above more than any change in the underlying yield story. Microsoft was the Dow's best performer (+3.66%, per multiple wires including Morningstar and Straits Times) after unveiling a broad Copilot overhaul — a unified "Home" workspace, a natural-language "Code" tool, and an always-on "Autopilot" agent — days after Stifel upgraded the stock to Buy (price target $575) on strong Azure growth (Azure crossed $100B in FY2026 revenue, +41% y/y). The stock closed at $516.17, its highest level of 2026 and best close since November, up over 30% from its late-July trough.

That offset a sharp reversal in Meta Platforms (−3.33% to −3.64% depending on the intraday snapshot cited; Bigdata.com's company-tearsheet close showed −3.33% to $751.66). Meta had rallied 36% in September and gained 4.5% Thursday to a fresh 52-week high on enthusiasm for its Muse AI agent, but gave back much of that Friday after Goldman Sachs warned that AI hyperscalers — naming Meta specifically, alongside Microsoft, Alphabet, Amazon and Oracle — need roughly $300B/year in AI-services revenue just to break even on a projected $1.1 trillion of 2027 capital spending, and $1 trillion/year to be meaningfully profitable (Yahoo Finance). The pullback came despite four separate Wall Street price-target hikes (to a $820–$950 range) following Meta's Connect keynote, illustrating profit-taking after a steep run rather than a change in the underlying bull case (TheBull.com.au, AOL.com). Intel, which had rallied as much as 14.3% this week on the same Muse-driven CPU-inference-demand thesis, also reversed (−3.45%, Alpha Vantage `GLOBAL_QUOTE`); no Friday-specific catalyst for Intel's move surfaced in this run's searches, so it is flagged as unconfirmed rather than attributed to the Goldman note, which did not name Intel.

| Sector | ETF | 1D |
|---|---|---|
| Industrials | XLI | +0.94% |
| Technology | XLK | +0.79% |
| Financials | XLF | +0.57% |
| Health Care | XLV | +0.50% |
| Utilities | XLU | +0.43% |
| Consumer Staples | XLP | +0.45% |
| Consumer Discretionary | XLY | +0.22% |
| Materials | XLB | +0.21% |
| Real Estate | XLRE | −0.22% |
| **Communication Services** | **XLC** | **−0.93%** |
| **Energy** | **XLE** | **−0.86%** |

Communication Services lagged on Meta's drag (a mirror image of the past two sessions, when it led). Energy fell in sympathy with the day's oil selloff — a reversal from earlier in the week when the sector led on the Houthi-driven oil spike.

### Rest of world: broadly higher, but treat Korea/China levels with caution — several regional exchanges were closed for holidays

*Source: Bigdata.com market tearsheet (FMP), country-ETF proxies and major-index table; holiday-closure detail from Finanz und Wirtschaft's "FuW Morning Report," September 25, 2026.*

| Country/Index | Ticker | 1D |
|---|---|---|
| Japan (ETF) | EWJ | +2.21% |
| Nikkei 225 (index) | ^N225 | +1.30% |
| South Korea (ETF) | EWY | +2.55% |
| KOSPI (index) | ^KS11 | +0.90% |
| Taiwan (ETF) | EWT | +1.51% |
| TAIEX (index) | ^TWII | −0.28% |
| Hong Kong (ETF) | EWH | −0.93% |
| Hang Seng (index) | ^HSI | −1.30% |
| China (ETF) | MCHI | −0.38% |
| Germany (DAX 40) | ^GDAXI | +0.61% |
| UK (FTSE 100) | ^FTSE | +0.14% |
| France (CAC 40) | ^FCHI | −0.04% |
| Euro Stoxx 50 | ^STOXX50E | +0.72% |

**Data-quality note:** the FuW Morning Report explicitly flagged that "there is no trading on the Seoul stock market, and the exchanges in Shanghai and Shenzhen are also closed" Friday for regional holidays, with thin volume across Asia generally. The tearsheet's KOSPI and China-linked figures above may therefore reflect a stale prior-session level carried forward rather than genuine Friday price action, while EWY and MCHI (US-listed ETFs) continued trading and reflect real Friday flows. As in prior reports, South Korea's EWY and Japan's EWJ also diverge from their own underlying indexes (a timing/composition effect, not a data error) — worth noting again rather than resolving, since this run's searches did not chase down the mechanism.

---

## Commodities

### Energy — Iran's Hormuz overture reverses the week's rally

*Source: Nasdaq/Barchart (settlement prints), MT Newswires, Bigdata.com/FMP tearsheet — all three agree closely.*

| Commodity | Price | 1D |
|---|---|---|
| Crude Oil (WTI) | $92.41 | −2.33% |
| Brent Crude Oil | $104.32 | −2.14% |
| Natural Gas (Henry Hub) | $3.25 | −3.53% |
| Gasoline RBOB | $3.20 | −4.09% |
| Heating Oil | $4.58 | +1.15% |

See The trigger, above, for the full narrative. Both benchmarks are still on track for a third consecutive monthly gain (Nasdaq/Barchart) despite Friday's pullback — this is a one-day relief move within a still-elevated price regime (WTI remains up ~60% YTD per the tearsheet's longer-window columns), not a trend change. IEA on September 11 had projected the largest drop in global oil demand this year on high prices even while raising its global-deficit estimate on war-restricted supply (Nasdaq/Barchart) — a reminder that today's move is sentiment-driven, not a change in the underlying supply picture.

### Metals — gold and silver firm as the dollar and yields pause

| Metal | Price | 1D |
|---|---|---|
| Gold Futures | $4,321.20 | +0.54% |
| Silver Futures | $64.80 | +1.25% |
| Platinum | $1,800.80 | +1.99% |
| Palladium | $1,276.00 | −0.48% |
| Copper | $6.77/lb | −0.35% |

FXStreet reported gold rebounding from a one-week low of $4,244 (Thursday) as the dollar and Treasury yields "take a breather" — still on track for a weekly loss given the hawkish Fed backdrop that dominated most of the week. Silver similarly reclaimed the $65 handle after the week's yield-driven pressure eased.

---

## Crypto

*Source: 9 of 15 watchlist pairs from the Bigdata.com tearsheet (as of ~9:33 PM UTC); 6 pairs (ZEC, XLM, BCH, HBAR, SUI, SHIB) from Alpha Vantage `DIGITAL_CURRENCY_DAILY`, whose UTC-midnight daily-close comparison may not align exactly with the tearsheet's later intraday snapshot.*

| Asset | Price | 1D | Source |
|---|---|---|---|
| Bitcoin (BTC) | $83,762.95 | −0.73% | Bigdata.com tearsheet |
| Ethereum (ETH) | $2,679.85 | −0.28% | Bigdata.com tearsheet |
| XRP | $1.55 | +1.39% | Bigdata.com tearsheet |
| **Solana (SOL)** | **$121.02** | **+3.43%** | Bigdata.com tearsheet |
| Dogecoin (DOGE) | $0.10 | +1.91% | Bigdata.com tearsheet |
| Cardano (ADA) | $0.25 | +2.23% | Bigdata.com tearsheet |
| Avalanche (AVAX) | $10.48 | +2.85% | Bigdata.com tearsheet |
| **Chainlink (LINK)** | **$13.78** | **+4.32%** | Bigdata.com tearsheet |
| Litecoin (LTC) | $70.82 | −1.51% | Bigdata.com tearsheet |
| Zcash (ZEC) | $1,545.27 | −0.02% (vs. prior close $1,545.58) | Alpha Vantage |
| Stellar (XLM) | $0.2230 | +2.52% (vs. $0.21752) | Alpha Vantage |
| Bitcoin Cash (BCH) | $338.13 | −0.03% (vs. $338.24) | Alpha Vantage |
| Hedera (HBAR) | $0.09349 | +0.51% (vs. $0.09302) | Alpha Vantage |
| Sui (SUI) | $1.0304 | +1.62% (vs. $1.0140) | Alpha Vantage |
| Shiba Inu (SHIB) | $0.00000580 | +0.35% (vs. $0.00000578) | Alpha Vantage |

No watchlist crypto position breached its 5% alert threshold today — LINK (+4.32%) came closest. This run's searches did not surface a distinct catalyst for LINK's or SOL's outperformance; both moved with a broad, moderate altcoin bid that did not extend to BTC or ETH, consistent with a mild risk-on tilt from the day's oil/yield relief rather than a crypto-specific story.

---

## Portfolio read (`analyst/watchlist.yaml`)

*Coverage this run: 53 of 53 tracked positions retrieved, despite Twelve Data being completely unavailable as a tool this session (see Connector status) — Alpha Vantage covered 4 GEXC names, 14 MOVERS names and 6 crypto pairs before hitting its 25-requests/day cap; Bigdata.com's company tearsheet (via `find_securities`) filled the remaining 16 GEXC names. One caveat: GOOG and GOOGL share one Alphabet Inc. entity-level price point in Bigdata.com's data (both share classes normally move almost identically but are not separately captured), and BABA/TSM resolved to their primary overseas listings (Hong Kong HKD and Taiwan TWD respectively, not the US-listed ADRs the watchlist symbols denote) — both flagged in the tables below rather than presented as exact ADR moves.*

### GEXC options-flow book (21 names, 3% threshold) — 3 breached

| Symbol | 1D | Source | Symbol | 1D | Source |
|---|---|---|---|---|---|
| AAPL | +1.53% | Alpha Vantage | MSFT | **+3.66%** | Bigdata.com |
| AMD | +0.22% | Bigdata.com | MU | +0.16% | Bigdata.com |
| AMZN | +0.12% | Bigdata.com | NFLX | −0.80% | Bigdata.com |
| AVGO | +0.70% | Bigdata.com | NOK | −0.48% | Bigdata.com |
| BABA | −1.45%* | Bigdata.com | ORCL | −1.76% | Bigdata.com |
| BAC | +1.20% | Bigdata.com | PFE | +0.92% | Bigdata.com |
| GOOG/GOOGL | +0.46%† | Bigdata.com | PLTR | −1.52% | Bigdata.com |
| HOOD | −1.18% | Bigdata.com | TSLA | −1.54% | Bigdata.com |
| **INTC** | **−3.45%** | Alpha Vantage | TSM | −1.00%* | Bigdata.com |
| **META** | **−3.33%** | Alpha Vantage | | | |
| NVDA | +0.22% | Alpha Vantage | | | |

*BABA priced in HKD (Hong Kong primary listing); TSM priced in TWD (Taiwan primary listing, prior session — Taiwan's exchange had already closed for the day). Both should track their NYSE ADRs closely in % terms but are not the ADR prints themselves.
†Both GOOG and GOOGL map to the same Alphabet Inc. entity in Bigdata.com's data this run; the two share classes can diverge slightly intraday (they did by ~0.2pp in the September 24 report).

- **MSFT +3.66%** — Copilot relaunch (unified "Home," "Code," "Autopilot" agent) plus a Stifel Buy upgrade; see Equities above.
- **META −3.33%** — profit-taking after this week's Muse-driven rally, triggered by a Goldman Sachs note questioning AI hyperscalers' capex payback economics; see Equities above.
- **INTC −3.45%** — reversed this week's +14.3% Muse-CPU-demand rally; no Friday-specific catalyst confirmed this run.

### MOVERS bot daily picks (14 names, 4% threshold) — 0 breached

Today's rotation: SNDK, CHPT, AGCO, NRG, SOXL, MRVL, CEG, KLAC, RIOT, STX, KNX, FOUR, ENTG, VST (all via Alpha Vantage `GLOBAL_QUOTE`).

| Symbol | 1D | Symbol | 1D |
|---|---|---|---|
| SNDK | +1.38% | RIOT | −2.04% |
| CHPT | −0.50% | STX | +1.20% |
| AGCO | +1.55% | KNX | −2.82% |
| NRG | +2.55% | FOUR | +0.79% |
| SOXL | +3.51% | ENTG | +2.19% |
| MRVL | +1.15% | VST | +0.38% |
| CEG | +0.63% | | |
| KLAC | +0.43% | | |

A quiet day for this book — SOXL's +3.51% (a leveraged semiconductor ETF) came closest to the 4% threshold, consistent with the sector's modest +0.79% (XLK) session.

### Index proxies (2% threshold) — none breached

| Symbol | 1D | Source |
|---|---|---|
| $SPX | +0.51% | Bigdata.com tearsheet |
| SPY | +0.54% | Bigdata.com tearsheet |
| QQQ | not retrieved — Nasdaq 100 index (^NDX) +0.42% used as disclosed proxy | Bigdata.com tearsheet |

QQQ itself wasn't retrieved this run (Alpha Vantage's daily cap was exhausted before reaching it, and the Bigdata.com tearsheet doesn't carry that specific ETF). ^NDX is a close proxy but not QQQ's actual print.

### Crypto book (15 names, 5% threshold) — 0 breached

See the Crypto section above for full detail, prices, and sourcing. LINK (+4.32%) was closest to the threshold.

---

## Portfolio summary: 53 of 53 tracked positions have confirmed data this run; 3 breached their alert threshold

All three breaches were in the GEXC book (3% threshold): **MSFT (+3.66%)** and **META (−3.33%)** both trace to sourced, specific catalysts; **INTC (−3.45%)** does not have a confirmed Friday-specific catalyst and is flagged as such rather than left unexplained. No MOVERS, index-proxy, or crypto position breached its threshold today.

---

## Risks to watch

- **Whether Iran's Hormuz proposal holds.** A Houthi attack on Saudi Arabia landed the same day as Araghchi's overture, and a separate Iranian official ruled out returning to a "pre-war diplomatic approach" — today's oil relief could reverse quickly on the next headline, as it has repeatedly this week in both directions.
- **The October 28 FOMC meeting**, with hike-odds estimates ranging 58–75% across sources checked today — itself a sign of how fluid the pricing is. December-hike odds were pegged around 92% (FXStreet).
- **AI-capex payback scrutiny.** Goldman Sachs' note naming Meta, Microsoft, Alphabet, Amazon and Oracle as needing ~$300B/year in AI revenue to break even (and $1T/year for real profitability) is a re-rating risk across the entire AI trade, not just Meta — worth watching whether other hyperscaler names see similar Friday-style reversals.
- **Oracle's continuing slide** (−1.76% today, −8.9% over 5 days, −29.67% YTD per Bigdata.com) — the financing-distress story flagged in the September 24 report (Project Jupiter force majeure, record CDS levels) looks like a persistent overhang rather than a one-day event.
- **Bond-market stress spilling into households and debt-laden firms**: the 30-year mortgage rate hit 7.45% (highest since 2023) and the 5-year Treasury broke 5% for the first time since 2007 earlier this week (Benzinga, InfoQuanta).
- **INTC's unexplained reversal** — worth a dedicated look on the next research pass, since this run's searches did not surface a Friday-specific catalyst despite Intel's strong week.
- **Trump–Xi summit follow-through**: the two-month tariff-truce extension (through January 10, 2027) buys time but leaves AI export controls, Taiwan, rare-earth access and China's reported continued parts shipments to Iran unresolved (Washington Post, AOL.com) — a source of headline risk rather than a settled backdrop.

---

## Connector status this run

- **Twelve Data: unavailable as a callable tool for this entire session.** Unlike prior reports, where it was rate-limited but still callable, no `mcp__Twelve_Data__*` tools loaded at all — the connector requires an interactive OAuth authorization that this non-interactive scheduled routine could not complete. This is a materially different failure mode than the per-minute credit cap flagged in `analyst/CONNECTORS.md` and in every prior report; the founder should re-authorize the connector via its `claude mcp`/`/mcp` flow (or claude.ai connector settings) if uninterrupted Twelve Data access is expected on future scheduled runs.
- **Alpha Vantage: hit its documented 25-requests/day cap partway through this run.** Used for the 6 crypto pairs not carried by the tearsheet (ZEC, XLM, BCH, HBAR, SUI, SHIB — all succeeded, with two initial per-second throttling errors that cleared on immediate retry), 4 GEXC names (AAPL, NVDA, META, INTC) and all 14 MOVERS names, before a call for ORCL returned the hard "25 requests per day" rate-limit error. A `REALTIME_BULK_QUOTES` call was attempted first to cover more symbols per request but returned a gated premium-plan response with fabricated sample data (correctly identified as such and discarded, not used).
- **Bigdata.com: no failures this run** — the most reliable connector again, and the source for the full cross-asset macro wrap, 9 of 15 crypto pairs, essentially all of today's narrative/causal-chain sourcing, and — as a fallback once Alpha Vantage's cap was hit — 16 of the 21 GEXC book's equity quotes via its company tearsheet (`find_securities` + `bigdata_company_tearsheet`). One resolution error caught and corrected mid-run: `find_securities` initially resolved watchlist symbol "NOK" to NOK Corporation (a Japanese auto-parts maker) rather than Nokia Oyj; re-querying by full company name ("Nokia Corporation") fixed it.
- **Blockscout and Quartr:** confirmed available as callable tools this session but not invoked — no on-chain or filing-level question came up in today's research.

No data point in this report was filled in from general training knowledge in place of a failed or gated connector call. The one item reported without a confirmed catalyst: INTC's −3.45% move.

---

## Sources

Market levels and cross-asset data: [Bigdata.com](https://bigdata.com) market tearsheet (sourced from FMP), as of ~8:00–9:33 PM UTC, September 25, 2026, and Bigdata.com company tearsheets (FMP) for individual GEXC equities. Crypto pairs not carried by the tearsheet and a subset of equity quotes: Alpha Vantage `DIGITAL_CURRENCY_DAILY` and `GLOBAL_QUOTE`. News, causal narrative, and analyst commentary: Bigdata.com news search, aggregating MT Newswires (Global Energy and general), CNBC.com, CNBC Pro, FXStreet News, Reuters (via multiple wires), AP/Transport Topics, Straits Times, The Korea Times, The Economic Times, Nasdaq/Barchart, Benzinga, InfoQuanta, PubT (Fidelis Capital Partners, Chung Wu Investment Group, MAI Capital Management notes), Yahoo! Finance, AOL.com, Morningstar, Crypto Briefing, TheBull.com.au, Rolling Out, Edaily, The Washington Post, Politico, Alliance News, France 24, Mediapart, Finanz und Wirtschaft, and others, all published September 25, 2026. Watchlist: `analyst/watchlist.yaml`.
