# Global Markets Wrap — September 16, 2026

*Compiled from Bigdata.com (market tearsheet + news search), Twelve Data, and Alpha Vantage. Blockscout and Quartr were reachable this session but not needed — no on-chain or filing-level question came up. Cross-asset levels from the Bigdata.com/FMP tearsheet as of ~8:00–9:35 PM UTC, September 16, 2026, unless a specific timestamp is given. This is a draft for human review, not a trade recommendation — see `analyst/GUARDRAILS.md`.*

## TL;DR

Three separate stories, one of them a scheduled catalyst, drove the session:

1. **The Fed hiked for the first time since July 2023 — and the market didn't like the tone.** The FOMC raised the federal funds rate 25bp to 3.75%–4.00%, a unanimous 12–0 vote. The dot plot showed 16 of 18 participants expecting at least one more hike this year (median year-end 2026 fed funds projection 4.1%, up from June's 3.8%), with inflation seen at 3.7% by year-end and not reaching 2% until 2029. Stocks were green heading into the 2:00 PM ET decision; Chair Kevin Warsh's hawkish press conference reversed that — the Dow fell as much as 631 points intraday and closed **-1.21%**, the 2-year Treasury yield jumped over 7bp, and gold swung from an intraday gain of as much as +1.7% to a loss of -1.3% before settling roughly flat-to-up on the day depending on the snapshot (see Precious Metals).
2. **Oil reversed sharply**, giving back most of the prior two days' spike after Saudi Arabia moved to route additional crude to Asian refiners via ship-to-ship transfers off Oman's Sohar port — bypassing the drone-damaged East-West pipeline — and the U.S. Energy Secretary said the pipeline could resume "within days." WTI fell **-3.21%** to $102.43, Brent **-2.91%** to $105.58, unwinding part of this week's Middle-East-driven rally.
3. **A "black swan" liquidity event hit Turkey**, unrelated to the Fed or oil: the Borsa Istanbul BIST 100 fell as much as 6% intraday and triggered a market-wide circuit breaker after asset manager Pusula Portföy failed to meet fund redemption requests, sparking a broader run (investors pulled a net 55 billion lira, ~$1.13B, from Turkish funds Wednesday). The lira itself barely moved (<0.1%), so this reads as an idiosyncratic fund-liquidity event rather than a sovereign-risk repricing — but it shows up starkly in the tearsheet: Turkey (TUR) **-6.61%** 1D, **-10.53%** 5D, the single worst mover on the entire country-ETF board.

A fourth, smaller thread worth flagging for the crypto book: **Zcash (ZEC) surged 18–20%** against a broadly soft crypto tape, on a governance vote, an ETF launch, and a short squeeze (see Crypto).

**Note on context:** this is the Fed's first rate *hike* in over three years, not a cut — the macro backdrop remains the energy-shock/inflation story that has run through this week's reports, and the dot plot leans toward more tightening, not less.

---

## Thread 1: FOMC hikes 25bp, hawkish Warsh press conference triggers risk-off reversal

*Source: CNBC.com, Benzinga, Alliance News, FXStreet News, Yahoo! Finance, FOX Business, Livemint (Bloomberg), all September 16, 2026.*

The Federal Open Market Committee raised the federal funds target range 25 basis points to 3.75%–4.00% — the first hike since July 2023 and the Fed's first rate change of any kind since December 2025. The vote was unanimous (12-0), which surprised some market participants who had expected at least one dissent (speculation had centered on Governor Christopher Waller).

The Summary of Economic Projections carried a hawkish edge: 16 of 18 participants see at least one more hike in 2026 (median year-end fed funds projection 4.1%, up from 3.8% in June), core PCE inflation is projected at 3.4% in 2026 and isn't seen hitting the Fed's 2% target until 2029, and GDP growth expectations were nudged up to 2.3% for 2026. Warsh again declined to submit his own dot-plot projection, as he did in June.

The post-meeting statement ran a terse 130 words — even shorter than July's — and Warsh's press conference lasted roughly 22 minutes. In it, he called the decision the "right" one, said monetary conditions were "not restrictive enough," and stated the Fed had merely "removed a dose of accommodation." He also deflected questions about pressure from President Trump (who has been pushing publicly for cuts), saying: "Independence is a two-way street."

