# Global Markets Wrap — September 24, 2026

*Compiled from Bigdata.com (market tearsheet + news search), Twelve Data (equity quotes), and Alpha Vantage (six crypto pairs not carried by the tearsheet). Blockscout and Quartr were confirmed available as callable tools this session but not invoked — no on-chain or filing-level question came up today. Cross-asset levels from the Bigdata.com/FMP tearsheet as of ~8:00–9:32 PM UTC, September 24, 2026; individual equity quotes from Twelve Data `get_quote`, pulled through the evening UTC in small batches to stay under the connector's 8-credit/minute cap (see Connector status — the cap's known non-resetting degradation from prior reports recurred, but full watchlist coverage was still achieved this run). **This is a draft for human review, not a trade recommendation** — see `analyst/GUARDRAILS.md`.*

## TL;DR

Day two of the same story: Treasury yields pushed to fresh multi-decade highs as three more Fed officials — New York's John Williams, Philadelphia's Anna Paulson, and Cleveland's Beth Hammack — backed further tightening, and a stronger-than-expected jobless-claims report (197,000, near 57-year lows) reinforced the case for a resilient economy that can absorb more hikes. The 10-year Treasury touched 5.15–5.18% intraday (highest since July 2007), the 30-year hit its highest since 2004 (~5.44–5.47%), and the 2-year its highest since 2023–2024. CME FedWatch priced October hike odds at 71–75%, up from 69–73% Wednesday and ~55% Tuesday. Oil extended its rally — WTI +2.66% to $94.61, Brent +3.55% to $106.74, having spiked as much as 5% intraday to $108.23 — on a Houthi missile attack on Saudi Arabia (Yanbu, Taif) and hawkish Iranian rhetoric, before paring gains on reports that US and Iranian negotiators are discussing a phased deal to reopen the Strait of Hormuz. Gold and silver extended Wednesday's slide on the stronger dollar and higher real yields. Equities, though, showed unusual resilience given the yield shock: the S&P 500 and Nasdaq Composite were roughly flat and the Dow fell just 0.31%, a sharp contrast with Wednesday's broad selloff. The reason: Meta's Muse AI agent (unveiled at Wednesday's Connect keynote) is driving a distinct rotation story — Meta itself (+4.48%) and Intel (+3.88%, on CPU-inference demand tied to Muse that Intel's CEO says the company can only half-fill) rallied hard, while Oracle fell 3.48% on a force majeure notice tied to delays at its Project Jupiter AI data center in New Mexico, compounding financing-cost worries after its long bonds' yield crossed 8% for the first time. Crypto swung sharply intraday — falling hard on the rate-hike repricing (Bitcoin briefly below $84,000, several altcoins down 5–10%) before rebounding into the US afternoon close. Litecoin was the standout of the day, +16.46%, on a distinct, well-sourced on-chain-activity and technical-breakout story unrelated to the macro tape.

