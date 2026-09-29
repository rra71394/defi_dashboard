# Global Markets Wrap — September 29, 2026

*Compiled from Bigdata.com (market tearsheet + news search), Alpha Vantage (6 crypto pairs not carried by the tearsheet, all 14 MOVERS names, and 4 of the most newsworthy GEXC names, in that order, before Alpha Vantage's 25-requests/day cap was hit mid-run on the 25th call), and Bigdata.com company tearsheets (the remaining 17 GEXC names, via `find_securities` + `bigdata_company_tearsheet`). **Twelve Data was not available as a callable tool in this session at all** — it requires an interactive OAuth authorization that this non-interactive scheduled run could not complete; see Connector status for detail. Cross-asset levels from the Bigdata.com/FMP tearsheet as of ~8:00–9:33 PM UTC, September 29, 2026; individual equity quotes are intraday/real-time as of ~9:36 PM UTC (see per-position sourcing below). **This is a draft for human review, not a trade recommendation** — see `analyst/GUARDRAILS.md`.*

## TL;DR

Oil reversed hard today after a week of Iran-driven gains: signs that Saudi Arabia has restored its East-West pipeline and Red Sea export flows (after early-September drone-strike damage) sent WTI down 3.48% to $89.38 and knocked Brent down 2.56% to $102.59 (both per wire settlement prints — see the Commodities section for a tearsheet-vs-settlement discrepancy flagged below), even though the underlying US-Iran standoff over the Strait of Hormuz remains unresolved and both benchmarks are still up double digits for the month. That supply-recovery story didn't stop Treasury yields from pushing to fresh multi-decade highs — the 10-year sits at 5.26% and the 30-year at 5.59%, both continuing the same rate-hike-cycle grind flagged in every report since mid-September, reinforced today by Fed Governor Michael Barr renewing his call for more rate hikes and New York Fed President John Williams saying he sees tighter policy ahead (even as August JOLTS job openings came in soft). US equities drifted modestly lower (S&P 500 −0.17%, Dow −0.26%) on higher yields, but the mega-cap tech complex split sharply on company-specific news: **Apple fell 2.66%** after Bank of America flagged competitive risk from Meta's new "Muse" AI shopping agent (which could reroute Apple's product-discovery and transaction revenue) on top of a Ternus-led management reorganization, while **Meta rose 3.24%** — Muse being the same story on the other side of the trade — and **Oracle jumped 3.99%** on a new "Fusion Claw" agentic-AI product launch plus a fresh data point on OpenAI's revenue run-rate (a direct read-through for Oracle's AI-infrastructure backlog). In crypto, **Avalanche (AVAX) rallied 7.76%** to a six-month high after Goldman Sachs' roughly $100 billion Treasury fund went live on an Avalanche-based institutional settlement network (Lynq), while **Chainlink (LINK) fell 5.16%** on profit-taking after touching a fresh 2026 high near $15.30 earlier in the session on its CCIP 2.0 launch — both moves are idiosyncratic, not macro-driven. Gold ticked up slightly (+0.27%) even as silver and platinum fell, a mixed read on precious metals against the same higher-yield backdrop that has pressured them for weeks.

**Note on context:** this is the same rate-hike cycle flagged in every report since September 16 (the Fed's first hike since 2023). Today's macro signal is genuinely mixed — a supply-driven retreat in oil, hawkish Fed commentary, and a soft labor-market data point (JOLTS) all landed the same day without resolving into a single clean narrative.

---

## The trigger: Middle East oil supply recovers, but the Fed stays hawkish on multi-decade-high yields

*Source: CNBC.com, Nasdaq (RTTNews), MSN/Reuters, Morningstar, MT Newswires, Alliance News, Infobae, all September 29, 2026.*

Oil prices fell sharply after satellite imagery (cited by Kpler) confirmed a "major operational recovery" at Saudi Arabia's Yanbu and Muajjiz Red Sea export terminals, with the East-West pipeline — damaged by drone strikes earlier this month — restored to roughly 50% of its 7-million-barrel-per-day capacity, "quicker than expected," per BOK Financial. September exports from major Middle Eastern producers climbed to 12.8 million barrels per day, the highest since February (Reuters/Kpler data, via Benzinga). WTI settled down 3.48% at $89.38 — its lowest close since August 31, seven down sessions in the last ten (Morningstar) — while Brent settled down 2.56% at $102.59. Both benchmarks are still up sharply for the month (WTI ~4-7%, Brent ~13-16%, depending on the wire cited), reflecting how elevated the starting base was. Crucially, the underlying conflict is not resolved: President Trump has rejected Iran's proposal to reopen the Strait of Hormuz, Iran has threatened to attack regional infrastructure, and Houthi attacks on Saudi energy facilities continue — so analysts (Ritterbusch and Associates, Saxo) framed today's move as a reduction in the immediate supply-disruption premium, not a resolution of the conflict.

That didn't ease the rates story. Treasury yields pushed to fresh highs — the 10-year at 5.26% (+0.38% on the day) and the 30-year at 5.59% (+0.54%) — with Infobae describing them as "the highest levels in over fifteen years." Fed Governor Michael Barr renewed his call for additional rate increases to combat sticky inflation, while New York Fed President John Williams said he expects monetary policy to tighten further, though he sees no urgency (MT Newswires). This landed alongside a softer data point — US job openings (JOLTS) fell in August, driven by a sharp decline in professional and business services — that cuts against the hawkish narrative without derailing it; CME FedWatch-implied odds of an October hike were described as "largely split" today rather than converging the way they did in late September.

**The cascade:** Saudi pipeline/export recovery reduces the acute Hormuz-disruption premium → oil sells off sharply even as the underlying US-Iran standoff continues → falling oil does not offset a fresh leg higher in Treasury yields, driven by hawkish Fed commentary against a softer JOLTS print → equities drift modestly lower on the yields story, while the day's real dispersion comes from single-name AI-strategy news (Apple/Meta/Oracle) rather than the macro tape → gold ekes out a small gain while silver and platinum fall, a split rather than a clean read-through from the yield/dollar mechanism that has pressured metals all month.

---

## Rates

*Source: Bigdata.com market tearsheet (FMP), as of September 29, 2026.*

| Maturity | Yield | 1D change |
|---|---|---|
| 1 Month | 4.04% | +0.00% |
| 2 Month | 4.18% | −0.48% |
| 3 Month | 4.25% | −0.70% |
| 6 Month | 4.36% | −1.13% |
| 1 Year | 4.58% | −0.22% |
| 2 Year | 4.89% | −0.61% |
| 3 Year | 4.98% | −0.60% |
| 5 Year | 5.06% | +0.00% |
| 7 Year | 5.16% | +0.19% |
| 10 Year | 5.26% | +0.38% |
| 20 Year | 5.64% | +0.71% |
| 30 Year | 5.59% | +0.54% |

*("1D change" is the relative change in the yield level per Bigdata.com/FMP, not basis points.)* Unlike the broad, front-to-back move flagged in the September 28 report, today's move was concentrated at the long end (7Y and out all up 0.19–0.71%) while the front end (1M–3Y) actually eased slightly — consistent with a market that's still pricing hikes further out but saw a modest near-term reprieve alongside the oil pullback.

---

## Equities

### US: modest broad decline; Apple/Meta/Oracle the day's real dispersion story

*Source: Bigdata.com market tearsheet (FMP), as of ~8:00–9:12 PM UTC.*

| Index | Level | 1D |
|---|---|---|
| S&P 500 | 7,670.84 | −0.17% |
| Dow Jones Industrial Avg | 51,349.92 | −0.26% |
| NASDAQ Composite | 26,797.54 | −0.09% |
| NASDAQ 100 | 30,339.33 | +0.21% |
| Russell 2000 | 2,807.92 | −0.35% |
| CBOE Volatility Index (VIX) | 16.04 | −0.19% |

The headline indexes were little-changed, but the mega-cap complex split on AI-strategy news rather than macro. **Apple fell 2.66%** to $329.40 after Bank of America analyst Wamsi Mohan warned that Meta's new "Muse" AI shopping agent — which can browse, fill forms, and complete purchases on a user's behalf, and has already gained access to Shopify, Expedia, and PayPal commerce integrations — could let Apple "keep every handset sale and still lose discovery, referral, and transaction initiation" (BofA kept its Buy rating). Layered on top: CEO John Ternus is reportedly restructuring Apple's organization to accelerate product launches and cut management layers, and Apple issued an emergency iOS 26.7.1 security patch for a CoreGraphics flaw with crypto-wallet exposure implications (no evidence this caused the price move). **Meta rose 3.24%** to $738.79 — the flip side of the same Muse story. **Oracle jumped 3.99%** to $137.90 (intraday high +8.2%) on the launch of "Fusion Claw," 25 new agentic-AI applications for its Fusion Cloud suite, a new OCI-native NetApp storage service, and a Axios report that OpenAI's annualized recurring revenue has approached $70 billion — a direct read-through for Oracle given its role as an OpenAI/Stargate infrastructure partner (this sits alongside the still-unresolved Project Jupiter force-majeure and cash-burn overhang flagged in prior reports). Alphabet slipped 0.53% and Microsoft was roughly flat (−0.05%), both described by AOL.com as facing smaller versions of the same search/commerce-bypass risk as Apple.

| Sector | ETF | 1D |
|---|---|---|
| Utilities | XLU | +1.20% |
| Industrials | XLI | +0.21% |
| Consumer Discretionary | XLY | +0.12% |
| Communication Services | XLC | +0.26% |
| Technology | XLK | −0.03% |
| Health Care | XLV | −0.31% |
| Financials | XLF | −0.33% |
| Consumer Staples | XLP | −0.53% |
| Materials | XLB | −0.78% |
| Energy | XLE | −0.90% |

Energy lagged despite still-elevated oil prices, consistent with today's sharp intraday pullback in crude; Utilities led, a classic lower-beta/defensive rotation on a quiet index day.

### Rest of world: broadly lower; South Korea the outlier on the upside

*Source: Bigdata.com market tearsheet (FMP), ETF proxies.*

| Country/Region (ETF) | Ticker | 1D |
|---|---|---|
| South Korea | EWY | +1.92% |
| Brazil | EWZ | +0.72% |
| Japan | EWJ | −0.33% |
| Hong Kong | EWH | −0.85% |
| China | MCHI | −0.84% |
| Germany | EWG | −0.55% |
| UK | EWU | −0.89% |
| France | EWQ | −1.15% |
| India | INDA | −0.28% |

South Korea's ETF (+1.92%) diverged from the index level itself (^KS11, −0.27%), a gap this run's searches did not resolve — flagged rather than reconciled. Most other major markets were modestly lower, tracking the same higher-yield backdrop pressuring US equities.

---

## Commodities

### Energy — sharp reversal on Saudi supply recovery; a tearsheet/settlement discrepancy worth flagging

*Source: Bigdata.com/FMP tearsheet; CNBC.com, Reuters (via MSN/Livemint), Morningstar, MT Newswires, Alliance News, all September 29, 2026.*

| Commodity | Tearsheet price/1D | Wire settlement (Reuters/Morningstar) |
|---|---|---|
| WTI Crude | $89.38 / −3.48% | $89.38, down 3.48% (**agrees**) |
| Brent Crude | $95.90 / −8.91% | $102.59, down 2.56% (**disagrees sharply**) |
| Natural Gas | $3.01 / −3.06% | — |
| Gasoline RBOB | $3.11 / −1.51% | — |
| Heating Oil | $4.53 / +0.74% | — |

**Flagging a real discrepancy rather than picking one number arbitrarily (per house style):** the Bigdata.com/FMP tearsheet's Brent print (−8.91%, to $95.90) is far more negative than every wire settlement source checked today, which converged tightly around $102.59, down 2.56–2.6% (CNBC, Reuters/Livemint, Morningstar, Infobae all independently reported this figure). The most likely explanation, per Morningstar: "The November Brent contract expires Tuesday, with December set to become the front-month contract" — the tearsheet's snapshot may be pricing a different contract month than the wires' settlement price, which would produce an apparent gap that's a contract-roll artifact rather than a true single-day move. Treat the wire-sourced −2.56% as the decision-relevant number for Brent; the tearsheet figure is presented above for transparency but should not be read as Brent falling nearly 9% in one session.

WTI's decline is well-corroborated across sources: Saudi Arabia's crude exports climbed to 5.28 million bpd in September (highest in seven months, Bloomberg tracking data via Nasdaq/RTTNews), and the East-West pipeline recovery reduced the near-term supply-disruption premium. Both benchmarks remain on track for a third consecutive monthly gain despite today's pullback.

### Metals — a mixed day, not a clean higher-yields sell-off

*Source: Bigdata.com/FMP tearsheet.*

| Metal | Price | 1D |
|---|---|---|
| Gold Futures | $4,179.70 | +0.27% |
| Silver Futures | $61.15 | −0.92% |
| Platinum | $1,701.00 | −2.50% |
| Palladium | $1,213.70 | −0.76% |
| Copper | $6.66/lb | +0.37% |

Gold opened near a two-month low (Yahoo! Finance) before recovering to a small daily gain, even as the same higher-real-yields dynamic that has pressured metals for weeks continued (10Y and 30Y both at fresh highs — see Rates). Silver and especially platinum fell more in line with that mechanism. This run's searches did not surface a gold-specific catalyst for the intraday reversal; presented as an observed data point, not an explained one.

---

## Crypto

*Source: 9 of 15 watchlist pairs from the Bigdata.com tearsheet (as of ~9:33 PM UTC); 6 pairs (ZEC, XLM, BCH, HBAR, SUI, SHIB) from Alpha Vantage `DIGITAL_CURRENCY_DAILY`, computed as the change from the 2026-09-28 UTC daily close to the 2026-09-29 UTC daily close — a different comparison window than the tearsheet's intraday snapshot, flagged per position.*

| Asset | Price | 1D | Source |
|---|---|---|---|
| Bitcoin (BTC) | $83,389.43 | −0.12% | Bigdata.com tearsheet |
| Ethereum (ETH) | $2,678.13 | −0.35% | Bigdata.com tearsheet |
| XRP | $1.49 | −0.30% | Bigdata.com tearsheet |
| Solana (SOL) | $118.63 | −0.17% | Bigdata.com tearsheet |
| Dogecoin (DOGE) | $0.09 | −0.05% | Bigdata.com tearsheet |
| Cardano (ADA) | $0.24 | −1.33% | Bigdata.com tearsheet |
| Litecoin (LTC) | $67.26 | −2.84% | Bigdata.com tearsheet |
| **Avalanche (AVAX)** | **$11.42** | **+7.76%** | Bigdata.com tearsheet |
| **Chainlink (LINK)** | **$14.65** | **−5.16%** | Bigdata.com tearsheet |
| Zcash (ZEC) | $1,485.64 | +0.17% (vs. prior close $1,483.10) | Alpha Vantage |
| Stellar (XLM) | $0.2304 | −0.85% (vs. $0.2324) | Alpha Vantage |
| Bitcoin Cash (BCH) | $309.98 | −0.05% (vs. $310.12) | Alpha Vantage |
| Hedera (HBAR) | $0.1206 | −1.17% (vs. $0.1220) | Alpha Vantage |
| Sui (SUI) | $1.1615 | −0.51% (vs. $1.1674) | Alpha Vantage |
| Shiba Inu (SHIB) | $0.00000567 | −0.18% (vs. $0.00000568) | Alpha Vantage |

**AVAX (+7.76%) and LINK (−5.16%) were the day's two watchlist breaches, and both are idiosyncratic — neither traces to the day's macro story.**

- **AVAX** jumped to a six-month high ($11.92 intraday, per Yahoo! Finance) after Goldman Sachs made its roughly $100 billion Financial Square Treasury Instruments Fund (FTIXX) available through Lynq, an institutional settlement network built on Avalanche. This is a genuine institutional-adoption catalyst, not a speculative move.
- **LINK** fell after touching a fresh 2026 high near $15.30–15.33 earlier in the session — up as much as ~12% in 24 hours per multiple sources (Yahoo! Finance, Crypto Wire, The Cryptonomist) — on the Monday launch of CCIP 2.0 (an upgraded Cross-Chain Interoperability Protocol securing $82–84B in cross-chain value, plus a new Swift banking-integration pilot with 17 institutions including HSBC, Citi, UBS, and Wells Fargo). CryptoPotato reported signs of profit-taking late in the session (smaller-holder wallet counts declining even as larger holders continued accumulating), consistent with the pullback to $14.65 by the tearsheet's ~9:33 PM UTC snapshot. Net effect: LINK is still up sharply week-over-week (tearsheet shows +10.87% on a 5D basis) despite today's single-day pullback — the -5.16% is a retracement from an intraday high, not a reversal of the underlying rally.

---

## Portfolio read (`analyst/watchlist.yaml`)

*Coverage this run: 53 of 53 tracked positions retrieved despite Twelve Data being completely unavailable (see Connector status) — Alpha Vantage covered the 6 crypto pairs above, all 14 MOVERS names, and 4 GEXC names (NVDA, INTC, META, AMD) before hitting its 25-requests/day cap on the 25th call (attempting MU); Bigdata.com's company tearsheet (via `find_securities`) filled the remaining 17 GEXC names, all via real-time/intraday quotes as of ~9:36 PM UTC. One caveat: BABA resolved to its Hong Kong primary listing (HKD 106.20, −1.39%) rather than the NYSE ADR, consistent with how Bigdata.com's entity resolution has handled this name in prior runs.*

### GEXC options-flow book (21 names, 3% threshold) — 1 breached

| Symbol | 1D | Source | Symbol | 1D | Source |
|---|---|---|---|---|---|
| **AAPL** | **−2.66%** | Bigdata.com | MSFT | −0.05% | Bigdata.com |
| AMD | −0.05% | Alpha Vantage | MU | +1.05% | Bigdata.com |
| AMZN | +0.21% | Bigdata.com | NFLX | +1.55% | Bigdata.com |
| AVGO | +1.58% | Bigdata.com | NOK | +2.37% | Bigdata.com |
| BABA | −1.39%* | Bigdata.com | **ORCL** | **+3.99%** | Alpha Vantage |
| BAC | −0.92% | Bigdata.com | PFE | +0.02% | Bigdata.com |
| GOOG/GOOGL | −0.53%† | Bigdata.com | PLTR | −0.27% | Bigdata.com |
| HOOD | −0.21% | Bigdata.com | TSLA | −1.29% | Bigdata.com |
| INTC | −0.09% | Alpha Vantage | TSM | 0.00%‡ | Bigdata.com |
| META | +3.24% | Alpha Vantage | | | |
| NVDA | −0.72% | Alpha Vantage | | | |

*BABA priced in HKD (Hong Kong primary listing), not the NYSE ADR. †GOOG and GOOGL both map to Alphabet Inc. in Bigdata.com's data this run — one shared price point. ‡TSM quoted in TWD on the Taiwan exchange, flat on the day per its ~05:30 UTC (Taiwan-hours) snapshot — not flagged as stale (current-day timestamp), just genuinely unchanged.

- **ORCL (+3.99%)** — see Equities above: Fusion Claw agentic-AI launch, new NetApp/OCI storage service, and the OpenAI revenue read-through, partly offset by the unresolved Project Jupiter cash-burn overhang.
- **AAPL (−2.66%)**, the closest non-breach to the threshold, came within a fraction of triggering: BofA's Meta-Muse competitive warning plus a management reorganization under CEO Ternus — see Equities above for full detail.

### MOVERS bot daily picks (14 names, 4% threshold) — 2 breached

Today's rotation: SNDK, CHPT, AGCO, NRG, SOXL, MRVL, CEG, KLAC, RIOT, STX, KNX, FOUR, ENTG, VST (all via Alpha Vantage `GLOBAL_QUOTE`).

| Symbol | 1D | Symbol | 1D |
|---|---|---|---|
| SNDK | +0.98% | RIOT | −1.06% |
| **CHPT** | **+8.87%** | STX | −0.87% |
| AGCO | −1.22% | KNX | +1.07% |
| NRG | +0.18% | FOUR | +0.14% |
| SOXL | +3.34% | ENTG | +2.75% |
| **MRVL** | **+4.51%** | VST | +2.02% |
| CEG | +1.59% | | |
| KLAC | +3.89% | | |

- **CHPT (+8.87%)** — ChargePoint extended a 65% one-month run; both listed charging-sector peers (EVgo, Blink Charging) were roughly flat to lower on the day, so this run's sourcing frames the move as stock-specific momentum rather than a sector story, with no single fresh catalyst identified today — flagged as an unexplained continuation rather than a confirmed one-day cause.
- **MRVL (+4.51%)** — Bank of America analyst Vivek Arya raised his view of Marvell's custom-AI-chip opportunity (citing a possible $300B market by 2030), and investors are positioning ahead of Marvell's October 6 analyst day; the stock is up 210% year-to-date per AOL.com/GuruFocus.
- KLAC (+3.89%) and SOXL (+3.34%) came closest to the threshold without breaching — both track the same semiconductor-sector strength touching MRVL and ORCL today.

### Index proxies (2% threshold) — none breached

| Symbol | 1D | Source |
|---|---|---|
| $SPX | −0.17% | Bigdata.com tearsheet (^SPX) |
| SPY | −0.17% | Bigdata.com tearsheet |
| QQQ | not independently retrieved — ^NDX (+0.21%) used as disclosed proxy | Bigdata.com tearsheet |

QQQ itself wasn't retrieved this run (Alpha Vantage's daily cap was exhausted before reaching it, and the Bigdata.com tearsheet doesn't carry that specific ETF). ^NDX is a reasonable direction proxy but not QQQ's actual print.

### Crypto book (15 names, 5% threshold) — 2 breached

See the Crypto section above for full detail, prices, and sourcing. **AVAX (+7.76%)** and **LINK (−5.16%)** were the two breaches, both sourced to idiosyncratic, non-macro catalysts.

---

## Portfolio summary: 53 of 53 tracked positions have confirmed data this run; 5 breached their alert threshold

Breaches: **GEXC book (1 of 21, 3% threshold)** — ORCL (+3.99%, sourced to its Fusion Claw launch and the OpenAI revenue read-through). **MOVERS book (2 of 14, 4% threshold)** — CHPT (+8.87%, stock-specific momentum, no confirmed single-day catalyst) and MRVL (+4.51%, sourced to a bullish BofA note ahead of its October 6 analyst day). **Crypto book (2 of 15, 5% threshold)** — AVAX (+7.76%, Goldman Sachs' Lynq Treasury-fund integration) and LINK (−5.16%, profit-taking after a fresh 2026 high on its CCIP 2.0 launch). No index-proxy position breached its threshold.

---

## Risks to watch

- **Whether the Saudi export recovery holds.** Today's oil reversal rests on a fast-moving pipeline repair; any fresh disruption (continued Houthi attacks on Saudi energy facilities, a Hormuz escalation) could reverse the move quickly, as has happened repeatedly this month.
- **The diverging Fed/labor-market signal** — hawkish commentary from Barr and Williams landed the same day as a soft JOLTS print; if this divergence persists, it complicates the clean "hike odds rising" narrative from recent reports.
- **The Brent tearsheet/settlement discrepancy** flagged in Commodities — worth confirming with the connector or a second source before this data point is used in any position sizing, given the likely contract-roll explanation is not yet fully verified.
- **CHPT's unexplained +8.87% move** — a momentum-driven run with no confirmed single-day catalyst; per-position sourcing found nothing beyond continuation of an existing trend, which is worth flagging as a name that could reverse as quickly as it ran.
- **The AI-agent competitive dynamic between Apple and Meta** — Muse is a live, developing story (Shopify/Expedia/PayPal integrations already in place); today's Apple/Meta divergence may not be a one-day event.
- **South Korea's ETF/index divergence** (EWY +1.92% vs. ^KS11 −0.27%) — unresolved in this run's sourcing, worth a dedicated check next time Korea shows a notable move.

---

## Connector status this run

- **Twelve Data: unavailable as a callable tool for this entire session**, the same failure mode documented in every scheduled run since September 25 — the connector requires an interactive OAuth authorization that this non-interactive scheduled routine cannot complete. The founder should re-authorize via claude.ai connector settings (or `claude mcp`/`/mcp` in an interactive session) if uninterrupted Twelve Data access is expected going forward.
- **Alpha Vantage: hit its documented 25-requests/day cap on the 25th call.** Used, in priority order: the 6 crypto pairs not carried by the tearsheet (ZEC, XLM, BCH, HBAR, SUI, SHIB — all succeeded after several per-second throttling errors that cleared on individual retry), all 14 MOVERS names (succeeded after several more throttling errors, retried individually), and 4 of the most newsworthy GEXC names (NVDA, INTC, META, AMD) before the 25th call (MU) returned the distinct daily-cap error message (explicitly citing the API key and the 25-requests/day limit, as opposed to the generic per-second throttling message — confirming these are two separate error types, as suspected but not confirmed in the September 28 report).
- **Bigdata.com: no outright failures this run** — the source for the full cross-asset macro wrap, 9 of 15 crypto pairs, essentially all narrative/causal-chain sourcing, and — once Alpha Vantage's cap was hit — the remaining 17 of the 21 GEXC book's equity quotes via `find_securities` + `bigdata_company_tearsheet` (real-time intraday data, not the tearsheet's ~8 PM UTC snapshot). One resolution wrinkle: `find_securities` for "NOK" initially returned only unrelated private companies and a Swiss utility also ticked NOK — a retry with the query "Nokia" resolved correctly to Nokia Oyj.
- **Blockscout and Quartr:** not checked for availability this run (no on-chain or filing-level question came up in today's research); both were confirmed available in the September 25 run and there is no reason to believe that changed.

No data point in this report was filled in from general training knowledge in place of a failed or gated connector call. Two items are flagged as observed-but-unexplained rather than sourced to a confirmed cause: gold's small intraday reversal, and CHPT's momentum run.

---

## Sources

Market levels and cross-asset data: [Bigdata.com](https://bigdata.com) market tearsheet (sourced from FMP), as of ~8:00–9:33 PM UTC, September 29, 2026, and Bigdata.com company tearsheets (FMP) for individual GEXC equities (real-time, ~9:36 PM UTC). Crypto pairs not carried by the tearsheet and a subset of equity quotes: Alpha Vantage `DIGITAL_CURRENCY_DAILY` and `GLOBAL_QUOTE`. News, causal narrative, and analyst commentary: Bigdata.com news search, aggregating CNBC.com, Reuters (via MSN/Livemint/The Economic Times), Morningstar, MT Newswires, Alliance News, Infobae, Nasdaq (RTTNews/Zacks), Benzinga, Yahoo! Finance/GuruFocus, AOL.com, Crypto Wire, The Cryptonomist, CryptoPotato, Tron Weekly Journal, Edaily, Gelonghui, Zhitongcaijing (智通财经), Wallstreetcn (华尔街见闻), Today's Headlines (今日头条), Simply Wall St, and SEC EDGAR structured-note filings (JPMorgan Chase, Goldman Sachs, Morgan Stanley, HSBC USA, Barclays Bank, BofA Finance), all published September 29, 2026. Watchlist: `analyst/watchlist.yaml`.
