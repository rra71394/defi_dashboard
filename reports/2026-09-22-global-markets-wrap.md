# Global Markets Wrap — September 22, 2026

*Compiled from Bigdata.com (market tearsheet + news search), Twelve Data, and Alpha Vantage. Cross-asset levels from the Bigdata.com/FMP tearsheet as of ~8:00–9:45 PM UTC, September 22, 2026. Blockscout and Quartr were confirmed available as callable tools this session but not invoked — no on-chain or filing-level question came up today. **This is a draft for human review, not a trade recommendation** — see `analyst/GUARDRAILS.md`. **Portfolio coverage note:** Twelve Data's per-minute rate limit did not clear for most of this session despite repeated waits (see Connector status) — the GEXC and MOVERS equity books and 5 of 15 crypto pairs are incomplete below; every gap is stated explicitly rather than filled from general knowledge.*

## TL;DR

A quiet, mixed US equity session (S&P 500 essentially flat at -0.00%, Nasdaq Composite +0.45%, Dow -0.36%) masked two real cross-currents. First, crude oil fell for a **fifth straight session** to a two-week low (WTI -2.00% to $90.52 per the tearsheet; wire settlement prints run higher, $94.59–$95.25 — see the sourcing-discrepancy note below) on Iran's offer to reopen the Strait of Hormuz within seven days if the US eases its blockade, Saudi Arabia restarting its damaged East-West pipeline, and a three-hour US-Iran meeting on the sidelines of the UN General Assembly that Trump called "very good." Second, **financials were the day's worst S&P sector** (XLF -1.97%) as JPMorgan and Goldman Sachs weighed on the Dow after UBS CEO Sergio Ermotti flagged softer Q3 wealth-management and banking fee income — wires also cited a rotation of capital out of wealth-management names and into AI plays on rising expectations for Meta's "Muse" AI agent. Semiconductors kept the Nasdaq positive even as the broader tape stalled: SanDisk, Micron, Marvell and ARM all gained 2%+.

**Crypto:** Bitcoin and Ethereum both eased (-0.44%, -0.99%) after last week's short-squeeze-driven rally, while XRP (+2.60% on the tearsheet, wires show +3.5–5%) and Cardano (+2.44%) kept grinding higher — XRP's move is a continuation of the short-covering bounce that began September 21 after the CLARITY Act's Senate cloture vote failed 49-50 on September 15/16, not a fresh catalyst: about $300 million in crowded short positions were closed September 21, and reports cite $1.9 billion in spot crypto-ETF net inflows over the last 24 hours.

**Commodities:** US natural gas spiked +5.65% to a two-week high above $3/MMBtu on lower end-of-season storage expectations and a short-covering rally, even as European gas fell on the same Iran de-escalation hopes pressuring oil. Gold and silver were little changed (-0.17%, +0.17%) — a quiet day for metals against a much noisier energy and rates tape.

**Rates:** the 10-year Treasury yield held flat at 4.96% on the tearsheet; Alpha Vantage's `TREASURY_YIELD` series (most recent print September 18, 5.01%) remains a few days stale relative to today, continuing the lag flagged in prior reports.

---

## The trigger: oil's fifth down day on Iran diplomacy, financials drag the Dow on a bank-to-AI rotation

*Source: MT Newswires, MT Newswires - Global Energy, Nasdaq, CNBC Arabia, Kabutan, MINKABU, all September 22, 2026.*

Crude fell for a fifth consecutive session, extending the de-escalation move that began September 21. Japan's Kyodo News and Reuters reported Iran has offered to reopen the Strait of Hormuz within seven days if the US lifts its blockade of Iranian ports and eases military pressure — Iran's semiofficial Fars news agency later called the reports "unreliable," a genuine source conflict worth flagging rather than resolving. Separately, Saudi Arabia reportedly restarted its East-West pipeline (damaged in a drone attack September 13, which had halted loadings at the Red Sea port of Yanbu), and US Treasury Secretary Scott Bessent said all Iranian airlines will be barred from US refueling services starting Wednesday — pressure and diplomacy moving in parallel. President Trump told reporters after a three-hour US-Iran meeting at the UN General Assembly that "it was a very good meeting" but that he still has "a big decision" to make on whether to pursue a negotiated deal or not; Iran's Revolutionary Guard struck a more guarded tone. TD Securities' Ryan McKay noted total Middle East crude transportation has returned to roughly 80% of pre-conflict levels, and that "without major escalation, Iran's key leverage in the strait may have been lost."

