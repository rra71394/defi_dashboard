# Architecture

## How the pieces fit together

```
                     ┌─────────────────────────────────────────┐
                     │              CLAUDE.md                  │
                     │   (always-loaded project context,       │
                     │    standing rules, fund mandate)         │
                     └───────────────────┬───────────────────-─┘
                                          │
              ┌───────────────────────────┼───────────────────────────┐
              │                           │                           │
   .claude/skills/analyst-      .claude/skills/analyst-    .claude/skills/analyst-
   research/SKILL.md            brief/SKILL.md             watchlist-check/SKILL.md
   (on-demand copilot)          (scheduled full wrap)       (fast monitoring pass)
              │                           │                           │
              └───────────────┬───────────┴───────────────┬───────────┘
                               │                           │
                     analyst/PLAYBOOKS.md         analyst/watchlist.yaml
                     analyst/CONNECTORS.md         (the fund's tracked
                     analyst/GUARDRAILS.md          positions — currently
                     (shared reference,             example data)
                     read by all three skills)
                               │
              ┌────────────────┼────────────────┬───────────────┬──────────────┐
              │                │                │               │              │
        Bigdata.com      Twelve Data      Alpha Vantage     Blockscout       Quartr
     (news, tearsheets,  (quotes,         (options, macro,   (on-chain      (primary-source
      filings search)     technicals)      commodities)       verification)  filings/transcripts)
                               │
                    output → reports/YYYY-MM-DD-*.md
                    (+ optional published dashboard artifact)
```

The skills don't duplicate the connector catalog or the guardrails inline — they point at `analyst/CONNECTORS.md`, `analyst/PLAYBOOKS.md`, and `analyst/GUARDRAILS.md` so there's one place to update each, not five.

## Why a flat-file watchlist (for now)

`analyst/watchlist.yaml` is deliberately simple — a flat file a skill can read directly, no database, no service. Two real alternatives exist if this needs to grow:

- **Quartr's native watchlist/workspace primitives** (`create_watchlist`, `add_to_watchlist`, `create_workspace`) — worth using if the fund wants the watchlist to live where the equities research already lives, and is willing to make Quartr the system of record. Tradeoff: it only covers what Quartr covers (public equities), so options/futures/crypto/metals positions would still need something else.
- **A real database** — worth it once the watchlist needs concurrent writers, position history, or P&L tracking beyond "what's the current level and did it move." Not worth the complexity for a single-analyst, single-file starting point.

Start with the flat file. Migrate only when you feel the actual limitation, not preemptively.

## Activating scheduling

Today, all three skills run when invoked (`/analyst-research`, `/analyst-brief`, `/analyst-watchlist-check`) — nothing runs on its own yet. That's intentional: turning a briefing generator into an autonomous recurring job is a live, durable action, and it deserves an explicit decision on cadence and output handling, not a default.

Two mechanisms exist in this environment to make that jump once you've decided:

- **The `/loop` skill** — runs a prompt or slash command on a recurring interval, either fixed (`/loop 30m /analyst-watchlist-check`) or self-paced. Good fit for `analyst-watchlist-check` during market hours.
- **`CronCreate`** — schedules a trigger more durably (survives across sessions). Better fit for `analyst-brief` on a fixed daily/weekly cadence (e.g. once at US market close).

Before wiring either one, decide:
1. **Cadence** — how often is actually useful vs. how often burns API quota for no new signal (Alpha Vantage's rate limits in particular won't tolerate an aggressive watchlist-check interval across many symbols — see `CONNECTORS.md`).
2. **Where output goes.** Right now a scheduled run would still just commit a file to `reports/` — nothing pushes to the CEO's email or Slack, because no messaging connector is part of this connector set yet. Decide whether "committed to the repo, CEO checks it" is good enough, or whether a delivery channel needs to be added first.
3. **Supervision.** Per `GUARDRAILS.md` §8, start with a human reviewing scheduled output before it's treated as reliable enough to run fully unattended.

## Extension points

- **New watchlist position:** add a row to `analyst/watchlist.yaml`. No code change needed — all three skills read it at run time.
- **New connector:** add it to `analyst/CONNECTORS.md`'s coverage matrix and detail section first, so the routing logic in `PLAYBOOKS.md` stays accurate, then reference it from whichever skill(s) it fits.
- **New skill (e.g. a risk-limit checker, a correlation/exposure report):** follow the pattern in `.claude/skills/analyst-*` — a `SKILL.md` with clear frontmatter `description` (that's what makes it trigger correctly) pointing at the shared `analyst/*.md` references rather than re-stating them.

## Known open gaps (see also `CONNECTORS.md`)

- No equity-index or rates futures coverage from any connector.
- No delivery channel to the CEO beyond the repo itself.
- No real watchlist data yet — `watchlist.yaml` ships with clearly-marked examples.
- No compliance/legal sign-off — `GUARDRAILS.md` is an engineering floor, not a legal review.
