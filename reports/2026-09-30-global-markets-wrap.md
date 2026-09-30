# Global Markets Wrap — September 30, 2026

*Compiled from Bigdata.com (market tearsheet, company tearsheets, and news search). **Twelve Data required interactive OAuth authorization that this non-interactive scheduled session could not complete — unavailable as a callable tool for the entire run, the same failure mode flagged in every scheduled brief since September 25.** **Alpha Vantage's 25-requests/day cap was already exhausted before this session made a single successful call** (confirmed via two calls returning the explicit daily-cap error, one seconds apart) — almost certainly consumed by other activity against the same shared API key earlier today; it was therefore unavailable for the entire run and every individual-security and crypto quote below was sourced from Bigdata.com instead (via `find_securities` + `bigdata_company_tearsheet`/`bigdata_etf_tearsheet`). Cross-asset levels from the Bigdata.com/FMP tearsheet as of ~8:00–9:35 PM UTC, September 30, 2026; individual equity quotes are intraday/real-time as of ~9:34–9:36 PM UTC (per-position sourcing below). Blockscout and Quartr were not needed for today's research (no on-chain or filing-level question came up) and were not checked for availability. **This is a draft for human review, not a trade recommendation** — see `analyst/GUARDRAILS.md`.*

## TL;DR

A cooler-than-expected August PCE inflation print (headline +0.3% m/m / 3.4% y/y, core +0.2% m/m / 3.0% y/y, both below consensus) initially sent Fed October-hike odds tumbling — from roughly 70–71% on Tuesday to as low as ~35–37% by the close — but the relief didn't hold through the bond market: a much stronger-than-expected 0.9% jump in personal spending, an upward revision to Q2 GDP (to 2.2% annualized from 1.5%), and hawkish commentary from Fed Governor Michael Barr (renewing his call for more hikes) pushed long-dated Treasury yields to fresh multi-decade highs anyway — the 10-year closed at 5.29% (highest since 2007) and the 30-year at 5.64% (highest since June 2002, its seventh straight daily rise). That "good inflation data, bad bond market" combination hit the Dow hard — down 443.87 points (-0.86%) to its lowest close since mid-June, snapping a five-month winning streak — while the Nasdaq Composite actually rose 0.24% on tech strength. Oil rallied on a Russia diesel-export-ban extension and continued Strait of Hormuz tanker attacks, even as Saudi supply recovery continues elsewhere. In the portfolio, two GEXC names breached their alert threshold in opposite directions (INTC +3.71% on a broad semiconductor rally, HOOD -3.20% despite bullish sell-side reaction to its AI-agent product launch), two MOVERS names breached (CHPT +5.94% on a momentum/short-squeeze continuation, RIOT -5.80% on no identifiable news), and CEG fell 3.99% — just short of its 4% threshold — after FERC delayed a PJM grid capacity plan, before reversing over 3% after-hours on a 20-year Amazon nuclear power deal.

**Note on context:** this is the same rate-hike cycle flagged in every report since the Fed's September hike — today's specific wrinkle is that a genuinely dovish inflation data point did not translate into a dovish market, because strength elsewhere (spending, growth, a hawkish Fed voice) outweighed it. That's a reminder that a single soft CPI/PCE print is not, by itself, a reliable signal for where yields go next in this cycle.

---

## The trigger: cool PCE, hot everything else — yields grind to fresh multi-decade highs anyway

*Source: CNBC.com, The Globe and Mail, Benzinga, MT Newswires, AOL.com, Nasdaq, Charlotte Observer, all September 30, 2026.*