**Market reaction:** Stocks were up modestly ahead of the 2:00 PM ET decision (S&P +0.2–0.3%). The reaction flipped hard after Warsh's remarks — the Dow fell as much as 631 points intraday and closed the session down **-1.21%** (51,461.90), while the S&P 500 (**-0.45%**, 7,551.81) and Nasdaq Composite (**-0.01%**, 25,978.42) held up better, cushioned by a chip-stock rally that started well before the Fed decision (see Equities). The 2-year Treasury yield — the maturity most sensitive to Fed policy — jumped more than 7bp to its highest level since July 2024. CNBC called the reaction "reminiscent of the July FOMC meeting," the prior time Warsh's press conference rattled markets.

| Maturity | Yield | 1D change* |
|---|---|---|
| 1 Month | 3.96% | +0.76% |
| 3 Month | 4.14% | +0.73% |
| 6 Month | 4.22% | +1.20% |
| 1 Year | 4.45% | +1.37% |
| 2 Year | 4.74% | +1.50% |
| 5 Year | 4.86% | +0.62% |
| 10 Year | 5.01% | +0.20% |
| 20 Year | 5.39% | -0.19% |
| 30 Year | 5.35% | -0.19% |

*("1D change" is the relative change in the yield level per the Bigdata.com/FMP tearsheet, not basis points.)*

**Freshness cross-check:** Alpha Vantage's `TREASURY_YIELD` daily series is stale again — most recent print dated September 14 (10-year at 4.97%), two days behind today's session, continuing the same staleness pattern flagged on 9/14 and 9/15. Not used as a same-day cross-check; the Bigdata.com/FMP tearsheet and multiple news-wire snapshots were used instead.

---

## Thread 2: Oil reverses sharply as Saudi Arabia eases supply fears

*Source: CNBC.com, Reuters (via AOL.com), FXStreet News, MT Newswires - Global Energy, Nasdaq, Nikkei Japan, Financial News, all September 16, 2026.*

Crude gave back a large chunk of the prior two sessions' Middle-East-driven rally after reports (Bloomberg, Reuters) that Saudi Arabia is routing additional crude to Asian refiners through ship-to-ship transfers off Oman's Sohar port — a workaround for the East-West pipeline shut down by last week's drone attack. U.S. Energy Secretary Chris Wright told CNBC the pipeline outage was a "brief and temporary interruption" that would be "measured in days," and Saudi Aramco is reportedly working to restore roughly half the pipeline's capacity within days (full repair still estimated at up to six weeks by regional officials and Kpler). A smaller-than-expected EIA inventory draw (-600,000 bbl vs. a consensus estimate near -1.5M bbl) added to the bearish pressure, and an API report the day before had shown a surprise 7.1-million-barrel build.

| Commodity | Price | 1D | 5D | 1M | YTD |
|---|---|---|---|---|---|
| WTI Crude (CLUSD) | $102.43 | **-3.21%** | +2.38% | +21.22% | +77.61% |
| Brent Crude (BZUSD) | $105.58 | **-2.91%** | +0.93% | +16.19% | +72.74% |
| Natural Gas | $2.89 | -0.96% | +2.12% | +7.47% | -20.07% |
| Gasoline RBOB | $3.24 | -0.21% | -2.05% | -0.94% | +88.66% |
| Heating Oil | $4.99 | -0.45% | +0.57% | +12.40% | +133.76% |

*Source: Bigdata.com/FMP tearsheet, ~9:35 PM UTC. News-wire snapshots through the day show WTI settling in a $101.72–$102.43 range and Brent in $105.12–$105.83 across different reporting times — consistent with normal intraday movement, not a data conflict.*

Crude is still up sharply on the month (WTI +21%, Brent +16%) — this is a partial reversal of the spike, not a return to pre-crisis levels. Kpler estimates Saudi crude exports could still fall by 3.5–4 million bpd if the pipeline outage extends, and Goldman Sachs' scenario range remains wide: $80/bbl if exports normalize vs. $120/bbl if attacks on shipping intensify.

---

## Thread 3: Turkish stock market crashes on asset-manager liquidity default

*Source: Bne IntelliNews, MSN, Yahoo! Finance Japan, Finwire, Sina, 21st Century Business, all September 16, 2026.*

