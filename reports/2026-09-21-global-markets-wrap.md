# Global Markets Wrap — September 21, 2026

*Compiled from Bigdata.com (market tearsheet + news search), Twelve Data, and Alpha Vantage (Treasury-yield freshness check). Blockscout and Quartr were confirmed available as callable tools this session but not invoked — no on-chain or filing-level question came up today. Cross-asset levels from the Bigdata.com/FMP tearsheet as of ~8:00–9:33 PM UTC, September 21, 2026; individual equity and crypto-pair quotes from Twelve Data `get_price`, pulled through the evening UTC, paced in small batches to stay under the connector's 8-credit/minute cap (see Connector status). **This is a draft for human review, not a trade recommendation** — see `analyst/GUARDRAILS.md`.*

## TL;DR

One mechanism, three overlapping stories: oil fell for a fourth straight session on easing Middle East risk, dragging the 10-year Treasury yield back down from Friday's 5% (2007-era) high to ~4.95–4.96% — and that combination of falling inflation-risk premium and falling discount rate lit up nearly every risk asset at once. President Trump said over the weekend he'd likely meet Iranian President Masoud Pezeshkian at this week's UN General Assembly and reportedly held off on further strikes on Iran-backed Houthis; separately, Saudi Arabia's crude exports have recovered to just over 4 million bpd in September (from a nine-year-low 2.4 million bpd in August), and the US Central Command said Strait of Hormuz transit volumes hit a six-month high. WTI fell as much as 4.5–4.8% intraday (Bigdata.com/FMP: -3.86% to $92.37; CNBC's settle: -4.5% to $95.78 — a real cross-source gap, see Commodities), and Brent eased toward $100.

**Equities:** the S&P 500 gained 1.49–1.55% (index vs. SPY), the Nasdaq Composite jumped 2.26%, and the Nasdaq 100 rose 2.83% to a fresh record close, led by a semiconductor rally (ARM and Intel both +13% intraday, AMD +9–10% and briefly crossing a $1 trillion market cap for the first time) on top of optimism about a US-China AI dialogue following a "very successful" Sunday meeting between Treasury Secretary Scott Bessent and Chinese Vice Premier He Lifeng, ahead of a Trump-Xi summit expected September 23–25. Energy was the only S&P sector to fall (XLE -2.88%), a direct mirror of the oil move.

**Crypto:** Bitcoin broke above $86,000 intraday for the first time since January (Bigdata.com/FMP: +6.86% to $86,730), closing the week above its 50-week moving average for the first time in 45 weeks. The move combined the same yields/oil tailwind with a crypto-specific short squeeze — reports range from roughly $300 million (in a single hour) to $648–710 million (trailing 24 hours) of short positions forced to cover — layered on last week's SEC/CFTC regulatory tailwinds (an SEC tokenized-stock exemption and a CFTC crypto-market-structure proposal, both filling the gap after the Senate's Clarity Act failed a cloture vote September 15/16).

**The one asset that didn't play along:** gold fell (-0.93% to $4,383.90/oz per Bigdata.com/FMP) even as yields eased, because the dollar firmed and Fed-hike odds for October stayed elevated (accounts range 54–56.5% per CME FedWatch to as high as 88% cited by one wire) — a reminder that gold is trading more on the dollar/rate-path axis than on the same oil-driven risk-sentiment wave lifting equities and crypto today.

---

## The trigger: oil's fourth straight down day eases the yield spike that rattled markets last week

*Source: CNBC.com, Reuters (via MSN), Nasdaq/RTTNews, Alliance News, FXStreet News, MT Newswires – Global Energy, Crypto Briefing, all September 21, 2026.*