August's PCE price index — the Fed's preferred inflation gauge — rose a seasonally adjusted 0.3% m/m, putting the 12-month gain at 3.4% (economists had looked for 3.7%); core PCE came in at 0.2% m/m / 3.0% y/y, also below the 0.3%/3.3% consensus. Treasury yields initially fell on the print — the 10-year briefly touched 5.20% intraday — and CME FedWatch-implied odds of an October Fed hike dropped sharply, from roughly 70–71% a day earlier to as low as ~35–45% depending on the hour and source cited (MT Newswires had it at 35% by the close; other intraday wires cited 37–44%). That relief didn't last: the same report showed personal consumption expenditures (actual spending, not the price index) jumped 0.9% and real PCE rose 0.6% — both stronger than expected — and the BEA's third estimate of Q2 GDP was revised up to 2.2% annualized from 1.5%, evidence the economy grew faster than previously thought. Layered on top, Fed Governor Michael Barr renewed his call for additional rate increases to fight sticky inflation, while New York Fed President John Williams reiterated a more patient stance (no urgency, but one further hike "may be appropriate late this year"). Net effect: the 10-year Treasury yield closed at 5.29% (+3.8bp), its strongest level since 2007, and the 30-year closed at 5.64% (+3.9–5bp depending on the source), its highest since June 2002 and a seventh consecutive daily increase — the longest such streak in two years per Benzinga. The 2-year yield, by contrast, eased to ~4.89% after hitting a 52-week high on Tuesday, so the move was concentrated at the long end.

**The cascade:** a cooler PCE print sends October hike odds sharply lower intraday → but stronger spending, an upward GDP revision, and a hawkish Fed voice (Barr) reverse the yield relief by the close, pushing 10s and 30s to fresh multi-decade highs → higher long-end yields make richly-valued equities look expensive, hitting cyclicals, healthcare, and consumer staples hardest → the Dow (more cyclical-weighted) falls sharply while the Nasdaq (tech-heavy) actually gains, since the same-day AI/semiconductor narrative was strong enough to offset the rates headwind for that sector specifically → oil rallies independently on a Russia diesel-export-ban extension and continued Hormuz tanker attacks, a geopolitical/refined-product story that isn't really about the Fed at all.

---

## Rates

*Source: Bigdata.com market tearsheet (FMP), as of September 30, 2026; corroborated by CNBC.com and The Globe and Mail wire prints.*

| Maturity | Yield | 1D change |
|---|---|---|
| 1 Month | 4.02% | -0.50% |
| 2 Month | 4.16% | -0.48% |
| 3 Month | 4.20% | -1.18% |
| 6 Month | 4.33% | -0.69% |
| 1 Year | 4.54% | -0.87% |
| 2 Year | 4.88% | -0.20% |
| 3 Year | 5.00% | +0.40% |
| 5 Year | 5.09% | +0.59% |
| 7 Year | 5.19% | +0.58% |
| 10 Year | 5.29% | +0.57% |
| 20 Year | 5.68% | +0.71% |
| 30 Year | 5.64% | +0.89% |

*("1D change" is the relative change in the yield level per Bigdata.com/FMP, not basis points.)* The curve bear-steepened at the long end today — 7-year and out all rose while the front end (1M–2Y) actually eased slightly — the mirror image of the intraday move: short-end yields tracked the initial dovish PCE reaction, while the long end reflects the stronger-spending/hawkish-Fed reversal that dominated by the close. The 10-year's 5.29% close is its highest level since 2007; the 30-year's 5.64% is a fresh 24-year high (since June 2002) and its seventh straight daily rise.

---

## Equities

### US: Dow snaps five-month win streak on cyclical/staples selling; Nasdaq gains on tech strength

*Source: Bigdata.com market tearsheet (FMP), as of ~8:00–9:12 PM UTC; corroborated by ABC News, Alliance News, MT Newswires wire prints.*

| Index | Level | 1D |
|---|---|---|
| S&P 500 | 7,651.54 | -0.25% |
| Dow Jones Industrial Avg | 50,906.05 | -0.86% |
| NASDAQ Composite | 26,861.06 | +0.24% |
| NASDAQ 100 | 30,408.50 | +0.23% |
| Russell 2000 | 2,796.86 | -0.39% |
| CBOE Volatility Index (VIX) | 16.34 | +1.87% |