The Borsa Istanbul BIST 100 index fell as much as **6% intraday**, triggering a market-wide circuit breaker — extending a two-day decline that MSN and Bne IntelliNews describe as potentially the index's worst two-day drop since March 2025. The trigger: asset manager Pusula Portföy announced Tuesday that some of its investment and money-market funds could not meet redemption requests. The resulting confidence shock spread into a broader run — Fintables data shows a net 55 billion lira (~$1.13B) pulled from Turkish investment funds Wednesday alone, with Tera Portföy (in the process of acquiring Pusula's related businesses, but stating it bears no responsibility for the defaults) seeing ~32 billion lira in outflows and Pusula-managed funds ~9.6 billion lira. Pusula's cumulative outflows since August 28 total an estimated 129–132 billion lira (~$2.7B). The Turkish banking index fell 7.7% at the worst of the selloff; only two BIST 100 constituents rose.

Importantly, this looks like a **contained, idiosyncratic liquidity event rather than a currency or sovereign-credit crisis**: the lira weakened less than 0.1% against the dollar (tearsheet USD/TRY +0.04% 1D), though 2-year and 10-year Turkish government bond yields rose 76bp and 61bp respectively and 5-year CDS widened 7bp to 237bp. A Turkiye Is Bankasi strategist framed it as contained "unless liquidity issues spread significantly beyond the fund management industry." The root cause cited by multiple sources: a Turkish Capital Markets Board tightening of investment-fund rules in late August (restricting concentration in illiquid stocks) collided with some funds' existing strategy of holding large, illiquid positions — Pusula's own listed vehicle KTLEV had reportedly returned +1,599% y/y before today's collapse.

| Country ETF | 1D | 5D | 1M |
|---|---|---|---|
| Turkey (TUR) | **-6.61%** | **-10.53%** | -8.24% |

*Source: Bigdata.com/FMP tearsheet. No other country ETF in the board moved more than -2% 1D, underscoring how idiosyncratic this move is.*

---

## Equities — US indexes and sectors

*Source: Bigdata.com market tearsheet (FMP), as of ~8:59 PM UTC.*

| Index | Level | 1D |
|---|---|---|
| S&P 500 | 7,551.81 | -0.45% |
| Dow Jones Industrial Avg | 51,461.90 | **-1.21%** |
| NASDAQ Composite | 25,978.42 | -0.01% |
| NASDAQ 100 | 28,945.06 | +0.02% |
| Russell 2000 | 2,858.81 | -0.40% |
| CBOE Volatility Index (VIX) | 17.71 | +2.97% |

The Dow was the laggard, weighed down by rate-sensitive financials and industrials; the Nasdaq was roughly flat as a chip-stock rally offset the broader hawkish-Fed selloff. VIX is up nearly 17% over the past month but remains in a historically unremarkable range (17.71).

**Sector table:**

| Sector | ETF | 1D |
|---|---|---|
| Health Care | XLV | +0.07% |
| Technology | XLK | +0.10% |
| Utilities | XLU | +0.00% |
| Industrials | XLI | -0.08% |
| Consumer Staples | XLP | -0.48% |
| Real Estate | XLRE | -0.60% |
| Materials | XLB | -0.73% |
| Consumer Discretionary | XLY | -0.63% |
| Communication Services | XLC | -0.90% |
| Financials | XLF | **-1.62%** |
| Energy | XLE | **-2.88%** |

Energy led the sector losers, tracking crude's reversal (Thread 2). Financials lagged on rate-hike-driven margin/credit anxiety. Technology and Health Care were the only sectors to close green.