Crude fell for a fourth consecutive session as markets priced in the prospect of renewed US-Iran diplomacy. President Trump told Fox News's Trey Yingst that "very big things" would happen with Iran "in the not so distant future," and said he'd likely be open to meeting Iranian President Masoud Pezeshkian on the sidelines of this week's UN General Assembly in New York; administration officials told the New York Times Trump had decided against further strikes on Iran-linked Houthi targets for now, even after the Houthis claimed strikes on Riyadh and an Aramco facility in Yanbu over the weekend, and after Trump separately warned Iran it would "fail economically" or face its leadership "wiped out" absent a deal. On the supply side, JPMorgan's Saturday note (cited by Reuters and MT Newswires) said Saudi Arabia's crude exports have recovered to just over 4 million bpd in September, up from a nine-year-low 2.4 million bpd in August, with Strait of Hormuz flows averaging 2.9 million bpd over the past six days versus just 700,000 bpd in August; US Central Command's Gen. Brad Cooper separately said Hormuz oil and LNG transit hit a six-month high over the past two weeks thanks to US Navy escort and mine-clearing operations.

**Sourcing discrepancy worth flagging, not resolving arbitrarily:** the Bigdata.com/FMP tearsheet puts front-month WTI (CLUSD) at **$92.37, -3.86% 1D**, while wire snapshots cluster in a different, more consistent range — CNBC's close: **$95.78, -4.5%**; Nasdaq/RTTNews: **$95.70, -4.5%+**; MT Newswires' after-hours read: **$95.48, -4.8%**. Brent is closer between sources: Bigdata.com/FMP has $100.34, -3.40%, versus CNBC's $100.34 close (-3.4%) and MT Newswires' $100.16 (-3.6%) — those effectively agree. This is the same kind of WTI tearsheet-vs-wire gap flagged in the September 18 report; treat the tearsheet's WTI print with caution and prefer the ~-4.5% to -4.8% wire-sourced range for WTI specifically.

The combined effect eased the acute inflation-risk premium that had been pushing Treasury yields toward 5%: the 10-year yield fell to **4.95–4.96%** Monday (Albuquerque Journal, WKYC/AP), down from Friday's 2007-era high just above 5%. Eurozone and UK gilt yields fell in sympathy, tracking Treasuries lower on the same oil-driven logic (Morningstar).

---

## Equities

### US indexes and sectors

*Source: Bigdata.com market tearsheet (FMP), as of ~8:00–8:50 PM UTC; cross-checked against CNBC/AP/MT Newswires closing prints (S&P 500 +1.49–1.55%, Nasdaq Composite +2.26–2.3%, Dow +0.71–0.8%), which are consistent to within rounding.*

| Index | Level | 1D |
|---|---|---|
| S&P 500 | 7,764.70 | +1.49% |
| Dow Jones Industrial Avg | 52,048.83 | +0.71% |
| NASDAQ Composite | 27,122.09 | +2.26% |
| NASDAQ 100 | 30,482.35 | +2.83% |
| Russell 2000 | 2,875.36 | +0.52% |
| CBOE Volatility Index (VIX) | 14.80 | -0.07% |