The Dow fell 443.87 points, its worst close since mid-June, ending a five-month winning streak (September: -4.3%) as selling concentrated in cyclicals, healthcare, and consumer staples — names most sensitive to the fresh leg higher in long-end yields. The S&P fell a milder 0.25% and the Nasdaq Composite actually rose 0.24% (September: +1.9%, a second straight monthly gain), as the same-day semiconductor rally (see Portfolio below) was strong enough to offset the rates headwind for tech specifically. The VIX rose 1.87% to 16.34 and is up notably on a 5-day (+9.89%) and 1-month (+9.52%) basis even though today's move alone was modest — a quieter but real rise in hedging demand under the surface of a "little-changed" index day.

| Sector (ETF) | 1D |
|---|---|
| Technology (XLK) | +0.64% |
| Energy (XLE) | -0.06% |
| Communication Services (XLC) | -0.45% |
| Consumer Discretionary (XLY) | -0.28% |
| Utilities (XLU) | -0.68% |
| Materials (XLB) | -0.81% |
| Real Estate (XLRE) | -1.04% |
| Financials (XLF) | -1.16% |
| Industrials (XLI) | -1.27% |
| Health Care (XLV) | -1.35% |
| Consumer Staples (XLP) | -1.52% |

Technology was the only sector ETF to close higher; note that a same-day MT Newswires close print described "technology and communication services" as the session's sole gainers — the tearsheet snapshot (~8 PM UTC) shows Communication Services down 0.45%, a modest discrepancy likely reflecting different snapshot times relative to the 4 PM ET cash close, flagged rather than resolved. **Energy was roughly flat (-0.06%) despite crude oil rallying over 1% on the day** — the same disconnect flagged in the September 29 report, now recurring for a second session.

### Rest of world: South Korea and Turkey lag; Japan and China firmer

*Source: Bigdata.com market tearsheet (FMP), ETF proxies and major indexes.*

| Country/Region (ETF) | Ticker | 1D | Index level | Index 1D |
|---|---|---|---|---|
| South Korea | EWY | -2.31% | KOSPI | -0.48% |
| Turkey | TUR | -2.73% | — | — |
| Thailand | THD | -2.52% | SET | -2.21% |
| Taiwan | EWT | -1.06% | TWSE (TAIEX) | +0.65% |
| Hong Kong | EWH | -0.50% | Hang Seng | -0.12% |
| China | MCHI | +0.17% | — | — |
| Japan | EWJ | +0.98% | Nikkei 225 | +1.94% |

**South Korea's ETF (EWY, -2.31%) diverged sharply from its own index (KOSPI, -0.48%) — the same unresolved ETF-vs-index gap flagged in the September 29 report, now recurring.** Taiwan shows a similar split (EWT -1.06% vs. TAIEX +0.65%). This run's searches did not investigate either gap in depth; flagged as an observed pattern worth a dedicated check, not an explained one. Turkey (-2.73% on the day, -16.19% over the past month per the tearsheet) continues a multi-week slide that predates today and wasn't re-researched given time constraints — not every laggard gets its own search in a daily brief.

---

## Commodities

### Energy — oil rallies on Russia's diesel export ban and continued Hormuz attacks; a Brent tearsheet/wire discrepancy persists

*Source: Bigdata.com/FMP tearsheet; MT Newswires, Nasdaq (Barchart), FXStreet, The Globe and Mail, InfoQuanta, all September 30, 2026.*

| Commodity | Tearsheet price/1D | Wire settlement |
|---|---|---|
| WTI Crude | $90.42 / +1.16% | $90.42, up 1.2% (MT Newswires — **agrees**) |
| Brent Crude | $97.88 / +1.79% | $103.63, up 1.0% (MT Newswires — **disagrees**) |
| Natural Gas | $3.03 / +0.50% | — |
| Gasoline RBOB | $3.27 / +4.31% | $3.27, up ~4.1–4.3% (Nasdaq/Barchart — agrees) |
| Heating Oil | $4.68 / +3.77% | — |