**Sourcing discrepancy, recurring pattern:** the Bigdata.com/FMP tearsheet has WTI at **$90.52, -2.00%** and Brent at **$98.52, -1.81%**. Wire settlement prints cluster higher for WTI specifically — CNBC Arabia's close: **$94.59, -1.24%**; MT Newswires' after-hours read: **$95.25, -0.7%**. Brent is closer across sources (tearsheet $98.52 vs. wire settles $98.28–$99.25). This is the same WTI tearsheet-vs-wire gap flagged in the September 18 and September 21 reports — now a third-plus recurrence — treat the tearsheet's WTI print with caution and prefer the wire-sourced ~$94–95 range for WTI specifically.

Separately, financials were the S&P's worst sector (XLF -1.97%, NYSE Financial Index -1.3% per MT Newswires) as JPMorgan and Goldman Sachs dragged on the Dow. Japanese wires (Kabutan, MINKABU) attributed this to comments from UBS CEO Sergio Ermotti suggesting Q3 wealth-management transaction and banking fee income will likely come in below last year, read negatively by the market, compounded by investors rotating capital out of wealth-management names and into AI plays amid rising expectations for Meta's AI agent "Muse." The Dow fell 0.36-0.39% (tearsheet vs. Sina wire, consistent within rounding) even as the Nasdaq Composite (+0.45%) and Nasdaq 100 (+0.82%) stayed positive on semiconductor strength — Sina Finance reported the Nasdaq touching a fresh intraday high before gains narrowed into the close, consistent with the S&P 500 itself closing essentially flat (-0.00%) after also giving back early gains.

**Unrelated but notable:** Novo Nordisk (not a fund position) fell 7.92% — the sharpest single-name decline surfaced in this run's searches — after new long-term targets failed to ease investor concern about its competitive position in the crowded weight-loss-drug market.

---

## Equities

### US indexes and sectors

*Source: Bigdata.com market tearsheet (FMP), as of ~8:00–8:59 PM UTC; cross-checked against MT Newswires/Sina wire prints (Dow -0.39%, Nasdaq Composite +0.36%, S&P 500 +0.02%), consistent within rounding.*

| Index | Level | 1D |
|---|---|---|
| S&P 500 | 7,764.64 | -0.00% |
| Dow Jones Industrial Avg | 51,863.69 | -0.36% |
| NASDAQ Composite | 27,244.28 | +0.45% |
| NASDAQ 100 | 30,732.40 | +0.82% |
| Russell 2000 | 2,889.92 | +0.51% |
| CBOE Volatility Index (VIX) | 14.21 | -4.44% |