**Chip stocks rallied intraday, a partial counter-current:** Ahead of and during the Fed decision, semiconductor names broadly rose on a specific catalyst — reports that SK Hynix is in talks with Intel about producing memory chips in the U.S. (potentially leasing part of Intel's Ohio facility or forming a joint venture). Intel led with a premarket pop as high as +7% before settling **+3.99%** on the day (per Twelve Data), with the Philadelphia Semiconductor Index (SOX) closing +0.63%, outperforming the Dow (-1.21%) and S&P (-0.45%). SK Hynix later said in an evening statement there are "no definitive plans" yet. This follows Monday's AI-slowdown-driven chip selloff (tied to Anthropic CEO Dario Amodei's call to slow frontier AI development) and Tuesday's partial rebound after Broadcom's CEO pushed back on AI-capex-pullback fears — this week's chip trade continues to be driven by name-specific news more than the macro backdrop.

**Oracle (ORCL)** continued to stabilize after last week's six-day, ~13.6% slide: shares closed **+2.03%** at $143.20 (per Twelve Data), building on a Wednesday-morning bounce (Benzinga: +1.71% at $142.75 mid-morning) as investors weighed the company's $664B cloud backlog against its debt load ($125B) and negative free cash flow (-$5.4B last quarter). Wall Street remains split: Mizuho ($320 target, Outperform) and UBS ($250) vs. Stifel ($200) and Freedom Broker ($205), with consensus still Strong Buy (mean target $251.77).

---

## Crypto

*Source: Bigdata.com tearsheet and news search; Twelve Data `get_quote` for pairs not carried by the tearsheet.*

The broad crypto book was little-changed to modestly higher on the day — a contrast with Tuesday's CLARITY Act-driven selloff — but one name stood out sharply.

**Zcash (ZEC) surged 18–20%**, the single biggest cross-asset move of the day outside Turkish equities. Multiple snapshots through the session put the gain between +10% (early) and +20.46% (BTCManager, intraday high $1,385, up from an $1,110 open) depending on timing; Twelve Data's ~9:38 PM UTC quote shows **+18.22%** to $1,312.71. Three catalysts converged: (1) Zcash's NU7 governance vote closed with 99.9% approval (2.4M ZEC voting) to cut block time from 75 to 25 seconds while keeping the existing halving schedule; (2) Grayscale's spot Zcash ETF (ticker ZCSH), launched August 25, has pulled in over $463M in assets; (3) the rally forced roughly $45M in short-position liquidations, creating a self-reinforcing squeeze. ZEC is now the ninth-largest crypto by market cap (~$21–22B) and up over 2,300% year-over-year — a move analysts describe as a private-money/institutional-comfort story (ETF approval for a privacy coin) rather than a broad-market signal.

| Asset | Price | 1D | Source |
|---|---|---|---|
| Bitcoin (BTC) | $75,997.88 | +0.54% | Bigdata.com tearsheet |
| Ethereum (ETH) | $2,403.22 | +0.23% | Bigdata.com tearsheet |
| XRP | $1.29 | +0.56% | Bigdata.com tearsheet |
| Solana (SOL) | $98.27 | +1.44% | Bigdata.com tearsheet |
| Dogecoin (DOGE) | $0.08 | +0.41% | Bigdata.com tearsheet |
| **Zcash (ZEC)** | **$1,312.71** | **+18.22%** | Twelve Data |
| Chainlink (LINK) | $10.92 | +0.26% | Bigdata.com tearsheet |
| Cardano (ADA) | $0.19 | -0.43% | Bigdata.com tearsheet |
| Stellar (XLM) | $0.181 | +2.78% | Twelve Data |
| Bitcoin Cash (BCH) | $218.40 | +0.74% | Twelve Data |
| Litecoin (LTC) | $51.20 | -0.10% | Bigdata.com tearsheet |
| Hedera (HBAR) | $0.0733 | -1.41% | Twelve Data |
| Sui (SUI) | $0.7067 | +2.88% | Twelve Data |
| Avalanche (AVAX) | $7.38 | +1.48% | Bigdata.com tearsheet |
| Shiba Inu (SHIB) | $0.00000489 | -1.21% | Twelve Data |

Bitcoin remains under a broader macro cloud: spot BTC ETFs saw $450M in net outflows Tuesday (their largest single-day withdrawal since June 25, per SoSoValue), and BTC briefly dipped as low as $74,913 intraday before recovering. Bernstein said SEC/CFTC rulemaking is now expected to move "aggressive and swift" to partially fill the regulatory gap left by the CLARITY Act's Tuesday defeat.

---

## Precious Metals — a whipsaw session

*Source: FXStreet News, Livemint (Bloomberg), Nikkei Japan, Emirates News Agency (WAM), all September 16, 2026.*

Gold had an unusually two-sided day, and the numbers below depend heavily on snapshot timing — flagged explicitly rather than picked arbitrarily:

| Metal | Price | 1D | Snapshot |
|---|---|---|---|
| Gold Futures (GCUSD, COMEX settle) | $4,387.50 | **+1.26%** | Bigdata.com/FMP tearsheet, ~9:35 PM UTC (matches Nikkei's reported COMEX settle of $4,387.5, +1.3%) |
| Spot gold (XAU/USD), post-press-conference | ~$4,262 | n/a | FXStreet, 7:43 PM UTC |
| Spot gold, after-hours low | ~$4,273 | n/a | Nikkei, evening ET |

Gold rallied as much as +1.7% intraday as oil and yields fell ahead of the Fed decision (a "flight to the safe non-yielding asset" read), then reversed to a loss of as much as -1.3% after Warsh's hawkish press conference reaffirmed the inflation threat and the dot plot showed another 2026 hike — "a hawkish hike hits gold through a stronger dollar and higher real yields," per Brown Brothers Harriman's Elias Haddad. The COMEX futures settlement (which the tearsheet reflects) appears to have printed before the post-presser reversal fully played out; spot continued trading lower into the evening. Silver, by contrast, rose modestly through the session (MT Newswires: silver futures +0.6% to $66.46 as of its ~9 PM UTC snapshot) even as gold gave back its gains — an unusual divergence within the metals complex worth watching, not explained in the sourcing gathered this run.

| Metal | Price | 1D |
|---|---|---|
| Gold Futures | $4,387.50 | +1.26% |
| Silver Futures | $63.42 | -0.68% |
| Platinum | $1,759.30 | -1.00% |
| Palladium | $1,285.50 | -1.31% |
| Copper | $6.51 | +1.02% |

*Source: Bigdata.com/FMP tearsheet, ~9:35 PM UTC — note this silver figure (-0.68%) differs from MT Newswires' intraday +0.6% read cited above; different snapshot times, not a data conflict we're resolving in either direction.*

---

## Portfolio read (`analyst/watchlist.yaml`)

**Coverage this run is incomplete on equities.** Twelve Data's documented per-minute credit cap (8 credits/minute, per `CONNECTORS.md`) did not clear reliably this session — after the first successful batch, subsequent batches failed even after real-time waits of up to ~10 minutes between attempts, a materially worse pattern than the 9/14–9/15 sessions. We got quotes for **18 of 21 GEXC names** and **0 of 14 MOVERS names** before deciding further waiting had poor odds of finishing in reasonable time; see Connector status below. All 15 crypto positions and both liquid index proxies ($SPX, SPY) were covered via the Bigdata.com tearsheet plus Twelve Data.

**GEXC options-flow book (21 names, 3% threshold) — 18 of 21 quoted, 2 breached:**

| Symbol | 1D | Symbol | 1D | Symbol | 1D |
|---|---|---|---|---|---|
| AAPL | +0.35% | INTC | **+3.99%** | ORCL | +2.03% |
| AMD | +1.72% | META | +0.46% | PFE | *not priced* |
| AMZN | -1.04% | MSFT | -1.36% | PLTR | +1.03% |
| AVGO | +0.11% | MU | *not priced* | TSLA | +0.43% |
| BABA | -1.90% | NFLX | -1.90% | TSM | +1.00% |
| BAC | -2.74% | NOK | *not priced* | | |
| GOOG | -0.62% | NVDA | +0.82% | | |
| GOOGL | -0.62% | | | | |
| HOOD | **-5.46%** | | | | |

Bold = breached the 3% threshold.

**HOOD (Robinhood) -5.46%** — idiosyncratic, not primarily a crypto-market-sentiment move: the DOJ/SDNY charged two former Robinhood engineers (Hefu Chai, Huaisong Xiang) Tuesday with commodities and wire fraud, alleging they used confidential information about upcoming Robinhood Crypto listings to trade perpetual futures on Hyperliquid ahead of public announcements, netting over $50,000 each. AOL.com noted the "framing contrast" explicitly: Bitcoin's ETF proxy (IBIT) was down only ~0.6% and SPY was higher on the day, while HOOD fell 5%+ and peer Webull (BULL) fell 9% in sympathy — read as a broker-specific regulatory/reputational repricing, not a crypto-market one. This adds to Tuesday's CLARITY-Act-driven weakness (HOOD -3.4% that session).

**INTC (Intel) +3.99%** — Thread on chip-stock rally above: SK Hynix memory-chip production talks (Ohio facility), later tempered by SK Hynix's own "no definitive plans" statement.

**MU, NOK, PFE** — not priced this run; Twelve Data calls for these three did not clear the rate limit before we stopped retrying.

**MOVERS bot daily picks (14 names, 4% threshold) — not priced this run.** Today's rotation: SNDK, CHPT, AGCO, NRG, SOXL, MRVL, CEG, KLAC, RIOT, STX, KNX, FOUR, ENTG, VST. None of these 14 could be quoted before we stopped retrying Twelve Data — see Connector status. We are not fabricating moves or threshold calls for this book this run.

**Index proxies (2% threshold) — 2 of 3 covered, none breached:** $SPX -0.45% (index level, Bigdata.com tearsheet), SPY -0.44% (Bigdata.com tearsheet, Americas ETF table). QQQ was not directly quoted; the Nasdaq 100 index level (+0.02%) is a directional proxy only, not the ETF itself — noting the substitution rather than presenting it as QQQ's actual move.

**Crypto book (15 names, 5% threshold) — 15 of 15 quoted, 1 breached:** **ZEC +18.22%** (see Crypto thread above — governance vote, ETF inflows, short squeeze; unrelated to the rest of the book). All other 14 positions moved -1.4% to +2.9%, well inside threshold — no individual narrative warranted beyond the general Fed-hike-day tape.

---

## Risks to watch

- **Whether Warsh's hawkish tone at today's press conference — and the dot plot's lean toward a further 2026 hike — marks the start of a sustained tightening cycle**, which would be the key macro overhang across every asset class covered in this report.
- **The Saudi East-West pipeline's actual restart timeline.** Official U.S. messaging says "days"; independent estimates (Kpler, regional officials) still say three to six weeks. A confirmed restart delay would likely reverse today's oil pullback.
- **Whether the Turkish fund-liquidity stress stays contained to Pusula/Tera-linked vehicles** or spreads into the broader Turkish banking/bond complex — today's data (lira nearly flat, but yields and CDS widening) suggests contained-for-now, per local strategists.
- **Zcash's sustainability above $1,250–$1,300.** Multiple analysts flagged the $45M short-squeeze component as a risk indicator, not just a tailwind — a move that reverses as quickly as it built is explicitly on the table per the sourcing gathered.
- **Twelve Data's degraded reliability this session** (see Connector status) — if this persists into tomorrow's run, the watchlist-check playbook's equity coverage will need a documented fallback (e.g., batching fewer names per pass, or escalating the plan-tier question raised in `CONNECTORS.md`).

---

## Connector status this run

All five of the fund's named connectors (Bigdata.com, Twelve Data, Alpha Vantage, Blockscout, Quartr) were confirmed available as callable tools this session.

- **Twelve Data:** materially worse rate-limiting than the 9/14–9/15 sessions. The documented 8-credit/minute cap did not reliably clear even after real-time waits as long as ~10 minutes between retries — a single batch of 8 `get_quote` calls succeeded, then the next batch failed repeatedly across three separate waits (90s, 150s, 240s) before eventually succeeding, and this pattern repeated inconsistently through the run. We stopped retrying after covering 18 of 21 GEXC-book equities and all 15 crypto positions, leaving 3 GEXC names (MU, NOK, PFE), all 14 MOVERS-book names, and QQQ specifically unpriced this run rather than continue indefinitely. The batched comma-separated `get_price` call is still broken (confirmed again: "does not support CSV format" — same error documented on 9/14 and 9/15).
- **Alpha Vantage:** `TREASURY_YIELD`'s daily series remains stale (most recent value September 14, four+ days' pattern now across three consecutive reports). `REALTIME_BULK_QUOTES` was tried as a possible workaround for the Twelve Data gap and returned a premium-plan-required gate (consistent with `CONNECTORS.md`'s documented free-tier limits) — not used as a substitute.

No data point in this report was filled in from general training knowledge in place of a failed or gated connector call; unpriced watchlist positions are labeled as such rather than estimated.

---

## Sources

Market levels and cross-asset data: [Bigdata.com](https://bigdata.com) market tearsheet (sourced from FMP), as of ~8:00–9:41 PM UTC, September 16, 2026. Individual equity and crypto-pair quotes not carried by the tearsheet: Twelve Data `get_quote` (real-time, per-symbol calls, partial coverage — see Connector status). News, causal narrative, and analyst commentary: Bigdata.com news search, aggregating CNBC, Benzinga, Alliance News, FXStreet News, Yahoo! Finance, FOX Business, MT Newswires (Global Energy), Nasdaq, Nikkei Japan, Livemint (Bloomberg), Emirates News Agency (WAM), Bne IntelliNews, MSN, Yahoo! Finance Japan, Finwire, Sina, 21st Century Business, AOL.com (Reuters), Crypto Briefing, Crypto Wire, BTCManager, Bitcoin.com, Business Insider, Boursorama (Reuters), Arkansas Democrat-Gazette (AP), and Edgar SEC filings, all published or updated September 16, 2026. Treasury-yield freshness check: Alpha Vantage `TREASURY_YIELD` (found stale — see Connector status). Watchlist: `analyst/watchlist.yaml`.
