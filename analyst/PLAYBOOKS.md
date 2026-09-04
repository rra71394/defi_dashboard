# Playbooks

Concrete, repeatable query sequences for each function. These are generalized directly from how `reports/2026-09-04-global-markets-wrap.md` was actually built — read that file alongside this one to see the pattern in its finished form.

## 1. Research copilot (`/analyst-research`)

Goal: answer one question, well-sourced, fast. Don't over-fetch.

1. **Classify the question** by asset class and by type:
   - *Level/price* ("what's X trading at", "how far is Y from its high") → a quote/price/time-series tool (Twelve Data `get_quote`/`get_price`, Alpha Vantage's asset-specific series, or Bigdata's tearsheet if it's a cross-asset context question).
   - *Driver/narrative* ("why did X move", "what's driving Y") → `bigdata_search`, smart mode, scoped to the relevant window. This is almost always the right tool for "why" questions — it's the only connector built for narrative retrieval.
   - *Fundamental/filing-level* ("what did the 10-K say about Z", "what did management say on the call") → Quartr (`search_companies` → `read_document`/`read_transcript`) or Bigdata's company tearsheet / document search with `document_type` filters.
   - *On-chain/crypto verification* ("does this protocol actually hold what it claims", "what's this wallet been doing") → Blockscout.
   - *Options-specific* → Alpha Vantage; no fallback exists if it's unavailable — say so rather than guessing from the underlying's price action.
2. **Resolve entities before structured calls.** Anything hitting a tearsheet or calendar tool needs an `rp_entity_id` (Bigdata `find_securities`) or a `companyId` (Quartr `search_companies`) first. Don't skip this and don't guess an ID.
3. **One focus per `bigdata_search` call.** A question spanning two entities, two time periods, or two aspects is two or more calls. This is a hard rule from the connector itself, not a style preference — violating it measurably degrades result relevance.
4. **Answer with sources inline**, not as a bibliography at the end unless the answer is long enough to need one. State the data's timestamp/"as of" explicitly.
5. **If a connector call fails or is gated** (see `CONNECTORS.md` gotchas), say so in the answer rather than silently falling back to general knowledge.

## 2. Scheduled briefing (`/analyst-brief`)

Goal: a full cross-asset wrap plus a portfolio-specific read, in the shape of `reports/2026-09-04-global-markets-wrap.md`.

1. **Start with `bigdata_market_tearsheet`.** One call gives you the whole cross-asset board — equities by country/sector/index, fixed income, the full yield curve, commodities, currencies incl. crypto, equity factors. This is your skeleton; everything else fills in the "why."
2. **Identify the day's 3–5 biggest or most unusual moves** from that tearsheet (biggest single-day mover, biggest weekly mover, anything that broke a multi-month level, anything inconsistent with the rest of its asset class).
3. **Run one `bigdata_search` per move/theme**, not one search for the whole day. If two moves share a root cause (e.g. a macro print moved rates, equities, and crypto together), one well-scoped search on the root cause plus one on any asset-class-specific wrinkle is enough — don't re-search the same catalyst four times.
4. **Cross-check numbers that matter with a second connector** where it's cheap to do so (e.g. a headline yield move via Alpha Vantage `TREASURY_YIELD`, a crypto price via Twelve Data) — the seed session found tearsheet and news-wire numbers agreed closely but not exactly (different snapshot times), which is normal; note the discrepancy rather than picking one arbitrarily.
5. **Layer in the portfolio.** Read `analyst/watchlist.yaml`; for each position, pull today's move and fold it into the relevant asset-class section, or add a short dedicated "Portfolio" section — whichever reads more naturally given how many positions moved materially.
6. **Write the report** to `reports/YYYY-MM-DD-<slug>.md` — lede/TL;DR first, then one section per asset class, then a "risks to watch" close, then sources.
7. **Optional: publish a dashboard artifact** for the same content if the audience will read it interactively (stat tiles, tables, causal-chain diagram) — see `dataviz` and `artifact-design` skills before building one. Don't build one for a briefing that's only ever going to be read as a file.

## 3. Watchlist monitoring (`/analyst-watchlist-check`)

Goal: cheap, frequent, terse. This is not a briefing — no narrative unless something actually breached a threshold.

1. Read `analyst/watchlist.yaml`.
2. For each position, pull a current level using the connector appropriate to its `asset_class` (see `CONNECTORS.md` coverage matrix) — batch multi-symbol calls where the tool supports it (e.g. Twelve Data's comma-separated `get_price`) instead of one call per symbol.
3. Compute the move against that position's `alert_threshold_pct`.
4. **Only for positions that breached their threshold**, run one scoped `bigdata_search` for that symbol/name over the last 24h to attach a reason.
5. Output a short flagged list: symbol, move, one-line reason (or "no news surfaced" if the search came back empty), source link. Positions that didn't breach threshold get one line with just the number — no narrative.
6. If nothing breached, say that plainly in one line. Don't pad a quiet check into a report.

## General rules that apply to all three

- Never present a number without knowing which connector it came from and how stale it might be.
- If a connector is down, gated, or rate-limited mid-run, name it and continue with what's available — don't fail silently or fabricate a fallback number.
- Prefer the connector with the tighter fit over the one that's merely available (e.g. Alpha Vantage for options over guessing from the underlying).
