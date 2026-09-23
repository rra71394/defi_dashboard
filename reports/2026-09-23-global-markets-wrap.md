# Global Markets Wrap — September 23, 2026

*Compiled from Bigdata.com (market tearsheet + news search), Twelve Data (equity quotes), and Alpha Vantage (crypto pairs not carried by the tearsheet, Treasury-yield freshness check). Blockscout and Quartr were confirmed available as callable tools this session but not invoked — no on-chain or filing-level question came up today. Cross-asset levels from the Bigdata.com/FMP tearsheet as of ~8:00–9:45 PM UTC, September 23, 2026; individual equity quotes from Twelve Data `get_quote`, pulled through the evening UTC in small batches to stay under the connector's 8-credit/minute cap — the cap was **materially degraded this run** (credits did not reliably clear between minutes; see Connector status), which limited how much of the MOVERS book could be retrieved. **This is a draft for human review, not a trade recommendation** — see `analyst/GUARDRAILS.md`.*

## TL;DR

A hot September flash PMI and a hawkish speech from Fed Governor Michael Barr combined to push the odds of an October Fed rate hike from ~55% to 69–73% (CME FedWatch) in the space of a few hours, sending the 10-year Treasury yield to **5.11–5.14%, its highest since 2007 (a 19-year high)**, with the 2-year and 5-year both breaking above 4.9% and 5% respectively for the first time since 2007. That single move rippled through every asset class: US equities fell broadly (S&P 500 -0.76%, Nasdaq Composite -1.13%), gold and silver sold off on the stronger dollar and higher real yields (gold -1.33%, silver -2.35%), and crypto — already extended after a short-squeeze rally into September 21 — sold off hard, with several altcoins (AVAX -8.16%, DOGE -7.66%, ADA -6.19%, LINK -5.65%) breaching the fund's 5% alert threshold. Layered on top: crude oil snapped a five-session losing streak (WTI +1.81% to $92.16, Brent +4.24% to $103.46) on a cargo-vessel attack in the Strait of Hormuz (one Indian sailor killed) and reports the Trump administration is weighing a 90-day US diesel export ban — a move the oil industry warns would raise, not lower, fuel prices. Markets are also positioning ahead of Thursday's Trump-Xi summit in Washington (trade truce extension, AI dialogue) and Meta's two-day Connect conference, which kicked off today.

**Note on context:** this is the same rate-hike cycle flagged in recent reports — the Fed hiked 25bp on September 16 (first hike since 2023) and its dot plot showed 16 of 18 FOMC participants expecting at least one more increase this year. Today's PMI and Fed-official commentary are the market repricing that expectation higher and sooner (October 27–28 meeting) rather than a new cutting-cycle narrative.

---

## The trigger: a hot PMI, a hawkish Fed governor, and a 19-year yield high

*Source: MT Newswires, CNBC.com, FXStreet News, Nasdaq/Barchart, Yonhap News, Nikkei Japan, CNN, all September 23, 2026.*

US private-sector output accelerated to its fastest pace in more than five years in September: S&P Global's flash Composite PMI rose to **58.4** (from 56.0 in August), with Manufacturing at 57.0 (vs. 53.5 expected) and Services at 58.7 — the highest readings since 2021 for both. Input-cost pressures also intensified to their **highest level since October 2022**, per the same report. Treasury yields jumped immediately: the 10-year rose as much as 14.1 basis points to **5.11–5.14%** (CNN and MT Newswires both confirm a 19-year high; MT Newswires notes 5-year yields also broke above 5% for the first time since 2007), and the 2-year surged 12–17bp to roughly 4.9–4.91%, its highest since 2024.

Fed Governor Michael Barr then added fuel at a Chicago Fed housing conference, saying "further policy adjustments are likely to be needed to ensure inflation comes down to target in a timely fashion" and that "risks to achieving our inflation target have increased, while risks to the labor market have receded." St. Louis Fed's Alberto Musalem and Boston Fed's Susan Collins (neither a 2026 voter) made similar remarks earlier in the week. Markets responded by pushing October rate-hike odds from **55% on Tuesday to 69–73% Wednesday** (accounts vary slightly by source/timestamp — CME FedWatch via MT Newswires: 71%; CNBC: 73%; FXStreet: 66-70%), and the US Dollar Index rose to a roughly two-month high.

