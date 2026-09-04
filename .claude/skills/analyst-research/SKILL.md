---
name: analyst-research
description: "On-demand research copilot for the fund. Use for any ad hoc market, company, sector, macro, or position question from the CEO or investment team — e.g. 'what's driving X', 'how exposed are we to Y', 'give me a read on Z', 'what did the Fed say about W', 'what's this wallet/protocol actually holding'. Routes the question to the right connector(s) (Bigdata.com, Twelve Data, Alpha Vantage, Blockscout, Quartr) and returns a sourced, dated answer. Not for full market wraps (use analyst-brief) or watchlist scans (use analyst-watchlist-check). Triggered by /analyst-research."
---

# Analyst research copilot

You are answering one research question for the fund's CEO or investment team, on demand. Depth should match the question — a quick level check gets a quick answer; a "what's driving X" question gets a sourced narrative.

## Before you start

Read, if you haven't already this session:
- `analyst/CONNECTORS.md` — which connector fits this question
- `analyst/PLAYBOOKS.md` §1 (Research copilot) — the routing and sourcing steps
- `analyst/GUARDRAILS.md` — sourcing, staleness, and no-unearned-conviction rules apply to every answer this skill produces

## What to do

1. Classify the question (level/price, driver/narrative, fundamental/filing, on-chain, options) and route it per `PLAYBOOKS.md` §1.
2. Resolve any entity IDs you need (`find_securities`, `search_companies`) before calling a structured tool that requires one.
3. Answer directly, with sources and timestamps inline. Don't pad a short answer to look thorough, and don't compress a genuinely multi-part answer just to be brief.
4. If the question touches a position in `analyst/watchlist.yaml`, say so and note the position's current status.
5. If a connector call fails or is gated, name it explicitly per `CLAUDE.md` rule 4 — don't quietly answer from general knowledge instead.
6. Distinguish sourced fact from your own synthesis if you're asked for a view, per `GUARDRAILS.md` §5.

No file output is required for this skill — answer in the conversation. Only write to `reports/` if the user asks you to save the answer.
