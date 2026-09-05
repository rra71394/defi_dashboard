---
name: analyst-watchlist-check
description: "Run a fast monitoring pass over the fund's watchlist (analyst/watchlist.yaml) — pulls a current level for every tracked position across equities, options, futures, crypto, and precious metals, flags any move past its configured alert threshold, and runs a scoped news check only on flagged names. Also writes a machine-readable signals cache that trading_agent's live bots read via research_guard.py, so this is not purely a human-facing report. Use for periodic position monitoring or when asked 'anything moving in the book', 'check the watchlist', 'any alerts'. Terse by design — not a full market wrap (use analyst-brief for that) and not a deep dive on one name (use analyst-research for that). Triggered by /analyst-watchlist-check."
---

# Watchlist monitoring pass

You are running a fast, cheap check over the fund's tracked positions — not writing a report. Most runs of this skill should produce a few lines of output, not a page.

## Before you start

Read, if you haven't already this session:
- `analyst/PLAYBOOKS.md` §3 (Watchlist monitoring) — the exact step sequence
- `analyst/CONNECTORS.md` — which connector to use per `asset_class`
- `analyst/watchlist.yaml` — the actual positions and their `alert_threshold_pct`

## What to do

Follow `analyst/PLAYBOOKS.md` §3:
1. Read every position in `analyst/watchlist.yaml`.
2. Pull a current level for each, using the connector that fits its `asset_class` (batch multi-symbol calls where the tool supports it, rather than one call per symbol).
3. Compute each move against its own `alert_threshold_pct` — thresholds are per-position, not uniform.
4. For positions that breached threshold only, run one scoped `bigdata_search` (that name, last 24h) to attach a reason.
5. Output format: one line per position. Breached positions get the move, a one-line reason (or "no news surfaced"), and a source link. Positions that didn't breach get just the number, no narrative.
6. If nothing breached, say so in one line — don't manufacture content to fill space.
7. If a connector call fails for a given position, say so on that position's line rather than dropping it silently — and do NOT invent a flag for it in step 8 below; a failed check is not a breach.
8. **Always write `/root/trading_agent/research_signals_cache.json`** (same droplet — a direct file write, not a `reports/` file, and not gated by "only if asked" like everything else in this skill). This is the ONLY way trading_agent's live bots (via `research_guard.py`) see that this skill ran at all. Exact shape, do not deviate from it:

   ```json
   {"fetched_at": 1788580632.0, "flags": {"NVDA": "Bigdata: -4.2% on guidance cut, sourced 2026-09-05 14:32 ET (https://...)"}}
   ```

   - `fetched_at` is a **Unix epoch number in seconds** (what Python's `time.time()` returns) — **not** an ISO date string. `research_guard.py` computes `time.time() - fetched_at` directly against this field; writing a string here silently breaks every downstream freshness check rather than raising an error.
   - `flags` has one entry per position that breached its threshold on THIS run only — symbol keys exactly as they appear in `watchlist.yaml` (e.g. `"$SPX"`, `"BTC/USD"`, `"NVDA"`), value = the same one-line reason + source you already produced for it in step 5.
   - A position that did not breach this run gets no key at all — this is a snapshot of current flags, not a full position dump.
   - If nothing breached (step 6), still write the file, with `"flags": {}` and the current `fetched_at` — this tells `research_guard.py` "checked, nothing to report right now" rather than leaving every bot reading a stale flag from whenever this last found something.
   - Overwrite the whole file every run. It is current state, not an accumulating log.

For the human-facing output in steps 1-6 (this skill's own response, and any `reports/` file): do not write to `reports/` by default — that's meant to be read in the moment. Only save there if the user asks, or if this run is scheduled per `analyst/ARCHITECTURE.md` (append/date-stamp rather than overwrite, per `analyst/GUARDRAILS.md` §6). Step 8's cache write is separate from this policy and happens every run regardless.
