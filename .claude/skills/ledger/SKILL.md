---
name: ledger
description: Walk scenes in reading order, build or update the setup/payoff ledger and the arc tracker.
argument-hint: "[scope] — e.g. chapter Mysterious Rhymes, part Your Aunt Buffing up a Groundhog, manuscript"
---

# /ledger — Claude Code adapter

Implements the novel-writing syndicate `ledger` command.

The canonical, tool-agnostic spec lives at:
`syndicates/novel-writing/commands/ledger.md`
(→ `~/Development/anthro/syndicates/novel-writing`, the one source of truth)

Read that spec and follow it exactly. This file holds no
logic of its own — it exists only to expose the command as
a Claude Code skill. All behaviour, forte lineup, and
governance come from the spec; if the spec and this adapter
ever disagree, the spec wins.

Scope argument: $ARGUMENTS
