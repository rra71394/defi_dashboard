---
name: analyst-brief
description: "Generate the fund's full cross-asset market briefing — equities, options, futures, crypto, and precious metals, with macro/rates context, plus a portfolio-specific pass over the fund's watchlist. Use when asked for a market update, daily/weekly briefing, market wrap, end-of-day/week summary, or 'what happened in markets today/this week'. Produces the same shape of output as reports/2026-09-04-global-markets-wrap.md. Not for a single ad hoc question (use analyst-research) or a fast position-only check (use analyst-watchlist-check). Triggered by /analyst-brief."
---

# Analyst briefing

You are producing a full market briefing for the fund's CEO, in the tradition of `reports/2026-09-04-global-markets-wrap.md` — read that file once if you haven't, as the reference for tone, structure, and depth.

## Before you start

Read, if you haven't already this session:
- `analyst/PLAYBOOKS.md` §2 (Scheduled briefing) — the exact step sequence
- `analyst/CONNECTORS.md` — tool routing per asset class
- `analyst/GUARDRAILS.md` — sourcing, staleness, and audit-trail rules
- `analyst/watchlist.yaml` — the fund's tracked positions to fold into the portfolio section

## What to do

Follow `analyst/PLAYBOOKS.md` §2 exactly:
1. `bigdata_market_tearsheet` first, for the full cross-asset skeleton.
2. Identify the 3–5 biggest/most unusual moves.
3. One `bigdata_search` per move or shared theme (not one search per asset class if they share a root cause).
4. Cross-check headline numbers with a second connector where cheap to do so.
5. Layer in `analyst/watchlist.yaml` positions.
6. Write the report to `reports/YYYY-MM-DD-<slug>.md` (use today's actual date — check it, don't assume).
7. Offer a dashboard artifact only if the output is genuinely dashboard-shaped and will be read interactively — load `dataviz` and `artifact-design` skills first if you build one. A file-only briefing doesn't need one.

## Output requirements

- Lede/TL;DR first, then one section per asset class, then a dedicated portfolio section (or fold positions into their asset-class sections if that reads more naturally), then "risks to watch," then sources.
- Every number sourced and timestamped, per `analyst/GUARDRAILS.md`.
- If any connector failed or was gated during this run, say so in the report itself, not just in your own reasoning — the CEO reading the file later has no visibility into what you tried and couldn't get.
- End by telling the user where the file landed and, if you published one, the dashboard link.
