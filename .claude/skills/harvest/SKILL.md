---
name: harvest
description: Survey unfinished scenes by maturity and present what each asks of the author. Recognition, not ranking.
---

# /harvest — Claude Code adapter

Implements the novel-writing syndicate `harvest` command.

The canonical, tool-agnostic spec lives at:
`syndicates/novel-writing/commands/harvest.md`
(→ `~/Development/anthro/syndicates/novel-writing`, the one source of truth)

Read that spec and follow it exactly. This file holds no
logic of its own — it exists only to expose the command as
a Claude Code skill. All behaviour, forte lineup, and
governance come from the spec; if the spec and this adapter
ever disagree, the spec wins.

Argument(s), if any: $ARGUMENTS
