# Guardrails

Engineering-level rules for a system whose output can influence real capital decisions. This is not a substitute for the fund's actual compliance and legal review — treat it as the floor, not the ceiling, and have counsel sign off on the workflow before the CEO relies on it operationally.

## 1. This is decision *support*, not a decision-maker

Nothing in this repo places an order, rebalances a position, or has any execution capability — that's deliberate, not a missing feature. Every connector here is read-only market/research data. Keep it that way: if a future iteration ever adds a broker/execution connector, that's a categorically different risk profile and deserves its own explicit review, not a quiet extension of this scaffold.

Every briefing, research answer, and monitoring alert is a **draft for a human to evaluate**, not a recommendation to act on directly. Say so, plainly, in any output the CEO sees — don't bury it in a footer.

## 2. Sourcing is mandatory, not best-effort

Every factual claim — a price, a level, a "why," a filing detail — needs a named source and a timestamp. "The market is worried about X" is not a claim this system gets to make without a `bigdata_search` result (or equivalent) backing it. If you can't source a claim, don't make it; say what you don't know instead.

## 3. Staleness is a first-class fact, not a footnote

Connectors have genuinely different latencies — some real-time, some 15-minutes-delayed, some prior-close-only, some daily-refresh. Blending them without saying which is which produces a briefing that *looks* coherent and isn't. State "as of &lt;time&gt;" on every price or level, and flag explicitly when two numbers in the same output come from different points in time.

## 4. Failures are reported, never papered over

When a connector call fails, is gated behind a plan tier, or hits a rate limit, the output must say so by name (this happened twice in the seed session — see `CONNECTORS.md`). The failure mode to actively guard against is the system quietly substituting a plausible-sounding number from general training knowledge in place of a live data point that failed to load. That is worse than an obvious gap, because it's invisible to the reader.

## 5. No unearned conviction

Don't generate price targets, "buy/sell" language, or confidence-scored calls unless the fund explicitly designs and approves that capability separately, with its own methodology disclosed. This scaffold's job is to surface what happened, why, and what's at risk — not to manufacture alpha claims. If asked directly for a view, distinguish clearly between "here's what the data and the coverage say" and "here's a synthesis/opinion," and label the latter as such.

## 6. Keep an audit trail

Every scheduled briefing and every watchlist alert should be durable and timestamped — that's why `reports/` exists as a committed archive rather than ephemeral chat output. If the CEO acts on something this system produced, there should be a record of exactly what it said, sourced from what, and when. Don't let a scheduled job overwrite its own history; append or date-stamp, never replace.

## 7. Data quality reflects on providers by name

If Bigdata.com, Twelve Data, Alpha Vantage, Blockscout, or Quartr data conflicts, is missing, or is stale, name the specific connector rather than a vague "the data shows." This matters for two reasons: it lets a reader weigh confidence appropriately, and it's the accurate, fair way to attribute information sourced from a specific paid provider.

## 8. Human sign-off before anything leaves the building

If briefings or alerts are ever wired to reach the CEO directly (email, Slack, etc. — not yet built, see `ARCHITECTURE.md`), keep a human review step between generation and delivery until the fund has enough operating history with this system to trust it unsupervised. Start supervised; loosen deliberately, not by default.