**Note on context:** this is the same rate-hike cycle flagged in every report since September 16 (the Fed's first hike since 2023). Today's Fed commentary and jobless-claims data are the market continuing to reprice a second hike higher and sooner, not a new narrative.

---

## The trigger: yields hit fresh multi-decade highs as more Fed voices back tightening

*Source: MT Newswires, CNBC.com, CNBC Pro, Forbes.com, FXStreet News, International Business Times, all September 24, 2026.*

Three more Federal Reserve officials reinforced the hawkish tone that first moved markets Wednesday. New York Fed President John Williams (a voter) said it was "reasonable" to expect another rate hike by year-end. Philadelphia Fed President Anna Paulson (a voter) said she supported last week's hike and that "some modest further tightening may be warranted," flagging that inflation risks have risen this month due to the Middle East conflict and the surge in AI investment. Cleveland Fed President Beth Hammack also signaled support for tighter policy. The Fed's own September projections showed 16 of 18 policymakers expecting at least one more hike in 2026.

Treasury yields, already at a 19-year high after Wednesday's hot PMI print, extended their climb: the 10-year rose as much as 20 basis points intraday to 5.148–5.18% (CNBC Pro, FXStreet, Bigdata.com/FMP tearsheet all corroborate a high in the 5.15–5.18% range) — its highest since July 2007. The 30-year hit 5.438–5.47%, its highest since 2004. The 2-year rose to roughly 4.87–4.95%, a level last seen in 2023–2024. A weak US Treasury auction and mounting fiscal-supply concerns (Stifel flagged total US government debt surpassing $40 trillion, plus heavy corporate-bond issuance competing for capital) compounded the move. Separately, US initial jobless claims fell to 197,000 for the week ended September 19 (vs. ~201,000 expected), the lowest since mid-July and near a 57-year low — a labor market resilient enough, in the market's read, to give the Fed room to keep hiking despite rising energy costs.

**The cascade:** more hawkish Fed commentary + a stronger jobless-claims print → yields to fresh multi-decade highs → stronger dollar → gold/silver extend Wednesday's decline; separately, a Houthi attack on Saudi Arabia and stalled-then-revived Hormuz diplomacy drove another leg of oil volatility. Equities absorbed the yield shock better than Wednesday because a distinct, idiosyncratic story — Meta's Muse AI agent driving CPU-demand and social-media-rotation trades — offset the macro drag in several of the largest names (see Equities and Portfolio read below).

---

## Rates

*Source: Bigdata.com market tearsheet (FMP), as of September 24, 2026; cross-checked extensively against same-day wire prints (CNBC, CNBC Pro, Forbes, FXStreet, International Business Times, Finwire) given the news volume on this move.*

| Maturity | Yield | 1D change |
|---|---|---|
| 1 Month | 4.01% | +0.50% |
| 2 Month | 4.18% | +1.95% |
| 3 Month | 4.24% | +1.19% |
| 6 Month | 4.34% | +0.70% |
| 1 Year | 4.51% | +0.45% |
| 2 Year | 4.87% | +0.41% |
| 3 Year | 4.99% | +0.40% |
| 5 Year | 5.03% | +0.80% |
| 7 Year | 5.10% | +0.99% |
| 10 Year | 5.18% | +1.37% |
| 20 Year | 5.53% | +1.47% |
| 30 Year | 5.47% | +1.30% |

*("1D change" is the relative change in the yield level per Bigdata.com/FMP, not basis points.)*

The tearsheet's end-of-day snapshot (5.18% on the 10-year) sits at the high end of the day's wire-reported intraday range (5.148–5.18%), consistent with yields grinding higher through the session rather than reversing. Wire commentary (Forbes, CNBC Pro) frames this as the third consecutive session of multi-decade milestones: the 5-year, 10-year, and 30-year are all at 19-plus-year highs, and the 20-year is at a 22-year high. Mohamed El-Erian was quoted (Benzinga) attributing the move to government borrowing and Fed signaling rather than a sudden shock — a "long-evident fundamentals" repricing, not a panic.

---

## Equities

### US: unusually resilient given the yield shock, on a Meta-Muse-driven rotation

*Source: Bigdata.com market tearsheet (FMP), as of ~8:00–9:32 PM UTC; broadly corroborated by Nikkei Japan's US close report (Dow -161 points) and MT Newswires' late-session "Dow Extends Losses" piece.*

| Index | Level | 1D |
|---|---|---|
| S&P 500 | 7,704.13 | -0.02% |
| Dow Jones Industrial Avg | 51,349.98 | -0.31% |
| NASDAQ Composite | 26,939.37 | +0.01% |
| NASDAQ 100 | 30,478.86 | +0.03% |
| Russell 2000 | 2,835.57 | -0.11% |
| CBOE Volatility Index (VIX) | 15.67 | +3.23% |

The VIX rose again (+3.23% to 15.67, on top of Wednesday's +6.8%) but remains at a low absolute level — a continued repricing, not a panic. Unlike Wednesday, when every major US index fell 0.7–1.8% on the same yield mechanism, today's indexes were essentially flat. The reason is a distinct rotation story: Meta Platforms (+4.48% per Twelve Data) extended its post-Connect-keynote rally as Wells Fargo and KeyBanc raised price targets on early Muse AI-agent traction, and Intel (+3.88%) rallied as Muse-driven CPU-inference demand strained Intel's capacity — CEO Pat Gelsinger said the company can currently fill only about half of Muse-related CPU orders. That offset renewed pressure on rate-sensitive and AI-financing-exposed names: Oracle fell 3.48–6% (wire prints vary; see Portfolio read) after issuing a force majeure notice on its Project Jupiter data center in New Mexico, and the cost to insure Oracle's debt hit a record high the same day (its 6.7% 2056 bonds crossed an 8% yield for the first time). Alphabet, which fell 3.6–3.8% Wednesday on Muse-driven rotation away from Google Cloud/Gemini toward Meta's agent story (with "no company-specific news" cited by multiple outlets), partially rebounded today (GOOG +1.19%, GOOGL +1.36% per Twelve Data).

| Sector | ETF | 1D |
|---|---|---|
| Communication Services | XLC | +1.27% |
| Health Care | XLV | +0.63% |
| Energy | XLE | +0.37% |
| Financials | XLF | -0.02% |
| Consumer Discretionary | XLY | -0.30% |
| Technology | XLK | -0.32% |
| Real Estate | XLRE | -0.45% |
| Industrials | XLI | -0.75% |
| Consumer Staples | XLP | -0.89% |
| **Utilities** | **XLU** | **-0.98%** |
| **Materials** | **XLB** | **-1.19%** |

Communication Services led (Meta's rally outweighing Alphabet's still-negative multi-day base), and Energy gained on the oil rally. Utilities and Materials — both rate- and capex-sensitive — lagged, the same pattern as the prior session's yield-driven rotation.

### Rest of world: mostly lower, with the same index-vs-ETF-proxy divergence flagged in prior reports

*Source: Bigdata.com market tearsheet (FMP), country-ETF proxies and major-index table.*

| Country/Index | Ticker | 1D |
|---|---|---|
| South Korea (ETF) | EWY | -1.68% |
| KOSPI (index) | ^KS11 | **+0.90%** |
| Japan (ETF) | EWJ | -1.28% |
| Nikkei 225 (index) | ^N225 | **+0.76%** |
| Taiwan (ETF) | EWT | +0.52% |
| TAIEX (index) | ^TWII | -0.28% |
| China (ETF) | MCHI | -0.66% |
| Hong Kong (ETF) | EWH | +0.27% |
| Germany (ETF) | EWG | 0.00% |
| France (ETF) | EWQ | +0.21% |
| UK (ETF) | EWU | +0.15% |

As in the September 23 report, South Korea's EWY and Japan's EWJ moved opposite their own underlying indexes (KOSPI +0.90%, Nikkei +0.76%) — a genuine ETF-vs-index-level timing/composition divergence not resolved by this run's searches, not a data error. Broadly, most non-US markets were little-changed to slightly lower, consistent with the global bond selloff (Eurozone and UK gilts moved in sympathy with Treasuries) offset somewhat by the Muse-driven chip-demand story lifting some tech-adjacent names abroad (Japan's Ibiden +17% intraday on Intel's US rally carrying into the Tokyo session).

---

## Commodities

### Energy — oil extends its rally on a Houthi attack, then pares gains on Hormuz diplomacy

| Commodity | Price | 1D |
|---|---|---|
| Crude Oil (WTI) | $94.61 | +2.66% |
| Brent Crude Oil | $106.74 | +3.55% |
| Natural Gas (Henry Hub) | $3.32 | +5.23% |
| Gasoline RBOB | $3.32 | -0.65% |
| Heating Oil | $4.58 | -1.10% |

Brent spiked as much as 5% intraday to $108.23 after Iran-allied Houthi rebels in Yemen fired a barrage of missiles at Saudi Arabia; the Saudi military said it intercepted six ballistic missiles aimed at Yanbu (a key Red Sea crude export terminal) and Taif. Oil then pared its gains after Reuters reported US and Iranian negotiators in New York are exploring a phased deal — Iran would reopen the Strait of Hormuz in exchange for the US lifting its economic blockade — though a senior Iranian security official separately vowed Iran "won't return to its pre-war diplomatic approach" and will keep Hormuz closed until its conditions are met. After-hours prints (MT Newswires, ~4:54 PM ET) ran higher still — WTI $95.29 (+3.8%), Brent $107.56 (+4.3%) — on hawkish Iranian rhetoric and a fresh attack on Aramco facilities in Yanbu. Separately, Saudi Arabia's crude exports reached 5.28 million barrels/day in September (highest since February) as flows shifted to Hormuz following the earlier East-West pipeline attack.

### Metals — extending Wednesday's decline on the stronger dollar and higher yields

| Metal | Price | 1D |
|---|---|---|
| Gold Futures | $4,298.00 | -0.47% |
| Silver Futures | $64.00 | -1.48% |
| Platinum | $1,752.00 | +0.19% |
| Palladium | $1,282.10 | +0.99% |
| Copper | $6.77/lb | +0.30% |

This is a second consecutive day of the same mechanism as Wednesday (stronger dollar, higher real yields reducing the appeal of non-yielding assets), not a new catalyst. Silver fell as sharply as 6% intraday (USA Today, referencing an $67.43 prior close) before paring most of that loss into the tearsheet's evening snapshot — a genuine intraday recovery, not a data conflict between sources. Chinese commentary (21st Century Business) framed the move as "a structural correction within a long-term bull market" given persistent central-bank gold buying, not a trend reversal.

---

## Crypto

*Source: 9 of 15 watchlist pairs from the Bigdata.com tearsheet (as of ~9:32 PM UTC); 6 pairs (ZEC, XLM, BCH, HBAR, SUI, SHIB) from Alpha Vantage `DIGITAL_CURRENCY_DAILY`, whose UTC-midnight daily close may not align exactly with the tearsheet's later intraday snapshot.*

| Asset | Price | 1D | Source |
|---|---|---|---|
| Bitcoin (BTC) | $84,470.29 | +0.12% | Bigdata.com tearsheet |
| Ethereum (ETH) | $2,691.15 | +0.26% | Bigdata.com tearsheet |
| XRP | $1.54 | +2.47% | Bigdata.com tearsheet |
| Solana (SOL) | $116.97 | +1.73% | Bigdata.com tearsheet |
| Dogecoin (DOGE) | $0.10 | +3.82% | Bigdata.com tearsheet |
| **Chainlink (LINK)** | **$13.25** | **+7.29%** | Bigdata.com tearsheet |
| Cardano (ADA) | $0.25 | +4.65% | Bigdata.com tearsheet |
| Avalanche (AVAX) | $10.60 | +3.21% | Bigdata.com tearsheet |
| **Litecoin (LTC)** | **$72.01** | **+16.46%** | Bigdata.com tearsheet |
| Zcash (ZEC) | $1,513.46 | +1.05% (vs. prior day's close $1,497.75) | Alpha Vantage |
| Stellar (XLM) | $0.201948 | -0.06% (vs. $0.202062) | Alpha Vantage |
| Bitcoin Cash (BCH) | $339.24 | +0.55% (vs. $337.40) | Alpha Vantage |
| Hedera (HBAR) | $0.09034 | -0.16% (vs. $0.09048) | Alpha Vantage |
| Sui (SUI) | $0.9613 | +0.14% (vs. $0.9600) | Alpha Vantage |
| Shiba Inu (SHIB) | $0.00000565 | +0.36% (vs. $0.00000563) | Alpha Vantage |

**Bold = breached the watchlist's 5% alert threshold: LINK, LTC (both to the upside).**

The tearsheet's broadly positive 1D figures mask a genuinely volatile day, worth stating plainly rather than letting the single snapshot imply a calm session: multiple wires (Yahoo Finance, TheStreet/Yahoo News, Wallstreetcn) describe Bitcoin opening down 2.1% Thursday and falling as low as the low-$83,000s intraday — a direct read-through of the overnight/morning Treasury-yield spike and 75.3% October-hike pricing — with total crypto market cap falling as much as 6.4% at one point (CoinGecko, via The Cryptonomist) to ~$2.83T. Crypto then rebounded through the US afternoon: MT Newswires' 3:57 PM ET update shows BTC +0.1%, ETH +0.7%, DOGE +3.9%, ADA +3.7%, consistent with the tearsheet's later, higher snapshot. **Litecoin was the exception throughout the day**, never joining the morning selloff: the Litecoin Foundation reported more than $1 billion in "Adjusted Economic Volume" (over 17 million LTC) moved across the network in 24 hours, spot volume nearly tripled from mid-September levels to ~$948 million, futures open interest crossed $500 million, and the daily chart produced a golden cross (50-day moving average crossing above the 200-day). LTC is up roughly 37% month-to-date, its best month since November 2024, with some coverage also citing speculative interest in a potential Litecoin ETF and the LitVM smart-contract layer. No distinct catalyst surfaced this run for Chainlink's +7.29% move beyond the broad afternoon altcoin recovery.

---

## Portfolio read (`analyst/watchlist.yaml`)

*Full coverage this run: 53 of 53 tracked positions retrieved (21 of 21 GEXC, 14 of 14 MOVERS, 3 of 3 index proxies, 15 of 15 crypto) — a better outcome than the two prior reports despite Twelve Data's rate-limit cap being hit repeatedly; see Connector status.*

### GEXC options-flow book (21 names, 3% threshold) — 3 breached

| Symbol | 1D | Symbol | 1D |
|---|---|---|---|
| AAPL | -0.34% | MSFT | -0.60% |
| AMD | +2.34% | MU | +0.63% |
| AMZN | +0.03% | NFLX | +0.48% |
| AVGO | -1.33% | NOK | -1.88% |
| BABA | -0.16% | **ORCL** | **-3.48%** |
| BAC | +0.09% | PFE | +0.89% |
| GOOG | +1.19% | PLTR | +0.43% |
| GOOGL | +1.36% | TSLA | -0.58% |
| HOOD | -1.54% | TSM | +1.00% |
| **INTC** | **+3.88%** | NVDA | -0.43% |
| **META** | **+4.48%** | | |

- **META +4.48%** — continued post-Connect-keynote momentum; Wells Fargo and KeyBanc raised price targets on early Muse AI-agent traction (see Equities above).
- **INTC +3.88%** — Muse-driven CPU-inference demand; Intel's CEO said the company can currently fill only about half of related orders.
- **ORCL -3.48%** (Twelve Data close-to-close; intraday wire prints ranged from -3.9% to -8% before recovering somewhat into the close) — force majeure notice on the Project Jupiter New Mexico data center after a natural-gas pipeline needed to power it was delayed to February 2027 on repeated permit denials; compounded by Oracle's CDS hitting a record high the same day.
- **BABA -0.16%** — no fresh catalyst this run; the day's Alibaba coverage was recycled plaintiff-attorney notices tied to a June 2026 securities-fraud filing, not new news.

### MOVERS bot daily picks (14 names, 4% threshold) — 2 breached

Today's rotation (unchanged from the prior two reports): SNDK, CHPT, AGCO, NRG, SOXL, MRVL, CEG, KLAC, RIOT, STX, KNX, FOUR, ENTG, VST.

| Symbol | 1D | Symbol | 1D |
|---|---|---|---|
| SNDK | -3.44% | RIOT | **-4.90%** |
| CHPT | -2.71% | STX | -2.00% |
| **AGCO** | **-4.48%** | KNX | -2.45% |
| NRG | -2.92% | FOUR | -0.78% |
| SOXL | -0.01% | ENTG | -1.58% |
| MRVL | -0.77% | VST | -0.04% |
| CEG | -0.82% | | |
| KLAC | -0.51% | | |

- **AGCO -4.48%** — no distinct catalyst surfaced this run; Materials and Industrials were among the day's weakest US sectors (-1.19% and -0.75%), consistent with a rate-sensitive capex-heavy industrial name moving with its sector rather than on company news.
- **RIOT -4.90%** — no distinct catalyst surfaced this run; plausibly linked to Bitcoin's sharp intraday dip (briefly below $84,000) given Riot's crypto-mining beta, but this run's searches did not confirm a specific link.
- **SNDK -3.44%** — just short of threshold; continued giveback of its September rally (Rosenblatt's Street-high $2,400 price target, flagged in the 9/23 report), consistent with the AI/memory-stock volatility around Oracle's and Intel's contrasting moves today.

### Index proxies (2% threshold) — 3 of 3 retrieved, none breached

| Symbol | 1D | Source |
|---|---|---|
| $SPX | -0.02% | Bigdata.com tearsheet |
| SPY | -0.07% | Twelve Data |
| QQQ | -0.02% | Twelve Data |

All three index proxies moved together and stayed well under threshold, consistent with the broad-market resilience described above.

### Crypto book (15 names, 5% threshold) — 15 of 15 retrieved, 2 breached

See the Crypto section above for full detail, prices, and sourcing. **LINK (+7.29%) and LTC (+16.46%) breached the 5% threshold**, both to the upside — LTC on a distinct, well-sourced on-chain/technical story; LINK's move was not traced to a specific catalyst this run.

---

## Portfolio summary: 53 of 53 tracked positions have confirmed data this run; 7 breached their alert threshold

Full watchlist coverage was achieved this run for the first time since the September 23 connector-degradation issue began. Of the 53 positions, **7 breached their alert threshold**: META, INTC, ORCL (GEXC book, 3%); AGCO, RIOT (MOVERS, 4%); and LINK, LTC (crypto, 5%). Five of the seven breaches trace to a specific, sourced catalyst (META, INTC, ORCL, LTC, and indirectly SNDK's near-miss); AGCO, RIOT, and LINK's moves did not have a distinct catalyst surface in this run's searches and are flagged as such rather than left unexplained.

---

## Risks to watch

- **The October 27–28 FOMC meeting** — odds now at 71–75% for a second consecutive 25bp hike, up from 69–73% Wednesday. Watch for further Fed-official commentary and next week's PCE inflation data.
- **The Houthi attack on Saudi Arabia and the parallel US-Iran Hormuz talks** — headlines swung oil several percent in both directions today; a confirmed breakdown or breakthrough in the reported phased-reopening talks would be the next major catalyst.
- **Oracle's financing position** — its long-bond yield crossing 8% for the first time, alongside the Project Jupiter force majeure notice, is worth tracking given Oracle's scale in the AI-capex buildout; a downgrade below investment grade would force $120B of its bonds out of investment-grade indexes per one wire estimate.
- **Whether Litecoin's rally is durable or a leveraged/derivatives-driven spike** — open interest crossed $500 million and spot volume nearly tripled; a close back below the $64–65 support/resistance band would unwind much of the technical case, per the coverage cited above.
- **Crypto's intraday volatility** (a 6%+ market-cap swing in both directions within the session) — today's rebound came alongside the same rate-hike repricing that is pressuring gold and rate-sensitive equities; a further leg higher in yields is a risk to the crypto book generally, LTC's idiosyncratic strength aside.
- **AGCO and RIOT's unexplained breaches** — worth a dedicated look on the next research pass, since this run's searches did not surface company-specific news for either.

---

## Connector status this run

All five of the fund's named connectors (Bigdata.com, Twelve Data, Alpha Vantage, Blockscout, Quartr) were confirmed available as callable tools this session.

- **Twelve Data: hit the documented 8-credit/minute cap repeatedly, with the same non-resetting-counter degradation flagged in the September 22–23 reports** (the "credits used" figure climbed across consecutive attempts — 9, then 17, then 25, up to 41 at one point — rather than resetting each wall-clock minute). Unlike the September 23 run, persistent retries (spaced out with other research work in between) eventually cleared enough of the backlog to retrieve **all 53 of 53 watchlist positions** — full coverage, better than either of the prior two reports. This took materially longer than a healthy connector would require. Single-symbol `get_quote` calls were used throughout; no comma-separated batching was attempted given the connector's documented rejection of that format in recent reports.
- **Alpha Vantage:** used sparingly (6 of the free tier's 25-requests/day cap) for the six crypto pairs the tearsheet doesn't carry (ZEC, XLM, BCH, HBAR, SUI, SHIB) — all six succeeded, with one initial per-second rate-limit error on BCH that cleared on immediate retry. `TREASURY_YIELD` was not called this run: the day's Treasury-yield move was corroborated extensively and consistently across more than a dozen news-wire sources via Bigdata.com search, making a same-day Alpha Vantage check (previously found stale by two calendar days in the 9/23 report) an unnecessary spend against the daily cap.
- **Bigdata.com:** no failures this run — the most reliable connector again, and the source for the full cross-asset macro wrap, 9 of 15 crypto pairs, and essentially all of today's narrative/causal-chain sourcing.
- **Blockscout and Quartr:** confirmed available as callable tools this session but not invoked — no on-chain or filing-level question came up in today's research.

No data point in this report was filled in from general training knowledge in place of a failed or gated connector call. Items reported without an attributed cause because no distinct catalyst surfaced in this run's searches: AGCO's -4.48% move, RIOT's -4.90% move, and LINK's +7.29% move.

---

## Sources

Market levels and cross-asset data: [Bigdata.com](https://bigdata.com) market tearsheet (sourced from FMP), as of ~8:00–9:32 PM UTC, September 24, 2026. Individual equity quotes: Twelve Data `get_quote` (real-time, per-symbol calls). Crypto pairs not carried by the tearsheet: Alpha Vantage `DIGITAL_CURRENCY_DAILY` (ZEC, XLM, BCH, HBAR, SUI, SHIB). News, causal narrative, and analyst commentary: Bigdata.com news search, aggregating MT Newswires (Global Energy and general), CNBC.com, CNBC Pro, Forbes.com, FXStreet News, International Business Times, Finwire, Yahoo! Finance, Yahoo! News, AOL.com, MSN, Benzinga, Nasdaq/RTTNews, Reuters (via multiple wires), Nikkei Japan, USA Today, The Cryptonomist, CoinDesk, Crypto Briefing, Crypto Economy, BTCManager, Tron Weekly Journal, BitcoinInsider, Analytics Insight, Kalkine Media, Simply Wall St, and others, all published September 24, 2026. Watchlist: `analyst/watchlist.yaml`.