**Separately, and reinforcing the same inflation-scare narrative:** oil snapped its five-session losing streak. Two developments drove the reversal: (1) the UK's Maritime Trade Operations reported a cargo vessel (identified as the Antigua/Barbuda-flagged bulk carrier *MV Cape Dao*) was struck by an unknown projectile in the Strait of Hormuz around 06:30 UTC, catching fire and drifting; one Indian seafarer was killed and the rest of the 27-person crew evacuated — this is the latest in a string of Hormuz attacks even as US Central Command has redirected 115 commercial vessels as part of a naval blockade on Iranian ports; and (2) Politico reported the Trump administration is preparing a 90-day US diesel export ban (the US supplies ~20% of diesel traded globally by sea, per the American Petroleum Institute), which Treasury Secretary Scott Bessent confirmed is under review, though the White House disputed the Politico report and Energy Secretary Chris Wright said the administration favors "restrictions," not an outright ban. WTI rose 1.81% to $92.16 and Brent rose 4.24% to $103.46 by the tearsheet's evening snapshot, with after-hours prints (MT Newswires, ~5:11 PM ET) running slightly higher still — WTI $92.88 (+2.8%), Brent $103.56 (+4.3%) — as the diesel-ban and "Iran won't surrender" headlines (Iranian President Masoud Pezeshkian, addressing the UN General Assembly) continued to land after the settle. US diesel futures themselves initially fell (-4% at one point) when reports characterized the ban as imminent, before the White House pushback; oil-industry economists (Rapidan Energy's Bob McNally, GasBuddy's Patrick De Haan) warn a real ban would cut refinery diesel production and push retail gasoline and diesel prices — already at record highs (diesel averaging $6.52/gallon nationally per AAA, per Politico) — higher, not lower.

**The cascade:** hot PMI + hawkish Fed speak → October hike odds jump → yields to a 19-year high → stronger dollar → gold/silver sell off; separately, oil's reversal on Hormuz/diesel-ban risk adds an independent inflation-scare leg. Equities fell on both the higher-discount-rate mechanism and the renewed energy-cost worry; crypto — already stretched after a short-covering rally into Monday — amplified the equity move on the rate-sensitivity read plus its own overbought unwind (see Crypto section).

---

## Rates

*Source: Bigdata.com market tearsheet (FMP); Alpha Vantage `TREASURY_YIELD` for freshness cross-check.*

| Maturity | Yield | 1D change |
|---|---|---|
| 1 Month | 3.99% | +0.50% |
| 2 Month | 4.10% | +0.24% |
| 3 Month | 4.19% | +0.72% |
| 6 Month | 4.31% | +1.17% |
| 1 Year | 4.49% | +1.35% |
| 2 Year | 4.85% | +2.97% |
| 3 Year | 4.97% | +3.33% |
| 5 Year | 4.99% | +3.31% |
| 7 Year | 5.05% | +3.27% |
| 10 Year | 5.11% | +3.02% |
| 20 Year | 5.45% | +2.25% |
| 30 Year | 5.40% | +2.08% |

*("1D change" is the relative change in the yield level per Bigdata.com/FMP, not basis points.)*

