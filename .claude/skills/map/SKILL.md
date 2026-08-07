---
name: map
description: Parse the Scrivener binder and report manuscript maturity per scene, chapter, and part. No content read, no fortes fire.
---

# /map — Claude Code adapter

Implements the novel-writing syndicate `map` command.

The canonical, tool-agnostic spec lives at:
`syndicates/novel-writing/commands/map.md`
(→ `~/Development/anthro/syndicates/novel-writing`, the one source of truth)

Read that spec and follow it exactly. This file holds no
logic of its own — it exists only to expose the command as
a Claude Code skill. All behaviour, forte lineup, and
governance come from the spec; if the spec and this adapter
ever disagree, the spec wins.

Argument(s), if any: $ARGUMENTS
