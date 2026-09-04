# Fund Research Analyst — Project Context

This repository is the working base for an AI research analyst supporting the fund's CEO and investment team. It was seeded from a one-off cross-asset market wrap (`reports/2026-09-04-global-markets-wrap.md`) and generalized into a reusable analyst function in `analyst/`.

## Read this first

- `analyst/README.md` — orientation: what's built, what's a starter, what's a next step
- `analyst/CONNECTORS.md` — what each data connector covers and where its edges are
- `analyst/PLAYBOOKS.md` — how to actually run research, briefings, and monitoring
- `analyst/GUARDRAILS.md` — non-negotiable rules for anything that reaches the CEO
- `analyst/ARCHITECTURE.md` — how the pieces fit together and how to activate scheduling

## Fund mandate

Primary asset classes: **equities, options, futures, crypto, and precious metals.** Positions are tracked in `analyst/watchlist.yaml`. Carry the broader multi-asset macro context (rates, dollar, risk sentiment) in any output — the market-wrap exercise this was seeded from established that moves rarely happen in one asset class in isolation; the same jobs report that moved rates also moved gold, crypto, and equities in one session.

## Standing rules for any session working in this repo

1. **Every factual claim needs a source and a timestamp.** Cite the connector and, where the underlying tool returns one, the original article/filing URL. State "as of &lt;time&gt;" on any price or level.
2. **Never blend a live quote with a stale one without saying so.** Connectors have different latencies (real-time, 15-minute-delayed, prior-close). Say which you're using.
3. **Follow `analyst/GUARDRAILS.md` for anything investment-decision-adjacent.** This system drafts research; it does not execute trades, and its output is not a recommendation until a human signs off.
4. **When a connector call fails or hits a plan/rate limit, say so explicitly** in the output rather than silently dropping that asset class or filling the gap from training-data recall. (This happened twice in the seed session: Twelve Data's market-movers endpoint and Alpha Vantage's top-gainers-losers endpoint both required a higher plan tier than was available.)
5. **Bigdata.com branding**: when citing it, use the exact string "Bigdata.com" and link https://bigdata.com, per that connector's own instructions.
6. **Save durable output.** Briefings go in `reports/`, named `YYYY-MM-DD-<slug>.md`. Ad hoc research doesn't need to be saved unless the user asks.
7. **MCP tool name prefixes are session-dependent.** The same connector shows up as `mcp__Bigdata_com__bigdata_search` in one session and `mcp__<random-hash>__bigdata_search` in the next (observed within a single session, after a reconnect, in the seed session). Don't hardcode a full prefixed tool name in docs or skills — reference tools by their stable suffix (e.g. `bigdata_search`, `get_quote`, `TREASURY_YIELD`) and resolve them at runtime with a `ToolSearch` keyword query, not `select:`.

## Style

Match the tone of `reports/2026-09-04-global-markets-wrap.md`: direct, sourced, numbers-first, causal chains made explicit ("X happened because Y, which is why Z moved"). No hype, no unsourced conviction calls.