The VIX fell another 4.44% to 14.21 — a fifth straight session of vol compression per the 5D change (-7.97%) — consistent with a market that shrugged off both the financials drag and the ongoing Iran headline risk. Storage-chip and semiconductor names led: SanDisk +4%+, Micron, SK Hynix, Marvell and ARM all +2%+, Seagate and Western Digital +1%+ (Sina Finance). The "Magnificent Seven" cohort diverged — Apple and Meta both +1%+, Alphabet +~1% (tearsheet shows GOOGL/GOOG individually down on the day per Twelve Data quotes below, a discrepancy against the wire's aggregate framing worth noting), Microsoft and Amazon both slightly negative.

| Sector | ETF | 1D |
|---|---|---|
| Materials | XLB | +1.65% |
| Technology | XLK | +0.73% |
| Consumer Staples | XLP | +0.99% |
| Health Care | XLV | +0.52% |
| Industrials | XLI | +0.17% |
| Real Estate | XLRE | -0.21% |
| Utilities | XLU | -0.32% |
| Consumer Discretionary | XLY | +0.09% |
| Communication Services | XLC | -1.06% |
| Energy | XLE | -1.09% |
| **Financials** | **XLF** | **-1.97%** |

Financials were the clear laggard for the reasons detailed in the trigger section above. Energy's decline (-1.09%) is a direct mirror of the oil selloff. Communication Services' -1.06% sits awkwardly against Meta's reported gain — no single-name breakdown within XLC surfaced in this run's searches to reconcile the two.

### Rest of world: broadly positive, South Korea and Taiwan again the standout movers

*Source: Bigdata.com market tearsheet (FMP).*

| Index | 1D |
|---|---|
| MOEX Russia | +1.88% |
| FTSE MIB (Italy) | +1.60% |
| Nikkei 225 (Japan) | +1.38% |
| CAC 40 (France) | +1.11% |
| Hang Seng (Hong Kong) | +0.18% |
| DAX 40 (Germany) | +0.20% |
| KOSPI (South Korea) | +0.15% |
| FTSE 100 (UK) | -0.15% |
| TWSE (TAIEX, Taiwan) | +1.31% |
| Jakarta Composite | -1.69% |

South Korea (EWY ETF proxy +1.83% 1D, +5.61% 5D) and Taiwan (EWT +4.04% 5D) remain the largest cumulative movers among the country ETF proxies over the past week, continuing the semiconductor-driven strength flagged in the September 21 report, even though the KOSPI index itself was only mildly positive today. No distinct catalyst for Jakarta's -1.69% decline surfaced in this run's searches.

---

## Rates

*Source: Bigdata.com market tearsheet (FMP); Alpha Vantage `TREASURY_YIELD` for freshness cross-check.*

| Maturity | Yield | 1D change |
|---|---|---|
| 1 Month | 3.97% | +0.25% |
| 2 Month | 4.09% | -0.24% |
| 3 Month | 4.16% | -0.24% |
| 6 Month | 4.26% | -0.23% |
| 1 Year | 4.43% | -0.45% |
| 2 Year | 4.71% | -1.05% |
| 3 Year | 4.81% | -0.21% |
| 5 Year | 4.83% | +0.00% |
| 7 Year | 4.89% | +0.00% |
| 10 Year | 4.96% | +0.00% |
| 20 Year | 5.33% | +0.00% |
| 30 Year | 5.29% | +0.00% |

*("1D change" is the relative change in the yield level per Bigdata.com/FMP, not basis points.)*

The front-to-belly of the curve (1Y through 3Y) eased slightly while 5Y and out held flat — consistent with MT Newswires' same-day note that the 10-year "was little changed at 4.968%." **Freshness cross-check:** Alpha Vantage's `TREASURY_YIELD` daily series shows its most recent print dated **September 18 (5.01%)** — four calendar days behind today's session, continuing the staleness pattern flagged in every report since September 14. Notably, the September 18 print (5.01%) is *higher* than both September 17's (4.94%) and today's tearsheet level (4.96%), underscoring that this series should not be used as a same-day figure — directionally informative only.

---

## Commodities

### Energy — oil's fifth down day; see the trigger section for the WTI sourcing discrepancy

| Commodity | Price | 1D (Bigdata.com/FMP) |
|---|---|---|
| Crude Oil (WTI) | $90.52 | -2.00% (wire settles: $94.59–$95.25, -0.7% to -1.24%) |
| Brent Crude Oil | $98.52 | -1.81% |
| **Natural Gas (Henry Hub)** | **$3.16** | **+5.65%** |
| Gasoline RBOB | $3.21 | +0.33% |
| Heating Oil | $4.72 | +0.20% |

Natural gas was the day's standout commodity mover, up 5.65% to trade above $3/MMBtu for the first time in two weeks in after-hours action (MT Newswires - Global Energy). The move came despite bearish medium-term fundamentals (the EIA's "Super El Niño" outlook, elevated storage projections) — the Wall Street Journal and NatGasWeather.com attributed the rally to expectations of lower end-of-season storage after a run of below-average weekly injections, plus a short-covering rally as bearish positioned traders were forced to exit, and a dip in production. European gas (Dutch TTF) moved the opposite direction, -2.48%, on the same Iran de-escalation hopes pressuring oil — a genuine divergence between the US and European gas markets on the same day's news.

At the pump, AAA had the national average gasoline price at $4.47/gallon, the most expensive September on record; GasBuddy's Patrick De Haan said diesel (a record $6.53/gallon, up from the September 4 record of $5.85) "has yet to hit their peak," though he expects it to crest within days.

### Metals — quiet day, little changed

| Metal | Price | 1D |
|---|---|---|
| Gold Futures | $4,376.40 | -0.17% |
| Silver Futures | $66.53 | +0.17% |
| Platinum | $1,825.50 | +1.34% |
| Palladium | $1,319.00 | +0.20% |
| Copper | $6.91/lb | +2.11% |

