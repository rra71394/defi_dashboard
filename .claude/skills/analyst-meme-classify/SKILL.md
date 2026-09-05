---
name: analyst-meme-classify
description: "Classifies meme-coin candidates that already cleared trading_agent's mechanical scan (meme_scanner.py) and on-chain verification (meme_verify.py) into a pattern label — KEEPER-SHAPED, MULTI-BAGGER-SHAPED, or QUICK-FLIP-OR-PASS — with sourced narrative context. Reads /root/trading_agent/meme_hits.json and meme_verified.json directly (same droplet). Use when asked to classify meme coin candidates, 'what do you think of these', or triggered by /analyst-meme-classify. DISCOVERY/RESEARCH ONLY — never a buy/sell instruction or a price prediction; real execution stays manual (Phantom/Core wallets), not automated."
---

# Meme coin candidate classification

You are adding the ONE thing trading_agent's mechanical pipeline can't do:
judgment about what a project actually IS, not just whether its numbers clear
a threshold. The scanner already checked size/age/activity; the verifier
already checked holder concentration, contract verification, and LP-lock
where applicable. Don't re-derive any of that — read it and build on it.

## Before you start

Read, if you haven't already this session:
- `analyst/GUARDRAILS.md` — the "no unearned conviction" rule applies MORE
  here than anywhere else in this repo. A label on this skill is a PATTERN
  MATCH against a checklist, never a prediction. Never write "will multi-bag"
  or give a price target — that requires separate explicit fund approval per
  GUARDRAILS.md and this skill does not have it.
- `analyst/CONNECTORS.md` — `bigdata_search` is the tool for "is there a real
  narrative here" questions; it has no dedicated meme-coin coverage, so
  results may be thin for a very new/small token. Say so rather than padding.
- `/root/trading_agent/meme_hits.json` (the scanner's mechanical pass) and
  `/root/trading_agent/meme_verified.json` (the on-chain verification pass) —
  read both in full before classifying anything. If either file is missing or
  stale (check its own timestamp field), say so and stop rather than guessing.

## What to do

1. **Join the two files** by token name/address. A candidate in `meme_hits.json`
   without a matching entry in `meme_verified.json` hasn't been on-chain
   checked yet — say so explicitly, don't classify it as if it had been.

2. **Read every flag already raised**, verbatim, before forming your own view:
   - Holder concentration (`top_n_pct_excl_pool` vs the 30% threshold)
   - Contract verification (`contract_verified`)
   - LP lock (`lp_lock.applicable` / `lp_lock.locked` — most current
     candidates will show `applicable: false`, meaning the pool is a
     concentrated-liquidity (V3-style) pool with no simple LP-lock check;
     that is NOT the same as "LP is unlocked" — say which one it is)
   - Data-quality issues (a token whose on-chain data is internally
     inconsistent, or a chain this checker doesn't cover yet, e.g. Solana)
     cannot be meaningfully classified — say so, don't force a label.

3. **One scoped `bigdata_search`** per candidate (name + "crypto" or the
   chain, last 7 days) for narrative context: is there a real project behind
   the ticker, a recognizable meme genre it's riding (animal coin, AI coin,
   tokenized-stock pairing per the founder's own $CHUMP/AMC example), or does
   it read as a copy-paste template with no distinct identity? If the search
   surfaces nothing, say "no narrative signal found" — that is itself
   information (very new/thin coverage), not a failed search to hide.

4. **Classify into one label per candidate**, each requiring BOTH an
   on-chain basis and a narrative basis — never label on numbers alone:
   - **KEEPER-SHAPED** — clean on-chain profile (verified, holder
     concentration under threshold, no data-quality issues) AND a real,
     sourced narrative distinct from a generic template.
   - **MULTI-BAGGER-SHAPED** — clean-to-mixed on-chain profile, smaller
     mcap, riding a narrative that looks early/fresh rather than already
     crowded. Higher variance is the tradeoff for the upside case; say that
     plainly rather than only naming the upside.
   - **QUICK-FLIP-OR-PASS** — any real on-chain flag (concentration,
     unverified, confirmed-unlocked LP), OR a narrative that reads as
     exhausted/copy-paste/no distinct identity, OR insufficient data to
     check either side.

5. **Output, per candidate, in this order**: name/chain -> label -> the
   on-chain basis (cite the actual numbers) -> the narrative basis (cite the
   source, or say none was found) -> one line on what would change the label
   (e.g. "would move to KEEPER-SHAPED if holder concentration drops under
   30%"). This is what makes the label a working tool instead of a verdict.

6. Never rank candidates against each other or imply an order to buy them in
   — that crosses from classification into a recommendation, which is outside
   this skill's guardrail.

Do not write a file for this skill by default, same as `analyst-watchlist-check`
— it's meant to be read in the moment. Only save to `reports/` if asked, or if
scheduled per `analyst/ARCHITECTURE.md`.