**The Brent gap flagged in the September 29 report persists today.** The Bigdata.com/FMP tearsheet's Brent print ($97.88, +1.79%) is materially below the wire-settlement figure multiple sources converged on ($103.63, +1.0%, per MT Newswires; The Globe and Mail separately reported Brent "climbed 1.9% to settle at $98.03," a third figure). As flagged previously, the November Brent contract's expiry and the roll to December front-month around this exact date is the likely source of cross-source noise; this run did not fully reconcile which print is the single "true" number, so both are shown. WTI, whose front-month contract isn't rolling, shows tight agreement across sources at $90.42.

Crude and gasoline rallied after Russia extended its ban on most diesel exports through October (tightening global refined-product supply further) and continued attacks on vessels transiting the Strait of Hormuz (UK Maritime Trade Operations reported three tankers struck Tuesday). EIA data showed gasoline inventories at a nearly 12-year low and a surprise draw in distillate stockpiles, both bullish. Countervailing bearish factors — Saudi Arabia's East-West pipeline restoration, continued high Saudi export volumes (5.28 million bpd in September, a seven-month high), and a fresh US Strategic Petroleum Reserve release of up to 40 million barrels — kept the rally from running further; President Trump also denied reports of pending Iran sanctions relief, adding a geopolitical premium. Both benchmarks remain on track for a third consecutive monthly gain.

### Metals

*Source: Bigdata.com/FMP tearsheet.*

| Metal | Price | 1D |
|---|---|---|
| Gold Futures | $4,186.70 | +0.17% |
| Silver Futures | $60.76 | -0.65% |
| Platinum | $1,718.90 | +1.05% |
| Palladium | $1,212.40 | -0.11% |
| Copper | $6.62/lb | +0.27% |

Gold ticked up modestly even against a backdrop of fresh multi-decade-high Treasury yields — normally a headwind for a non-yielding asset — while silver fell more in line with that mechanism. This run's searches did not surface a specific catalyst for gold's small divergence; presented as an observed data point, not an explained one (the same caveat noted for gold in the September 29 report).

---

## Crypto

*Source: Bigdata.com market tearsheet, as of ~9:33 PM UTC. **9 of the fund's 15 watchlist pairs are covered below; the remaining 6 (ZEC, XLM, BCH, HBAR, SUI, SHIB) could not be sourced this run** — they aren't carried by the Bigdata.com tearsheet, and both connectors that normally fill that gap (Alpha Vantage `DIGITAL_CURRENCY_DAILY`, Twelve Data) were unavailable for the entire session (see Connector status). This is a genuine data gap, not a number filled from memory.*

| Asset | Price | 1D |
|---|---|---|
| Bitcoin (BTC) | $83,703.31 | +0.09% |
| Ethereum (ETH) | $2,683.60 | +0.26% |
| XRP | $1.49 | -0.15% |
| Solana (SOL) | $118.00 | -0.89% |
| Dogecoin (DOGE) | $0.09 | +0.41% |
| Cardano (ADA) | $0.24 | +0.00% |
| **Avalanche (AVAX)** | **$10.92** | **-4.50%** |
| Chainlink (LINK) | $14.32 | -1.89% |
| Litecoin (LTC) | $66.59 | -0.31% |

**AVAX (-4.50%) is a sharp reversal of the prior two sessions' Goldman-Sachs-driven rally (+7.76% Tuesday, +12% over 24 hours as of Tuesday per Yahoo! Finance) and the closest crypto position to its alert threshold today, though it did not breach the fund's 5% level.** This run's searches found no fresh negative catalyst specific to today — the most relevant item found was a September 23 Form 8-K disclosure (reported September 29) that Avalanche Treasury Corporation (AVAT) sold roughly $15 million of its longest-dated locked AVAX tokens to the Avalanche Foundation for debt reduction, a mild bearish supply signal but not obviously sized to explain a same-day 4.5% move. Read most plausibly as profit-taking after a sharp, narrow-catalyst rally rather than a new negative story — flagged as an observed-but-not-fully-explained move rather than a confirmed one.