A semiconductor-led rally powered the Nasdaq to a record close: the Philadelphia Semiconductor Index rose materially on the session, with **ARM and Intel both surging over 13% intraday**, **AMD up 9–10%** and briefly crossing a **$1 trillion market cap for the first time** (its fifth straight winning session, market cap milestone reached after Nvidia, Broadcom, and Micron), **Qualcomm +6%**, and **Seagate and Micron both +2%+**. Broader mega-cap tech also participated — Meta +6%, Tesla +3%+, Alphabet and Nvidia +1%+ — while Microsoft turned lower intraday, a rare divergence within the mega-cap cohort. Drivers cited across wires: optimism about a US-China AI-safety dialogue (Treasury Secretary Bessent called Sunday's meeting with Chinese Vice Premier He Lifeng "very successful," describing a new "US-China AI dialogue" mechanism ahead of a Trump-Xi summit expected September 23–25), heightened AI-hardware demand expectations, and the easing oil/yield backdrop described above. The VIX stayed low (14.80, essentially flat) — a rally built on relief, not a squeeze out of distress.

| Sector | ETF | 1D |
|---|---|---|
| Communication Services | XLC | +3.56% |
| Technology | XLK | +2.77% |
| Consumer Discretionary | XLY | +1.08% |
| Health Care | XLV | +0.37% |
| Real Estate | XLRE | +0.14% |
| Industrials | XLI | +0.14% |
| Financials | XLF | +0.07% |
| Materials | XLB | -0.56% |
| Utilities | XLU | -1.07% |
| Consumer Staples | XLP | -1.06% |
| Energy | XLE | **-2.88%** |

**Energy was the sole notable sector decliner**, a direct mirror of the oil selloff — MT Newswires reported the NYSE Energy Sector Index down 1.7% and XLE down 1.8% in late-afternoon trading (a smaller move than the tearsheet's full-day -2.88%, consistent with further weakness into the close). No idiosyncratic energy-stock catalyst surfaced in this run's searches beyond the crude-price read-through.

### Rest of world: broadly higher, led by Asia's chip-exposed markets

*Source: Bigdata.com market tearsheet (FMP); Albuquerque Journal/AP, WKYC/AP, Morningstar, all September 21, 2026.*

| Index | 1D |
|---|---|
| KOSPI (South Korea) | +1.65% |
| Hang Seng (Hong Kong) | +1.18% |
| Nikkei 225 (Japan) | +1.38% |
| DAX 40 (Germany) | +1.36% |
| Euro Stoxx 50 | +1.50% |
| CAC 40 (France) | +0.92% |
| FTSE 100 (UK) | +0.73% |
| TWSE (TAIEX, Taiwan) | +1.14% |
| FTSE MIB (Italy) | -1.60% |

AP's wire framing (Albuquerque Journal, WKYC) was explicit that the same mechanism — oil and Treasury yields "giving back some of last week's jumps" — lifted indexes "more than 1% from Germany to Hong Kong to South Korea." iShares MSCI country-ETF proxies in the tearsheet show South Korea (EWY, +4.33%) and Taiwan (EWT, +3.58%) as the largest single-day country movers globally, both carrying heavy semiconductor weightings (Samsung/SK Hynix, TSMC) that rode the same chip rally lifting US tech. FTSE MIB was a standout laggard against an otherwise uniformly positive European tape; no distinct Italy-specific catalyst surfaced in this run's searches.

---

## Rates

*Source: Bigdata.com market tearsheet (FMP); Albuquerque Journal/AP, WKYC/AP; Alpha Vantage `TREASURY_YIELD` for freshness cross-check.*

| Maturity | Yield | 1D change |
|---|---|---|
| 1 Month | 3.96% | -0.25% |
| 3 Month | 4.17% | +0.72% |
| 6 Month | 4.27% | +0.71% |
| 1 Year | 4.45% | +0.23% |
| 2 Year | 4.76% | +0.00% |
| 5 Year | 4.83% | -0.62% |
| 10 Year | 4.96% | -1.00% |
| 20 Year | 5.33% | -0.93% |
| 30 Year | 5.29% | -0.94% |

*("1D change" is the relative change in the yield level, per Bigdata.com/FMP, not basis points.)*

The curve eased from the front-intermediate belly out to the long end (5s through 30s all down on the day) while the very front end (1Y, 2Y) held roughly flat — consistent with a market pricing out some of last week's inflation-risk premium (oil-driven) rather than pricing out the Fed's hiking cycle itself. AP wire prints put the 10-year specifically at **4.95–4.96%**, down from Friday's brief push just above 5% — its highest since 2007. **Freshness cross-check:** Alpha Vantage's `TREASURY_YIELD` daily series remains stale — most recent print dated **September 17 (4.94%)**, four calendar days (two trading sessions) behind today, continuing the pattern flagged in every report since 9/14. Directionally consistent with today's tearsheet/wire level, not used as a same-day figure.

---

## Commodities

### Energy — the day's biggest cross-asset trigger; see the trigger section above for the WTI sourcing discrepancy

| Commodity | Price | 1D (Bigdata.com/FMP) | Wire-sourced close |
|---|---|---|---|
| WTI Crude | $92.37 | -3.86% | ~$95.48–$95.78, -4.5% to -4.8% (CNBC, Nasdaq/RTTNews, MT Newswires) |
| Brent Crude | $100.34 | -3.40% | ~$100.16–$100.34, -3.4% to -3.6% (CNBC, MT Newswires) — consistent |
| Natural Gas | $2.83 | -2.85% | — |
| Gasoline RBOB | $3.17 | -2.51% | — |
| Heating Oil | $4.70 | -3.06% | — |

### Metals — gold and silver both fell despite easing yields; dollar strength and Fed-hike odds are the more direct driver today

| Metal | Price | 1D |
|---|---|---|
| Gold Futures | $4,383.90 | -0.93% |
| Silver Futures | $66.53 | -0.92% |
| Platinum | $1,805.50 | -0.05% |
| Palladium | $1,319.50 | +0.00% |
| Copper | $6.79/lb | +1.50% |

Multiple wires (RTTNews/Nasdaq, The Economic Times, FXStreet) attribute gold's decline to a firmer dollar (index ~100.2–100.3) and continued elevated odds of an October Fed hike — cited variously as 54–56.5% (CME FedWatch, per Chinese-language wires) up to 88% (per The Economic Times) depending on source and snapshot time, a real dispersion worth noting rather than picking one figure. CNBC Arabia's close-of-day read had spot gold at $4,349.94 (-0.6%), after an intraday low near $4,322 — a wider range than the futures-based tearsheet figure above, consistent with ordinary intraday-vs-settlement timing differences. One Flush Financial Services Network note flagged that gold's decline was cushioned by continued official/ETF buying (SPDR holdings +4.28 tons on the day; central banks bought a net 289 tonnes in Q2) — offered as a data point from a single source, not independently corroborated in this run.

### Agricultural and other — Lean Hogs the day's most extreme move, unexplained

**Lean Hogs futures -10.63%** was the single largest move on the full tearsheet, outside crypto — no distinct catalyst surfaced in this run's searches (none were run specifically on livestock/hogs, given the day's three larger cross-asset stories taking priority per the one-search-per-theme discipline). Orange Juice (+4.97%), Corn (+2.94%), Cotton (+2.85%), and Live/Feeder Cattle (+2.7–2.8%) were the next-largest agricultural movers, also without an attributed cause in this run.

---

## Crypto

*Source: Bigdata.com tearsheet (9 of 15 watchlist pairs) and Twelve Data (remaining 6 pairs). See the trigger section above for the driving narrative.*

| Asset | Price | 1D | Source |
|---|---|---|---|
| Bitcoin (BTC) | $86,730.17 | **+6.86%** | Bigdata.com tearsheet |
| Ethereum (ETH) | $2,774.49 | +4.90% | Bigdata.com tearsheet |
| Solana (SOL) | $119.44 | **+7.46%** | Bigdata.com tearsheet |
| XRP | $1.53 | **+8.63%** | Bigdata.com tearsheet |
| Cardano (ADA) | $0.25 | **+7.68%** | Bigdata.com tearsheet |
| Dogecoin (DOGE) | $0.10 | **+13.75%** | Bigdata.com tearsheet |
| Avalanche (AVAX) | $11.29 | -0.36% | Bigdata.com tearsheet |
| Chainlink (LINK) | $13.15 | **+5.11%** | Bigdata.com tearsheet |
| Litecoin (LTC) | $62.39 | **+6.22%** | Bigdata.com tearsheet |
| Stellar (XLM) | $0.2147 | **+8.87%** | Twelve Data |
| Bitcoin Cash (BCH) | $269.10 | **+6.45%** | Twelve Data |
| Hedera (HBAR) | $0.09278 | **+7.22%** | Twelve Data |
| Sui (SUI) | $1.0188 | **+13.53%** | Twelve Data |
| Shiba Inu (SHIB) | $0.00000598 | **+8.73%** | Twelve Data |
| **Zcash (ZEC)** | **$1,456.00** | **-3.52%** | Twelve Data |

Bitcoin traded as high as $86,114–$87,000 intraday depending on source/snapshot (Geo TV, Yahoo! Finance) before settling near $86,500–86,730; MT Newswires' CoinMarketCap-sourced read has BTC +6.5% to $86,502 as of ~4:00 PM ET, broadly consistent with the tearsheet figure above. **Three watchlist positions didn't clear the book's 5% alert threshold: Ethereum (ETH, +4.90%, just under), Avalanche (AVAX, -0.36%), and Zcash (ZEC, -3.52%)** — the latter two genuine outliers against an otherwise uniformly strong session. AVAX had an outsized +51% 5-day move already on the tearsheet, so today's flat print may be consolidation after that run. Zcash is a repeat laggard: the September 18 report flagged ZEC as the sole non-breaching position that day too, following back-to-back >10% gains on 9/16–9/17 — today's outright decline extends that same post-rally cooling pattern rather than reversing it. No distinct catalyst for AVAX's or ZEC's underperformance surfaced in this run's searches.

---

## Portfolio read (`analyst/watchlist.yaml`)

*Twelve Data `get_price`/`get_quote` calls, paced in small batches through the evening UTC to stay under the connector's 8-credit/minute cap — the batched comma-separated `get_price` call is still broken this session ("does not support CSV format"), consistent with every prior report since 9/14.*

### GEXC options-flow book (21 names, 3% threshold) — 5 of 21 breached

| Symbol | 1D | Symbol | 1D | Symbol | 1D |
|---|---|---|---|---|---|
| AAPL | +0.82% | INTC | **+12.14%** | ORCL | +0.67% |
| AMD | **+9.92%** | META | **+11.32%** | PFE | +0.29% |
| AMZN | +1.86% | MSFT | +1.59% | PLTR | **+3.06%** |
| AVGO | +1.38% | MU | +2.71% | TSLA | **+3.03%** |
| BABA | +2.23% | NFLX | +2.19% | TSM | +2.41% |
| BAC | +0.42% | NOK | +2.48% | | |
| GOOG | +1.94% | NVDA | +2.24% | | |
| GOOGL | +1.62% | | | | |
| HOOD | +2.89% | | | | |

Bold = breached the 3% threshold.
- **INTC (Intel) +12.14%** and **META (Meta Platforms) +11.32%** are the book's two standout movers — Intel rode the same semiconductor rally described above (ARM/Intel both +13% intraday per multiple wires); no distinct Meta-specific catalyst surfaced in this run's searches beyond the broad tech/AI-optimism tailwind (Meta was cited among the day's "major tech giants" gainers, up over 6% in one intraday Sohu/Sina snapshot, before extending further into the close per this quote).
- **AMD +9.92%** — the AMD $1 trillion market-cap story detailed in the Equities section above.
- **PLTR +3.06%** and **TSLA +3.03%** cleared the threshold narrowly; both track the broad risk-on tape with no distinct single-name catalyst surfacing in this run's searches.
- **HOOD (Robinhood) +2.89%** sits just under threshold but is worth noting given crypto-linked-equity participation in today's Bitcoin rally, a repeat pattern from the 9/18 report. **MU +2.71%** and the rest of the book (AAPL, AMZN, AVGO, BABA, BAC, GOOG, GOOGL, MSFT, NFLX, NOK, NVDA, ORCL, PFE, TSM) posted small-to-moderate gains, none past threshold.

### MOVERS bot daily picks (14 names, 4% threshold)

Today's rotation: SNDK, CHPT, AGCO, NRG, SOXL, MRVL, CEG, KLAC, RIOT, STX, KNX, FOUR, ENTG, VST.

| Symbol | 1D | Symbol | 1D | Symbol | 1D |
|---|---|---|---|---|---|
| SNDK | -1.44% | CEG | +2.91% | ENTG | +0.65% |
| CHPT | **-8.72%** | KLAC | +3.94% | VST | +0.06% |
| AGCO | +0.11% | RIOT | +1.77% | | |
| NRG | -0.42% | STX | +2.17% | | |
| SOXL | **+14.85%** | KNX | -0.09% | | |
| MRVL | **+5.36%** | FOUR | +1.00% | | |

Bold = breached the 4% threshold. **3 of 14 breached today**, a much quieter book than the GEXC list.
- **SOXL (3x-leveraged semiconductor ETF) +14.85%** moves mechanically ~3x its underlying index — consistent with the Philadelphia Semiconductor Index's rally described above, not an idiosyncratic signal.
- **MRVL (Marvell) +5.36%** rides the same semiconductor rally as AVGO, MU, and KLAC in the other two books; no distinct Marvell-specific headline surfaced in this run's searches beyond the sector tailwind.
- **CHPT (ChargePoint) -8.72%** is the day's most notable decliner across the entire portfolio — a sharp move against a broadly rallying tape; no distinct ChargePoint-specific catalyst surfaced in this run's searches (none were run specifically on ChargePoint, given the day's three larger cross-asset stories taking priority per the one-search-per-theme discipline).
- **SNDK (SanDisk) -1.44%** is a mild laggard worth flagging given SanDisk's outsized prior run (part of the memory-chip cohort that rallied hard on 9/18); today's pullback may be idiosyncratic profit-taking rather than a reversal of the broader chip trade, but no distinct catalyst surfaced in this run's searches either.
- **RIOT (Riot Platforms) +1.77%** is notably muted for a crypto-mining name given Bitcoin's +6.86% session — a departure from the tight RIOT/BTC correlation flagged in the 9/18 report (RIOT +8.52% that day on a comparable BTC move); no distinct catalyst surfaced in this run's searches to explain the decoupling.
- The remaining names (AGCO, NRG, KLAC, STX, KNX, FOUR, ENTG, VST) posted small moves in line with the broad tape, none past threshold.

### Index proxies (2% threshold) — 1 of 3 breached

| Symbol | 1D | Source |
|---|---|---|
| $SPX | +1.49% | Bigdata.com tearsheet |
| SPY | +1.55% | Twelve Data |
| QQQ | **+2.77%** | Twelve Data |

SPY and the underlying S&P 500 index track closely (+1.55% vs. +1.49%, a normal small gap from snapshot timing), and both sit just under the 2% threshold. QQQ's larger move breaches it, mirroring the Nasdaq 100's semiconductor-led rally described in Equities above.

### Crypto book (15 names, 5% threshold) — 12 of 15 breached

See the Crypto section above for full detail. **Ethereum (ETH, +4.90%), Avalanche (AVAX, -0.36%), and Zcash (ZEC, -3.52%) did not breach** — ETH missed by a hair, while AVAX and ZEC were outright negative on a day when every other crypto position gained 6.2% or more. Litecoin (+6.22%) sits just above threshold; every other breaching name gained 6.4% or more, several (DOGE +13.75%, SUI +13.53%, XRP +8.63%) by a wide margin.

---

## Portfolio summary: 21 of 53 tracked positions breached their alert threshold today

A broad risk-on session shows up as a broad set of breaches: the crypto book breached almost uniformly (12/15), while the equity books were more selective — GEXC breached 5/21 (the threshold there is a tight 3%, and today's gains, while broad, mostly landed in the 1-3% range short of it) and the index proxies breached 1/3 (QQQ only). The MOVERS book breached 3/14 (CHPT, SOXL, MRVL), skewed toward the semiconductor names and one sharp decliner rather than a uniform move. The two most notable negative outliers in the whole portfolio — **CHPT (-8.72%)** and **ZEC (-3.52%)** — both lack an identified catalyst in this run's searches and are worth a scoped follow-up.

---

## Risks to watch

- **Whether today's rally is durable or a one-day relief bounce.** AOL.com's own framing of the crypto move was explicit: sustainability hinges on oil prices staying low through quarter-end (September 30) and Bitcoin holding above its $81,159 weekly close — a reversal in either would call the move into question. Yahoo! Finance separately cited Morgan Stanley's warning that the S&P 500 could still drop as much as 7% if energy prices rise again and the 10-year yield returns to ~5%.
- **This week's Trump-Xi summit (expected September 23–25) and the new US-China AI dialogue mechanism** announced after Sunday's Bessent–He Lifeng meeting — a real catalyst behind today's tech rally that could cut either way depending on the summit's outcome.
- **Whether the Trump-Pezeshkian meeting at the UN General Assembly this week actually happens and produces anything** — today's oil/yields move is priced on the *prospect* of diplomacy, not a concluded deal; Iran's own officials (parliament speaker, IRGC) struck a more guarded tone than US officials, and fighting involving Iran-backed Houthis and Saudi forces continues.
- **October Fed meeting odds** — cited variously as 54–56.5% (CME FedWatch per several sources) for a 25bp hike, a meaningful probability that's already weighing on gold even as equities and crypto shrugged off the same rate-path risk today.
- **The WTI tearsheet-vs-wire sourcing discrepancy** flagged in the trigger section — resolve which figure is accurate before using today's WTI 1D move in any downstream calculation; this is now the third report in two weeks (see also 9/18) to flag a WTI gap of this kind.
- **CHPT (ChargePoint) and ZEC (Zcash)'s uncaught declines** — both moved against the broad tape with no catalyst surfaced in this run; worth a scoped follow-up search before next check-in.
- **RIOT's decoupling from Bitcoin today** (+1.77% vs. BTC's +6.86%, a much looser correlation than its historical pattern with the underlying) — worth watching whether this persists.

---

## Connector status this run

All five of the fund's named connectors (Bigdata.com, Twelve Data, Alpha Vantage, Blockscout, Quartr) were confirmed available as callable tools this session.

- **Twelve Data:** the documented 8-credit/minute free-tier cap held throughout — the batched comma-separated `get_price` call is still broken ("does not support CSV format," the same error documented in every report since 9/14). Individual `get_quote`/`get_price` calls succeeded for all 37 equity/ETF symbols and all 6 remaining crypto pairs, but pacing required repeated waits (rate-limit errors hit roughly a dozen times over the course of this run before calls cleared); failed attempts appeared to still count against the per-minute quota in this session, which is a new observation worth flagging for future runs — budget more wall-clock time than the 9/18 report's ~65-second-batches-of-6 pattern assumed.
- **Alpha Vantage:** `TREASURY_YIELD`'s daily series remains stale (most recent print September 17, four calendar days behind today's session), continuing the pattern flagged in every report since 9/14. Directionally consistent with today's tearsheet/wire level, not used as a same-day figure. One credit spent; none spent elsewhere given the connector's daily cap and its better fit for options/macro data than same-day cross-asset levels already covered by Bigdata.com.
- **Bigdata.com:** no failures this run. One data-quality issue flagged rather than silently resolved — see the WTI tearsheet-vs-wire discrepancy in the trigger section.
- **Blockscout and Quartr:** confirmed available as callable tools this session but not invoked — no on-chain or filing-level question came up in today's research.

No data point in this report was filled in from general training knowledge in place of a failed or gated connector call. Items reported without an attributed cause because no distinct catalyst surfaced in this run's searches: CHPT's -8.72% move, ZEC's -3.52% move, RIOT's muted +1.77% (against BTC's +6.86%), Lean Hogs' -10.63% move, and several smaller individual moves noted inline above — each gap is stated explicitly rather than papered over with a plausible-sounding guess.

---

## Sources

Market levels and cross-asset data: [Bigdata.com](https://bigdata.com) market tearsheet (sourced from FMP), as of ~8:00–9:33 PM UTC, September 21, 2026. Individual equity and crypto-pair quotes not carried by the tearsheet: Twelve Data `get_quote`/`get_price` (real-time, per-symbol calls), pulled through the evening UTC. Treasury-yield freshness check: Alpha Vantage `TREASURY_YIELD` (found stale, most recent print September 17). News, causal narrative, and analyst commentary: Bigdata.com news search, aggregating Benzinga, Yahoo! Finance, Yahoo! News, Zacks.com, MSN, Albuquerque Journal (AP), WKYC News (AP), CNBC.com, CNBC Arabia, Nasdaq (RTTNews), MT Newswires (Global Energy and general), Alliance News, FXStreet News, The Globe and Mail, AOL.com, International Business Times, Livemint, Moneycontrol.com, The American Bazaar, Geo TV, The Economic Times, Epoch Times, NTD, Crypto Briefing, Sina (新浪), Sohu, Eastmoney (东方财富网), Today's Headlines (今日头条), Sina Finance (财经_手机新浪网), Securities Times, Credit Protection Association, Flush Financial Services Network, Morningstar, BQ Prime, and Financial News (파이낸셜뉴스), all published September 21, 2026. Watchlist: `analyst/watchlist.yaml`.