No distinct catalyst for gold/silver's near-flat session surfaced in this run's searches — a contrast to the sharper macro-driven metals moves in recent reports (e.g., September 21's dollar/Fed-hike-odds-driven gold decline). Copper's +2.11% continues its strong medium-term run (+26.18% 6M, +49.07% 1Y per the tearsheet) without an identified same-day catalyst in this run.

### Agricultural — Lean Hogs and Sugar the standouts, no catalyst surfaced

**Lean Hogs +1.72%** (partially reversing a brutal stretch: -10.01% 5D, -12.21% 1M) and **Sugar +0.98%** (+6.60% 5D) were the largest agricultural moves; **Wheat -1.67%** and **Coffee -1.68%** the largest declines. No distinct catalysts for any of these surfaced in this run's searches — none were run specifically on agriculturals, given the day's three larger cross-asset stories (oil, financials, natural gas) taking priority per the one-search-per-theme discipline.

---

## Crypto

*Source: Bigdata.com tearsheet (9 of 15 watchlist pairs) and Alpha Vantage `DIGITAL_CURRENCY_DAILY` (1 pair, ZEC). Five pairs (XLM, BCH, HBAR, SUI, SHIB) are unavailable this run — see Connector status.*

| Asset | Price | 1D | Source |
|---|---|---|---|
| Bitcoin (BTC) | $86,212.76 | -0.44% | Bigdata.com tearsheet |
| Ethereum (ETH) | $2,748.39 | -0.99% | Bigdata.com tearsheet |
| XRP | $1.57 | +2.60% (wires: +3.5% to +5.1%) | Bigdata.com tearsheet |
| Cardano (ADA) | $0.25 | +2.44% | Bigdata.com tearsheet |
| Dogecoin (DOGE) | $0.10 | +0.37% | Bigdata.com tearsheet |
| Solana (SOL) | $118.07 | -0.59% | Bigdata.com tearsheet |
| Avalanche (AVAX) | $11.05 | -1.56% | Bigdata.com tearsheet |
| Chainlink (LINK) | $12.89 | -1.86% | Bigdata.com tearsheet |
| Litecoin (LTC) | $62.43 | +0.70% | Bigdata.com tearsheet |
| Zcash (ZEC) | $1,467.55 | -0.21% (vs. prior day's close $1,470.69) | Alpha Vantage |
| Stellar (XLM), Bitcoin Cash (BCH), Hedera (HBAR), Sui (SUI), Shiba Inu (SHIB) | — | — | **Unavailable this run** |

Bitcoin and Ethereum both pulled back modestly after last week's sharp short-squeeze rally (BTC +12.92% 5D, ETH +12.39% 5D per the tearsheet) — a pause, not a reversal. XRP and ADA were the session's relative outperformers, continuing (not repeating) the move that began September 21: AOL.com and Yahoo! Finance both report XRP's rebound is being driven by **short-position closures (~$300 million on September 21)** rather than fresh buying, following the CLARITY Act's failed 49-50 Senate cloture vote on September 15/16, which stripped XRP of a path to guaranteed commodity-classification clarity that its peers didn't face. Key support cited at $1.53 — a close below that level would call the rebound's durability into question, per the same coverage. Separately, Crypto Wire cited SoSoValue data showing **US-listed spot crypto ETFs recorded $1.9 billion in net inflows** over the trailing 24 hours, with Bitcoin accounting for roughly $1.36 billion of that — a broader tailwind alongside the XRP-specific short-covering story. Veteran trader Peter Brandt's September 21 chart projecting a long-term XRP target of $5.40 also circulated widely in today's coverage; flagged here as market commentary, not a level this report endorses.

---

## Portfolio read (`analyst/watchlist.yaml`)

*Twelve Data `get_quote` calls. The connector's documented 8-credit/minute cap did not clear for most of this session despite three separate waits (60s, 90s, and 150s of zero calls in between) — see Connector status for detail. Only 8 of 21 GEXC names were retrieved before the connector locked up; the MOVERS book (14 names) and the QQQ index proxy could not be pulled at all this run.*

### GEXC options-flow book (21 names, 3% threshold) — 8 of 21 retrieved, 1 breached

| Symbol | 1D | Symbol | 1D |
|---|---|---|---|
| AAPL | +0.23% | BABA | +0.48% |
| AMD | +1.34% | **BAC** | **-3.04%** |
| AMZN | -1.34% | GOOG | -0.99% |
| AVGO | +0.52% | GOOGL | -1.07% |

Bold = breached the 3% threshold.
- **BAC (Bank of America) -3.04%** is the book's sole breach and a direct read-through of today's financials-sector story detailed above (JPM/GS dragging the Dow on the UBS-flagged wealth-management/banking fee outlook).
- **AMZN -1.34%** and **GOOG/GOOGL (both ~-1%)** sit against the wire framing that had Alphabet "up nearly 1%" and Amazon "down nearly 1%" — Twelve Data's quotes show Alphabet down, not up, a real discrepancy between this run's direct quote pull and the aggregate wire commentary cited in the Equities section; the Twelve Data figures are the more precise per-symbol source and are used here.
- **AMD +1.34%**, **AVGO +0.52%**, **BABA +0.48%**, **AAPL +0.23%** posted small gains, none past threshold.
- **13 names not retrieved this run** (HOOD, INTC, META, MSFT, MU, NFLX, NOK, NVDA, ORCL, PFE, PLTR, TSLA, TSM) — Twelve Data's per-minute cap locked up before these could be pulled; not filled from general knowledge or from the wire commentary above (which only covers a subset in aggregate, not per-symbol detail suitable for threshold-checking).

### MOVERS bot daily picks (14 names, 4% threshold) — unavailable this run

Today's rotation: SNDK, CHPT, AGCO, NRG, SOXL, MRVL, CEG, KLAC, RIOT, STX, KNX, FOUR, ENTG, VST. None of these are equity ETFs or sector proxies carried by the Bigdata.com tearsheet, and Twelve Data's rate limit locked up before this book could be reached. **No data available for this book this run** — not filled from general knowledge.

### Index proxies (2% threshold) — 2 of 3 retrieved, none breached

| Symbol | 1D | Source |
|---|---|---|
| $SPX | -0.00% | Bigdata.com tearsheet |
| SPY | -0.02% | Bigdata.com tearsheet |
| QQQ | — | **Unavailable this run** (Twelve Data locked up; not carried by the tearsheet) |

$SPX and SPY track closely, both essentially flat, consistent with the S&P 500's quiet session described above.

### Crypto book (15 names, 5% threshold) — 10 of 15 retrieved, 0 breached

See the Crypto section above for full detail and sourcing. None of the 10 retrieved pairs moved more than 3% in either direction today — a much quieter session than September 21's broad breach. **5 pairs unavailable this run: XLM, BCH, HBAR, SUI, SHIB** (Alpha Vantage's daily-request cap was reached after pulling ZEC; not filled from general knowledge).

---

## Portfolio summary: 1 of 24 tracked positions with confirmed data breached their alert threshold today; 29 of 53 positions have no data this run

A materially incomplete pull, disclosed in full above rather than papered over: of the book's 53 tracked positions, 24 returned live data this run (8 GEXC + 2 index proxies + 10 crypto + BAC's breach already counted in the 8), and only **BAC (-3.04%)** breached its threshold among them. The remaining 29 positions — the entire 14-name MOVERS book, 13 of 21 GEXC names, QQQ, and 5 crypto pairs — have no data this run due to the Twelve Data and Alpha Vantage connector issues detailed in Connector status below. This is a materially thinner portfolio read than the September 21 report and should not be read as "a quiet day" for the missing names — it reflects a data gap, not confirmed inactivity.

