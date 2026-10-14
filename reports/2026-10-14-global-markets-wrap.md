# Global Markets Wrap — October 14, 2026

**No report today. Research was stopped before it started: the connectors this briefing depends on for sourced news/narrative and reliable levels are down or gated, continuing the same unresolved pattern flagged in every scheduled session since October 2.**

## What was checked

Per the standing instruction to verify connector availability before doing any research (not fabricate from general knowledge if they're down):

| Connector | Status | Evidence |
|---|---|---|
| **Bigdata.com** | **Down** | `bigdata_market_tearsheet` returned: *"You've used up your credits. Go to [Bigdata](https://app.bigdata.com) to manage your account."* This is the playbook's required starting point (`PLAYBOOKS.md` §2.1 — "Start every briefing here") and the only connector with news/narrative search (`bigdata_search`). Same account-wide credit exhaustion reported on October 2, 5, 6, 7, 8, 9, 12, and 13 — now unresolved across at least nine trading-day sessions. |
| **Twelve Data** | **Down** | MCP server tools are not loaded this session — the connector requires interactive OAuth authorization that a non-interactive scheduled session cannot complete. Same gap flagged since September 25. |
| **Quartr** | **Down** | `search_companies` returned `"error":"subscription_required"` — the connected account (`stockoptionfunds@gmail.com`) has `"currentPlan":"none"`. Unchanged from October 9, 12, and 13. |
| **Alpha Vantage** | **Down for this run** | `NEWS_SENTIMENT` was rejected outright — *"This is a premium endpoint... subscribe to any of the premium plans"* — so this key has no news/narrative access at all. `GLOBAL_QUOTE` for AAPL also hit a rate limit this time (*"Please consider spreading out your free API requests more sparingly... 25 requests per day"*), worse than October 13 when one quote got through — no price data was retrievable at all on this pass. |
| **Blockscout** | Up, but budget-limited and on-chain-only | Session unlocked; a live `get_block_number` call succeeded (Ethereum block 26,193,455, 2026-10-14 21:33 UTC), but the free session budget is **7 of 8 calls remaining**, and a persistent notice confirms *all Blockscout MCP requests have required a PRO API key since 10/08/2026*. On-chain only (wallet/contract/transfer data) — no price levels, no news, and it alone can't support a cross-asset wrap. |

## Why this stops the brief rather than producing a thin one

A cross-asset wrap in this fund's style is built on causal chains ("X happened because Y, which is why Z moved") with every claim sourced and timestamped. With Bigdata.com's news search down, Quartr down, and Alpha Vantage's only narrative endpoint premium-gated (on top of its quote endpoint also being rate-limited on this pass), there is no connector left that can source a "why" for any move, and no connector left that can even reliably source a "what" (a level or price) outside of on-chain data. Publishing anything today would mean either fabricating numbers and causal narrative from general training knowledge — explicitly forbidden by this task and by `analyst/GUARDRAILS.md` §2 and §4 — or publishing nothing of substance, which isn't the product this briefing is meant to be. Today is also a regular Wednesday trading session (not a weekend/holiday thin-report case), so there is no legitimate "quiet session" reason to still file a short wrap.

## Action needed

- **Bigdata.com**: account needs a credit top-up or plan review at [Bigdata.com](https://bigdata.com) — unresolved since October 2, now affecting at least nine scheduled trading-day sessions.
- **Twelve Data**: needs interactive OAuth authorization (via the Twelve Data MCP connector settings) — not something this scheduled session can complete on its own.
- **Quartr**: needs an active Pro subscription on the connected account.
- **Alpha Vantage**: `NEWS_SENTIMENT` requires a premium plan on the connected key, and the free key's 25-requests/day cap is now blocking even single quote lookups.
- **Blockscout**: requires a PRO API key for sustained use (as of 2026-10-08) — the free per-session call budget (8 calls, 7 remaining as of today) is not enough to support a watchlist-scale monitoring pass going forward.

No market data, levels, or news claims are presented in this note — per standing instructions, nothing here should be read as a market update.