---

## Portfolio read (`analyst/watchlist.yaml`)

*Coverage this run: 47 of 53 tracked positions retrieved. Twelve Data was unavailable all session; Alpha Vantage's daily cap was already exhausted before this session's first call. All 38 equity/ETF positions (21 GEXC, 14 MOVERS, 3 index proxies) were sourced from Bigdata.com (`find_securities` + `bigdata_company_tearsheet`/`bigdata_etf_tearsheet`), real-time/intraday as of ~9:34–9:36 PM UTC. 9 of 15 crypto pairs came from the Bigdata.com tearsheet (~9:33 PM UTC); the remaining 6 (ZEC, XLM, BCH, HBAR, SUI, SHIB) have no data this run — see Crypto section above.*

### GEXC options-flow book (21 names, 3% threshold) — 2 breached

| Symbol | 1D | Symbol | 1D |
|---|---|---|---|
| **HOOD** | **-3.20%** | NFLX | -1.02% |
| **INTC** | **+3.71%** | NOK | -2.03% |
| AAPL | +1.10% | NVDA | +0.51% |
| AMD | +0.69% | ORCL | -0.35% |
| AMZN | +1.01% | PFE | -0.70% |
| AVGO | -1.10% | PLTR | +0.04% |
| BABA | +0.38%* | TSLA | +0.56% |
| BAC | -0.96% | TSM | +0.20%† |
| GOOG/GOOGL | +0.93%‡ | MSFT | +0.77% |
| META | -1.84% | MU | +0.00% |

*BABA priced in HKD (Hong Kong primary listing, $106.60), not the NYSE ADR — consistent with how Bigdata.com's entity resolution has handled this name in prior runs. †TSM quoted in TWD (Taiwan exchange), as of its ~05:30 UTC (Taiwan-hours) snapshot. ‡GOOG and GOOGL both map to Alphabet Inc. in Bigdata.com's data — one shared price point ($344.08).

- **INTC (+3.71%)** rode a broad September semiconductor rally (SOXX ETF +11% on the month, its best since June) on resilient AI-infrastructure/data-center spending and elevated CPU demand tied to agentic AI workloads; Intel Foundry revenue reportedly grew 31% y/y in Q2, the strongest growth among non-memory IDMs (Counterpoint Research, cited via Benzinga). Analyst sentiment is more mixed than the price action — consensus rating is Hold with a $114–116 average target, against a stock that's already up ~256% over 12 months and trading near 63x forward earnings.
- **HOOD (-3.20%)** fell despite broadly bullish sell-side reaction (Morgan Stanley Overweight/$150 target, KeyBanc raising to $140, Deutsche Bank reiterating Buy/$134) to its HOOD Summit product launches — AI-driven "Robinhood Agents," US perpetual futures via Bitstamp, and 24/7 weekend equities trading. The stock fell anyway; no single negative catalyst was identified beyond broader financial-sector weakness tied to the day's yield spike (Financials sector ETF -1.16%).

### MOVERS bot daily picks (14 names, 4% threshold) — 2 breached

Today's rotation: SNDK, CHPT, AGCO, NRG, SOXL, MRVL, CEG, KLAC, RIOT, STX, KNX, FOUR, ENTG, VST.

| Symbol | 1D | Symbol | 1D |
|---|---|---|---|
| SNDK | +0.59% | **RIOT** | **-5.80%** |
| **CHPT** | **+5.94%** | STX | +0.97% |
| AGCO | -1.66% | KNX | -0.93% |
| NRG | -1.56% | FOUR | -2.45% |
| SOXL | +0.59% | ENTG | -0.46% |
| MRVL | +0.36% | VST | -1.76% |
| CEG | -3.99% | | |
| KLAC | -0.81% | | |

