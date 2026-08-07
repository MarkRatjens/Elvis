---
name: revise
description: Fire prose-scribe in correction mode to apply approved fixes to existing prose. Minimum alteration, zero additions.
argument-hint: "[scope] [title]  — e.g. scene Sarah celebrates her promotion"
---

# /revise — Claude Code adapter

Implements the novel-writing syndicate `revise` command.

The canonical, tool-agnostic spec lives at:
`syndicates/novel-writing/commands/revise.md`
(→ `~/Development/anthro/syndicates/novel-writing`, the one source of truth)

Read that spec and follow it exactly. This file holds no
logic of its own — it exists only to expose the command as
a Claude Code skill. All behaviour, forte lineup, and
governance come from the spec; if the spec and this adapter
ever disagree, the spec wins.

Scope / target argument: $ARGUMENTS