The curve moved up in a broadly parallel shift, with the belly (2Y–7Y) moving hardest in relative terms — consistent with a repricing of near-term Fed policy rather than a long-end inflation-expectations story alone (the 10-year's absolute move, +14bp, was still the largest in basis-point terms). Wire prints (CNN, MT Newswires) put the intraday 10-year high slightly above the tearsheet's snapshot, at 5.12–5.14%. **Freshness cross-check:** Alpha Vantage's `TREASURY_YIELD` daily series shows its most recent print dated **September 21 (4.96%)** — two calendar days behind today's session and well below today's 5.11% print, continuing the staleness pattern flagged in every report since September 14. Do not use the Alpha Vantage series as a same-day figure.

---

## Equities

### US indexes and sectors

*Source: Bigdata.com market tearsheet (FMP), as of ~8:00–9:45 PM UTC; cross-checked against MT Newswires' close (Nasdaq Composite -1.1% to 26,936.04, Dow -0.7% to 51,511.59, S&P 500 -0.7% to 7,706.03), which matches the tearsheet almost exactly.*

| Index | Level | 1D |
|---|---|---|
| S&P 500 | 7,706.03 | -0.76% |
| Dow Jones Industrial Avg | 51,511.59 | -0.68% |
| NASDAQ Composite | 26,936.04 | -1.13% |
| NASDAQ 100 | 30,470.29 | -0.85% |
| Russell 2000 | 2,838.66 | -1.77% |
| CBOE Volatility Index (VIX) | 15.18 | +6.83% |

The VIX jumped 6.83% to 15.18, ending a run of vol compression seen in prior reports — still a low absolute level, but the day's move reflects genuine repricing rather than a panic. Small-caps (Russell 2000 -1.77%) underperformed large-caps, consistent with higher rate-sensitivity. Semiconductor and memory names — Tuesday's leadership group after Rosenblatt's Street-high $2,400 price target on SanDisk — gave back some of that rally: the Philadelphia Semiconductor Index fell over 1% (Sina Finance, 21st Century Business), with SK Hynix, SanDisk, and Intel all down more than 2% and ARM, Micron, Qualcomm, AMD, and Marvell down more than 1%. Meta was a standout gainer (+1.01% per Twelve Data; see Portfolio read) heading into its two-day Connect conference, where the company is expected to showcase its "Muse" AI agent and reportedly unveil camera-free "Luna" smart glasses. Popular China-linked ADRs sold off sharply — Alibaba fell nearly 4–4.75% (Twelve Data/wire estimates agree closely), with Baidu, Xiaomi, Tencent and others down 2–4%, ahead of Thursday's Trump-Xi summit.

| Sector | ETF | 1D |
|---|---|---|
| Energy | XLE | +0.99% |
| Industrials | XLI | -0.11% |
| Financials | XLF | -0.47% |
| Technology | XLK | -0.47% |
| Materials | XLB | -0.49% |
| Consumer Staples | XLP | -0.36% |
| Communication Services | XLC | -0.85% |
| Health Care | XLV | -0.64% |
| Real Estate | XLRE | -1.55% |
| Consumer Discretionary | XLY | -1.50% |
| **Utilities** | **XLU** | **-1.92%** |

Energy was the sole gaining sector, a direct mirror of the oil move. Utilities and real estate — the most rate-sensitive equity sectors — led decliners, consistent with the yield spike being the day's dominant mechanism. Financials (-0.47%) were more modestly negative today after being the prior session's worst performer.

### Rest of world: broadly lower, South Korea the outlier decliner

*Source: Bigdata.com market tearsheet (FMP), country-ETF proxies.*

| Country | ETF | 1D |
|---|---|---|
| South Korea | EWY | -3.62% |
| South Africa | EZA | -3.92% |
| Australia | EWA | -2.51% |
| Taiwan | EWT | -2.27% |
| China | MCHI | -1.99% |
| Hong Kong | EWH | -1.88% |
| Japan | EWJ | -1.75% |
| Germany | EWG | -1.83% |
| UK | EWU | -1.22% |

Nearly every major market fell alongside the US on the same global bond-yield repricing (Eurozone and UK gilts moved in sympathy with Treasuries, MT Newswires). South Korea's EWY was the day's largest single-day mover despite the underlying KOSPI index itself only falling modestly (+0.90% in local terms per the tearsheet's index table, a genuine ETF-vs-index divergence not resolved in this run's searches) — South Korea and Taiwan remain the largest cumulative gainers over the past year (EWY +127.93% 1Y, EWT +74.99% 1Y) on the semiconductor/AI trade flagged in prior reports.

---

## Commodities

### Energy — oil snaps a five-day losing streak; see the trigger section for the Hormuz attack and diesel-ban story

| Commodity | Price | 1D |
|---|---|---|
| Crude Oil (WTI) | $92.16 | +1.81% |
| Brent Crude Oil | $103.46 | +4.24% |
| Natural Gas (Henry Hub) | $3.17 | +1.80% |
| Gasoline RBOB | $3.35 | +3.91% |
| Heating Oil | $4.69 | -1.57% |

**Minor sourcing note:** Alliance News's New York close snapshot has WTI easing intraday from an elevated Tuesday reference ($95.21) to $92.54, while most other wires (CNBC, MT Newswires) describe WTI as *rising* today from Tuesday's ~$89–90 settle — the discrepancy looks like a difference in which Tuesday print each outlet is using as the base, not a live disagreement on today's level; the tearsheet's $92.16 is corroborated independently by CNBC's cited settle of the same figure.

### Metals — broad decline on the stronger dollar and higher yields

| Metal | Price | 1D |
|---|---|---|
| Gold Futures | $4,318.40 | -1.33% |
| Silver Futures | $64.96 | -2.35% |
| Platinum | $1,748.60 | -4.21% |
| Palladium | $1,269.50 | -2.79% |
| Copper | $6.79/lb | -0.64% |

Spot gold broke below $4,300/oz intraday (Eastmoney citing London spot: $4,299.92, -1.4%) before recovering slightly into the settle. FXStreet's headline captures the mechanism cleanly: "Gold buckles as 5% yields and Fed hawks take control." Silver underperformed gold on the day (as it typically does, given its larger industrial-demand component and lower liquidity) despite the OECD's same-day upward revision to global growth forecasts, which should be constructive for industrial metals demand over time. ECB Governing Council member Joachim Nagel's hawkish comments on Eurozone rates compounded the global rate-hike repricing.

### Agricultural

*Source: Bigdata.com tearsheet only — no dedicated search run today given the three larger cross-asset stories (rates/PMI, oil, crypto) took priority under the one-theme-per-search discipline.*

**Feeder Cattle (+1.86%)**, **Live Cattle (+1.32%)**, and **Rough Rice (+1.87%)** were the largest agricultural gainers; **Lean Hogs (-0.95%, and -9.96% 5D)** and **Corn (-1.49%)** the largest decliners. No catalysts identified this run.

---

## Crypto

*Source: 9 of 15 watchlist pairs from the Bigdata.com tearsheet (as of ~9:45 PM UTC); 6 pairs (ZEC, XLM, BCH, HBAR, SUI, SHIB) from Alpha Vantage `DIGITAL_CURRENCY_DAILY`, whose daily print reflects a UTC-midnight-to-UTC-midnight close and may not align exactly with the tearsheet's later intraday snapshot — a genuine timing difference given crypto trades 24/7, flagged rather than blended silently.*

| Asset | Price | 1D | Source |
|---|---|---|---|
| Bitcoin (BTC) | $84,493.14 | -1.97% | Bigdata.com tearsheet |
| Ethereum (ETH) | $2,678.00 | -2.73% | Bigdata.com tearsheet |
| XRP | $1.50 | -4.45% | Bigdata.com tearsheet |
| Solana (SOL) | $114.63 | -3.28% | Bigdata.com tearsheet |
| **Dogecoin (DOGE)** | **$0.09** | **-7.66%** | Bigdata.com tearsheet |
| **Avalanche (AVAX)** | **$10.37** | **-8.16%** | Bigdata.com tearsheet |
| **Cardano (ADA)** | **$0.24** | **-6.19%** | Bigdata.com tearsheet |
| **Chainlink (LINK)** | **$12.30** | **-5.65%** | Bigdata.com tearsheet |
| Litecoin (LTC) | $61.91 | -1.55% | Bigdata.com tearsheet |
| Zcash (ZEC) | $1,617.72 | -0.74% (vs. prior day's close $1,629.81) | Alpha Vantage |
| Stellar (XLM) | $0.21716 | +0.42% (vs. $0.21626) | Alpha Vantage |
| Bitcoin Cash (BCH) | $343.99 | -0.29% (vs. $345.00) | Alpha Vantage |
| Hedera (HBAR) | $0.09864 | -0.45% (vs. $0.09909) | Alpha Vantage |
| Sui (SUI) | $1.0267 | +0.24% (vs. $1.0242) | Alpha Vantage |
| Shiba Inu (SHIB) | $0.00000612 | +0.16% (vs. $0.00000611) | Alpha Vantage |

**Bold = breached the watchlist's 5% alert threshold: DOGE, AVAX, ADA, LINK.**

Today's decline is a pullback from an extended run, not a fresh negative catalyst on crypto specifically: Bitcoin and Ethereum both surged into a short squeeze on September 21 (BTC hit $87,397 intraday, an 8-month high, on roughly $647.9–800 million in 24-hour short liquidations per CoinGlass/AOL.com, plus a record $999 million in single-day US spot Bitcoin ETF inflows), so today's move is largely an unwind of that overbought spike, amplified by the same 10-year-yield-to-19-year-high mechanism driving the broader risk-off tape (Crypto Briefing explicitly linked the two: "10-year Treasury yield hits new high, pressures tech stocks and Bitcoin markets"). The higher-beta alts that rallied hardest into the squeeze (AVAX, DOGE, ADA, LINK) gave back the most today — consistent with a mean-reversion dynamic rather than four separate catalysts; this run's searches did not surface a distinct, asset-specific news story for any of the four breaching names beyond the broad macro/positioning unwind already covered.

---

## Portfolio read (`analyst/watchlist.yaml`)

*Twelve Data `get_quote` calls, paced in small batches to stay under the connector's 8-credit/minute cap. Coverage: 21 of 21 GEXC names, 2 of 14 MOVERS names, 1 of 1 QQQ proxy. Crypto book: see Crypto section above (15 of 15, via Bigdata.com + Alpha Vantage). See Connector status for why the MOVERS book is materially incomplete.*

### GEXC options-flow book (21 names, 3% threshold) — 21 of 21 retrieved, 5 breached

| Symbol | 1D | Symbol | 1D |
|---|---|---|---|
| AAPL | -0.82% | MSFT | +0.56% |
| AMD | -1.42% | MU | -2.26% |
| AMZN | -2.21% | NFLX | -1.09% |
| AVGO | -2.61% | NOK | -1.76% |
| **BABA** | **-4.75%** | **ORCL** | **-3.14%** |
| BAC | -0.34% | PFE | +0.84% |
| **GOOG** | **-3.58%** | **PLTR** | **+3.67%** |
| **GOOGL** | **-3.79%** | TSLA | +0.35% |
| HOOD | -1.24% | TSM | -1.18% |
| INTC | -1.02% | NVDA | -1.47% |
| META | +1.01% | | |

Bold = breached the 3% threshold (5 of 21):
- **BABA -4.75%** — the book's largest single-name decline, consistent with the broad China-ADR selloff (Baidu, Tencent, Xiaomi all down 2–4%) heading into Thursday's Trump-Xi summit; no company-specific catalyst surfaced.
- **GOOG -3.58% / GOOGL -3.79%** — both share classes breached; no Alphabet-specific news surfaced this run, consistent with the broad tech/growth pullback on the rate move (both Nasdaq indexes underperformed the S&P today).
- **ORCL -3.14%** — no company-specific catalyst surfaced; consistent with the broader software/growth-multiple compression on higher yields.
- **PLTR +3.67%** — the book's only gainer past threshold; no distinct same-day catalyst surfaced in this run's searches.
- **META +1.01%** — did not breach, but notable given the stock's outsized recent moves (it was reportedly up ~3.3% intraday per Chinese-language wire coverage before settling lower into the close) around today's opening session of Meta Connect.

### MOVERS bot daily picks (14 names, 4% threshold) — 2 of 14 retrieved, 1 breached

Today's rotation: SNDK, CHPT, AGCO, NRG, SOXL, MRVL, CEG, KLAC, RIOT, STX, KNX, FOUR, ENTG, VST.

| Symbol | 1D |
|---|---|
| SNDK | -3.77% |
| **CHPT** | **-6.40%** |

- **CHPT (ChargePoint) -6.40%** breached the threshold; no distinct same-day catalyst surfaced in this run's searches.
- **SNDK -3.77%** — just short of the 4% threshold; this is a partial giveback of Tuesday's +6.82% rally on Rosenblatt Securities' Street-high $2,400 price-target initiation (Kevin Cassidy, Buy rating), consistent with the broader memory/semiconductor pullback described in the Equities section.
- **12 names not retrieved this run** (AGCO, NRG, SOXL, MRVL, CEG, KLAC, RIOT, STX, KNX, FOUR, ENTG, VST) — Twelve Data's per-minute cap did not clear reliably despite repeated waits; not filled from general knowledge or wire commentary.

### Index proxies (2% threshold) — 3 of 3 retrieved, none breached

| Symbol | 1D | Source |
|---|---|---|
| $SPX | -0.76% | Bigdata.com tearsheet |
| SPY | -0.72% | Bigdata.com tearsheet |
| QQQ | -0.84% | Twelve Data |

All three index proxies moved together and stayed well under threshold, consistent with the broad-based (rather than single-name-driven) nature of today's selloff.

### Crypto book (15 names, 5% threshold) — 15 of 15 retrieved, 4 breached

See the Crypto section above for full detail, prices, and sourcing. **DOGE (-7.66%), AVAX (-8.16%), ADA (-6.19%), and LINK (-5.65%) breached the 5% threshold** — all four are part of the broad post-short-squeeze unwind described above, not individually distinct news events per this run's searches.

---

## Portfolio summary: 10 of 53 tracked positions breached their alert threshold today; 41 of 53 have confirmed data

Of the 53 tracked positions, **41 returned live data this run** (21 GEXC + 2 MOVERS + 3 index proxies + 15 crypto), and **10 of those 41 breached their threshold**: BABA, GOOG, GOOGL, ORCL, PLTR (GEXC book, 3%), CHPT (MOVERS, 4%), and DOGE, AVAX, ADA, LINK (crypto, 5%). The remaining **12 positions (the bulk of the MOVERS book)** have no data this run due to the Twelve Data connector degradation detailed below — this should not be read as "no notable moves" for those names, since the same connector issue that blocked their retrieval means today's move for AGCO, NRG, SOXL, MRVL, CEG, KLAC, RIOT, STX, KNX, FOUR, ENTG, and VST is simply unknown from this run.

---

## Risks to watch

- **October 27–28 FOMC meeting** — markets now price 69–73% odds of a second consecutive 25bp hike, up sharply from 55% just one day ago; watch upcoming jobless-claims data (due tomorrow) and any further Fed-official commentary for confirmation or reversal of that repricing.
- **The Strait of Hormuz attack on MV Cape Dao** and whether it represents an isolated incident or a renewed escalation — this is the same waterway where a Saudi pipeline was attacked September 13 and where "near-daily attacks" have continued per multiple wires even as transit volumes have risen.
- **The US diesel export ban decision**, expected within days per Politico's sourcing — the White House has disputed the report, but if implemented, oil-industry analysts (Rapidan Energy, GasBuddy) warn it would likely raise, not lower, US fuel prices after an initial Gulf Coast-only dip, and could invite European retaliation on gasoline exports to the US.
- **Thursday's Trump-Xi summit** — expectations are low for a major breakthrough (Bank of America's base case is a one-year extension of the existing trade truce, expiring November 10), but AI-dialogue and rare-earths headlines could move markets either direction.
- **The Citigroup Earnings Revision Index turned net negative this week for the first time in 23 weeks** (Bloomberg, via MSN) — SentimentTrader's historical analysis cited in that report flags this as a leading indicator that realized S&P 500 earnings tend to soften one to two quarters after the revision cycle turns; separately, Morgan Stanley's Michael Wilson has floated a scenario where the S&P 500 falls as much as 7% if energy prices keep rising alongside bond-market volatility.
- **This portfolio read is missing 12 of 53 positions** (the bulk of the MOVERS book) due to the Twelve Data connector issue below — prioritize this book on the next monitoring pass once the connector clears.
- **The crypto book's four threshold breaches (DOGE, AVAX, ADA, LINK) are a positioning unwind, not a new negative catalyst** — worth confirming on the next pass whether the pullback stabilizes or extends, particularly if Treasury yields continue higher.

---

## Connector status this run

All five of the fund's named connectors (Bigdata.com, Twelve Data, Alpha Vantage, Blockscout, Quartr) were confirmed available as callable tools this session.

- **Twelve Data: materially degraded, consistent with the failure pattern first flagged in the September 22 report.** The documented 8-credit/minute cap was hit repeatedly, and unlike a clean per-minute reset, the "credits used" counter frequently continued climbing across consecutive attempts even after multi-minute waits with zero intervening calls (observed sequences like 9→24 credits used across a single extended wait), suggesting the per-minute window is not resetting reliably this session — the same anomaly documented on 9/22. This consumed a large share of this session's time and ultimately left 12 of the 14 MOVERS-book names unpulled. Batched/comma-separated `get_price` requests are also still rejected outright ("does not support CSV format"), consistent with every prior report since 9/14; all equity pulls this run used single-symbol `get_quote` calls. Despite the degradation, full coverage was eventually achieved for the 21-name GEXC book and QQQ by pacing single calls with waits between batches.
- **Alpha Vantage:** `TREASURY_YIELD` remains stale (most recent print September 21, two calendar days behind), continuing the pattern flagged since 9/14. `DIGITAL_CURRENCY_DAILY` performed well this run — all 6 requested pairs (ZEC, XLM, BCH, HBAR, SUI, SHIB) succeeded after two initial per-second (not daily-cap) rate-limit errors cleared with brief spacing between calls; no daily-cap issue was hit this run.
- **Bigdata.com:** no failures this run — the most reliable connector again, and the sole source for the full cross-asset macro wrap, 9 of 15 crypto pairs, and all the day's narrative/causal-chain sourcing.
- **Blockscout and Quartr:** confirmed available as callable tools this session but not invoked — no on-chain or filing-level question came up in today's research.

No data point in this report was filled in from general training knowledge in place of a failed or gated connector call. Items reported without an attributed cause because no distinct catalyst surfaced in this run's searches: BABA/GOOG/GOOGL/ORCL/PLTR's individual moves beyond the broad macro pullback, CHPT's -6.40% move, and the four crypto breaches beyond the broad positioning-unwind explanation. Items with no data at all this run, stated explicitly rather than estimated: AGCO, NRG, SOXL, MRVL, CEG, KLAC, RIOT, STX, KNX, FOUR, ENTG, and VST (12 of the MOVERS book's 14 names).

---

## Sources

Market levels and cross-asset data: [Bigdata.com](https://bigdata.com) market tearsheet (sourced from FMP), as of ~8:00–9:45 PM UTC, September 23, 2026. Individual equity quotes: Twelve Data `get_quote` (real-time, per-symbol calls). Crypto pairs not carried by the tearsheet: Alpha Vantage `DIGITAL_CURRENCY_DAILY` (ZEC, XLM, BCH, HBAR, SUI, SHIB). Treasury-yield freshness check: Alpha Vantage `TREASURY_YIELD` (found stale, most recent print September 21). News, causal narrative, and analyst commentary: Bigdata.com news search, aggregating MT Newswires (Global Energy and general), CNBC.com, CNBC Pro, CNBC Arabia, CNN, FXStreet News, Nasdaq/RTTNews/Barchart, Yahoo! Finance, AOL.com, MSN, The Washington Post, Politico, Fox News, Reuters (via multiple wires), Yonhap News, Nikkei Japan, Sina/Sina Finance, 21st Century Business, Eastmoney, Chinatimes, AlMonitor, gCaptain, Business Standard, Crypto Briefing, Crypto Wire, The Cryptonomist, and others, all published September 23, 2026. Watchlist: `analyst/watchlist.yaml`.