- **CHPT (+5.94%)** extended a dramatic September run (up roughly 80% over the trailing month per the tearsheet) that began with a Q2 earnings beat ($116M revenue, +18% y/y, improved margins, a much smaller loss than expected) into a heavily-shorted stock — Kalkine Media frames the continuation as a short-squeeze dynamic rather than fresh news, with no new same-day catalyst identified and peers EVgo (-3%) and Blink Charging (-0.45%) showing no spillover.
- **RIOT (-5.80%)** — **no news surfaced.** Two separate searches (direct entity query, and a broader Bitcoin-miner/hashrate query) returned zero results. Bitcoin itself was flat (+0.09%) today, so this reads as an idiosyncratic, single-name move; stated here as an unexplained data point rather than guessed at.
- **CEG (-3.99%)**, the closest non-breach to its 4% threshold, fell alongside NRG and Talen Energy after FERC suspended PJM Interconnection's reliability backstop capacity-procurement filing for five months pending a paper hearing — TD Cowen called the renewed uncertainty "negative for all involved" for grid operators racing to meet AI-driven power demand. The stock reversed sharply after-hours (+3.5–5% per Yahoo!/Wallstreetcn) on news of a 20-year, $3B+ nuclear power purchase agreement with Amazon for the Calvert Cliffs plant — a same-day swing not captured in the 1D figure above, which is sourced to the ~9:34 PM UTC intraday snapshot before the after-hours move.

### Index proxies (2% threshold) — none breached

| Symbol | 1D | Source |
|---|---|---|
| $SPX | -0.25% | Bigdata.com tearsheet (^SPX) |
| SPY | -0.23% | Bigdata.com tearsheet |
| QQQ | +0.25% | Bigdata.com ETF tearsheet |

### Crypto book (15 names, 5% threshold) — none breached; 6 of 15 unfilled

See the Crypto section above for full detail. AVAX (-4.50%) came closest to breaching but did not cross the 5% threshold. ZEC, XLM, BCH, HBAR, SUI, and SHIB have no data this run (see Connector status).

---

## Portfolio summary: 47 of 53 tracked positions have confirmed data this run; 4 breached their alert threshold; 6 crypto pairs unfilled

