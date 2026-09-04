---
name: analyst-watchlist-check
description: "Run a fast monitoring pass over the fund's watchlist (analyst/watchlist.yaml) — pulls a current level for every tracked position across equities, options, futures, crypto, and precious metals, flags any move past its configured alert threshold, and runs a scoped news check only on flagged names. Use for periodic position monitoring or when asked 'anything moving in the book', 'check the watchlist', 'any alerts'. Terse by design — not a full market wrap (use analyst-brief for that) and not a deep dive on one name (use analyst-research for that). Triggered by /analyst-watchlist-check."
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
7. If a connector call fails for a given position, say so on that position's line rather than dropping it silently.

Do not write a file for this skill by default — it's meant to be read in the moment. Only save to `reports/` if the user asks, or if this run is being driven by a scheduled job per `analyst/ARCHITECTURE.md` (in which case, append/date-stamp rather than overwrite, per `analyst/GUARDRAILS.md` §6).