---

## Risks to watch

- **Whether the Iran-US diplomatic track (three-hour UN meeting, Iran's Strait of Hormuz reopening offer) produces anything concrete**, or whether Iran's own semiofficial Fars news agency's denial of the Hormuz-reopening report proves closer to the mark — a real, unresolved source conflict in today's coverage.
- **The financials-to-AI rotation flagged today** (UBS's Q3 wealth-management/fee-income warning, capital reportedly shifting toward AI names on Meta's "Muse" agent) — worth watching whether this is a one-day read-through of one CEO's comments or the start of a broader theme.
- **XRP's rebound remains short-covering-driven, not new-buyer-driven**, per AOL.com/Yahoo! Finance — a close below the cited $1.53 support level would call the move's durability into question.
- **The WTI tearsheet-vs-wire sourcing discrepancy** — now flagged in three consecutive reports (9/18, 9/21, 9/22) — resolve which figure is accurate before using WTI's 1D move in any downstream calculation.
- **This portfolio read is materially incomplete** (29 of 53 positions with no data) due to the Twelve Data connector lockup described below — the MOVERS book in particular (daily-rotating, momentum-driven names) has zero coverage today and should be a priority for the next monitoring pass once the connector clears.
- **Natural gas's short-covering-driven spike (+5.65%)** against bearish medium-term fundamentals (El Niño outlook, elevated storage projections) — worth watching whether this holds or reverses as a pure positioning unwind.

---

## Connector status this run

All five of the fund's named connectors (Bigdata.com, Twelve Data, Alpha Vantage, Blockscout, Quartr) were confirmed available as callable tools this session.

- **Twelve Data: materially degraded, a worse failure mode than prior reports.** The documented 8-credit/minute cap was hit as usual on the first batch of calls, but — unlike every prior report in this series — **it did not clear on schedule.** One batch of 8 individual `get_quote`/`get_price` calls succeeded (AAPL, AMD, AMZN, AVGO, BABA, BAC, GOOG, GOOGL — the entire successful pull for this run), but every subsequent attempt was rejected with an ever-increasing "API credits used" counter (9 → 21) across three separate waits (roughly 60, 90, and 150 seconds of zero intervening calls), suggesting the per-minute window was not resetting normally this session. This is a new failure pattern worth flagging for the next run — it consumed a large share of this session's time and left 13 of 21 GEXC names, all 14 MOVERS names, and QQQ unpulled. The batched comma-separated `get_price` call is still broken ("does not support CSV format"), consistent with every prior report since 9/14.
- **Alpha Vantage:** `TREASURY_YIELD` remains stale (most recent print September 18, four calendar days behind), continuing the pattern flagged since 9/14. One credit spent there; `DIGITAL_CURRENCY_DAILY` succeeded once (ZEC) before the connector's 25-requests/day cap was hit on the very next call (XLM) — this free-tier key appears to have very little daily headroom remaining, consistent with the hard daily-ceiling gotcha documented in `CONNECTORS.md`.
- **Bigdata.com:** no failures this run — the most reliable connector again, and the sole complete source for the cross-asset macro wrap above.
- **Blockscout and Quartr:** confirmed available as callable tools this session but not invoked — no on-chain or filing-level question came up in today's research.

No data point in this report was filled in from general training knowledge in place of a failed or gated connector call. Items reported without an attributed cause because no distinct catalyst surfaced in this run's searches: Communication Services' (XLC) -1.06% move against a reportedly-positive Meta, Jakarta Composite's -1.69% decline, gold/silver's near-flat session, copper's +2.11% move, and the agricultural-commodity moves noted inline above. Items with no data at all this run, stated explicitly rather than estimated: the MOVERS bot book (14 names), 13 of the GEXC book's 21 names, QQQ, and 5 of the crypto book's 15 pairs (XLM, BCH, HBAR, SUI, SHIB).

---

## Sources

Market levels and cross-asset data: [Bigdata.com](https://bigdata.com) market tearsheet (sourced from FMP), as of ~8:00–9:45 PM UTC, September 22, 2026. Individual equity quotes: Twelve Data `get_quote` (real-time, per-symbol calls; incomplete this run — see Connector status). Crypto: Alpha Vantage `DIGITAL_CURRENCY_DAILY` (ZEC only). Treasury-yield freshness check: Alpha Vantage `TREASURY_YIELD` (found stale, most recent print September 18). News, causal narrative, and analyst commentary: Bigdata.com news search, aggregating MT Newswires (Global Energy and general), MT Newswires - EMEA, Nasdaq (RTTNews), Kabutan, MINKABU, Sina (新浪) and Sina Finance, Sohu, CNBC Arabia, Benzinga, AOL.com, Yahoo! Finance, Yahoo! News, MSN, NBC News, Crypto Briefing, Crypto Wire, Cryptonews, Bitcoin.com, Analytics Insight, iProUP, Eastmoney (东方财富网), IndexBox, El Economista (MX), Via Ritzau, Ámbito, and others, all published September 22, 2026. Watchlist: `analyst/watchlist.yaml`.