Breaches: **GEXC book (2 of 21, 3% threshold)** — INTC (+3.71%, broad semiconductor-sector rally) and HOOD (-3.20%, no clear catalyst despite a bullish product launch). **MOVERS book (2 of 14, 4% threshold)** — CHPT (+5.94%, short-squeeze continuation of a post-earnings rally) and RIOT (-5.80%, no news found). **Crypto book (0 of 15, 5% threshold)** — AVAX came closest at -4.50% (profit-taking after this week's Goldman/Lynq-driven rally) but did not breach. **No index-proxy position breached.** CEG (-3.99%) is flagged as a near-miss just below the MOVERS book's 4% threshold.

---

## Risks to watch

- **Whether today's yield reversal (cool PCE → hawkish-data-and-Fed-commentary reversal) repeats around Friday's nonfarm payrolls report** — a hot print could extend the 10-year/30-year's run to fresh multi-decade highs and pressure equities further, especially cyclicals.
- **The unresolved Brent tearsheet-vs-wire discrepancy** (now flagged two sessions running) — worth confirming directly with Bigdata.com or a second connector before any Brent data point from this system is used in position sizing.
- **The South Korea and Taiwan ETF-vs-index divergences**, also now recurring across two sessions — unresolved in this run's sourcing.
- **RIOT's unexplained -5.80% move** — a single-name decline with no identifiable catalyst against a flat Bitcoin tape; worth a dedicated check next time it's flagged.
- **CEG/NRG/Talen's FERC-driven weakness** — the PJM capacity-procurement delay is a multi-month overhang for AI-data-center-exposed power names generally, not a one-day story; CEG's sharp after-hours reversal on the Amazon deal shows how fast that narrative can flip on company-specific news.
- **The six-crypto-pair data gap (ZEC, XLM, BCH, HBAR, SUI, SHIB)** persists as long as Alpha Vantage's daily cap is exhausted early and Twelve Data remains unauthorized — this is now a recurring, not one-off, monitoring blind spot for roughly 40% of the crypto book.

---

## Connector status this run

- **Twelve Data: unavailable as a callable tool for the entire session** — the same failure mode documented in every scheduled run since September 25. It requires an interactive OAuth authorization that this non-interactive scheduled routine cannot complete. The founder should re-authorize via claude.ai connector settings (or `claude mcp`/`/mcp` in an interactive session) if uninterrupted Twelve Data access is expected going forward.
- **Alpha Vantage: 25-requests/day cap was already exhausted before this session's first call.** Two calls (`DIGITAL_CURRENCY_DAILY` for ZEC, seconds apart) both returned the explicit daily-cap error message naming the API key (N9QYR08EFWEGLVFZ) and the 25-requests/day limit — not the generic per-second throttling message — confirming this was the hard daily ceiling, not a transient rate limit. Per house rule, this was not retried in a hot loop; all individual-security and crypto sourcing for this report was rerouted to Bigdata.com instead. The likely explanation is that the same shared API key was already used up by other activity (e.g. an earlier watchlist-check pass) before this scheduled brief ran; the daily cap resets on API-key-local midnight, not this session's start time.
- **Bigdata.com: no outright failures this run** — the source for the full cross-asset macro wrap, all narrative/causal-chain sourcing, 9 of 15 crypto pairs, and — in place of both Twelve Data and Alpha Vantage — all 38 individual equity/ETF quotes in the portfolio section via `find_securities` + `bigdata_company_tearsheet`/`bigdata_etf_tearsheet`. One resolution note: `find_securities` for "GOOG" returned Google LLC (a private subsidiary entity) rather than the public parent; a follow-up query for "Alphabet Inc" resolved correctly.
- **Blockscout and Quartr:** not checked for availability this run — no on-chain or filing-level question came up in today's research. Both were confirmed available in the September 25 run and there is no reason to believe that changed.

No data point in this report was filled in from general training knowledge in place of a failed or gated connector call. Three items are flagged as observed-but-unexplained rather than sourced to a confirmed cause: gold's small daily gain against a rising-yield backdrop, AVAX's reversal, and RIOT's decline. The Brent tearsheet/wire discrepancy and the South Korea/Taiwan ETF-index divergences are flagged as unresolved data-quality questions rather than market events.

---

## Sources

Market levels and cross-asset data: [Bigdata.com](https://bigdata.com) market tearsheet (sourced from FMP), as of ~8:00–9:35 PM UTC, September 30, 2026, and Bigdata.com company/ETF tearsheets (FMP) for individual portfolio equities and ETFs (real-time, ~9:34–9:36 PM UTC). News, causal narrative, and analyst commentary: Bigdata.com news search, aggregating CNBC.com, The Globe and Mail, ABC News, Alliance News, MT Newswires, Benzinga, AOL.com, Nasdaq (Barchart/RTTNews/Zacks), Yahoo! Finance, FXStreet News, InfoQuanta/Cailian Press, Charlotte Observer, The Wichita Eagle, Boursorama, Morningstar, Kalkine Media, Tron Weekly Journal, Brave New Coin, The Cryptonomist, Watcher Guru, The Fly, Eastmoney (东方财富网), Chinatimes, 36Kr, Central Charts, and Wallstreetcn, all published September 30, 2026 (one AVAX-context item dated September 28–29). Watchlist: `analyst/watchlist.yaml`.
