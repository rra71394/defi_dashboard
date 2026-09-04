# Fund Analyst — Handoff

Start here. This directory is the base for the fund's AI research analyst: an on-demand copilot, a scheduled briefing generator, and a watchlist monitor, all built on the connectors available in this environment (Bigdata.com, Twelve Data, Alpha Vantage, Blockscout, Quartr).

## What's actually here

| File | What it is |
|---|---|
| `CONNECTORS.md` | What each connector covers, mapped to the fund's asset classes and to the three functions below. Read this before wiring anything new. |
| `PLAYBOOKS.md` | The actual step-by-step query patterns for research, briefings, and monitoring — generalized from the September 4 market wrap. |
| `GUARDRAILS.md` | Rules that apply to anything that could influence a real investment decision. Non-negotiable. |
| `ARCHITECTURE.md` | How the three skills, the connectors, and the watchlist fit together, plus how to turn briefings/monitoring into scheduled jobs. |
| `watchlist.yaml` | The fund's tracked positions. **Currently example data — replace before relying on this for anything real.** |

## The three functions, as skills

| Skill | Invoke | Does |
|---|---|---|
| `analyst-research` | `/analyst-research <question>` | On-demand copilot — answers any market/company/macro question, sourced. |
| `analyst-brief` | `/analyst-brief` | Full cross-asset market wrap + a portfolio-specific pass over the watchlist. Same shape as `reports/2026-09-04-global-markets-wrap.md`. |
| `analyst-watchlist-check` | `/analyst-watchlist-check` | Fast pass over the watchlist only — flags positions that moved past their threshold, with a scoped news check on flagged names only. |

These live in `.claude/skills/`. They work today, invoked manually. They are **not yet scheduled** — see `ARCHITECTURE.md` for how to wire that up once you've decided on a cadence and where output should land.

## What this handoff does *not* include (by design — decide these before going live)

- **A real watchlist.** `watchlist.yaml` has illustrative example positions across all five asset classes so the skills have something to run against. Swap in real holdings.
- **A delivery channel to the CEO.** Right now output lands as a committed file in `reports/` and, optionally, a published dashboard link. Nothing pushes to email/Slack/etc. — none of today's connectors are a messaging channel.
- **Scheduling.** The briefing and monitoring skills run when invoked. Turning them into a recurring job (daily briefing at market close, watchlist check every N hours) is one `/loop` or `CronCreate` call away — see `ARCHITECTURE.md` — but that's a live, autonomous, recurring action, so it's left as an explicit next step rather than turned on by default.
- **Compliance/legal review.** `GUARDRAILS.md` states engineering-level guardrails (sourcing, staleness, no execution). It is not a substitute for your fund's actual compliance and legal sign-off on an AI-assisted research workflow.
- **Options-chain and equity-index-futures coverage** is thinner than the other asset classes across all five connectors — flagged in detail in `CONNECTORS.md`.

## Fastest way to see it work

Run `/analyst-research` with a real question, or `/analyst-watchlist-check` to see a monitoring pass over the example watchlist. Both work against live data right now, no setup required beyond what's already connected.
