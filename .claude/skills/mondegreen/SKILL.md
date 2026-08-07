---
name: mondegreen
description: Generate chapter title candidates as "Suspicious Minds" mondegreens, themed to the chapter's content.
argument-hint: "[chapter title]  — e.g. Recidivist Grinds"
---

# /mondegreen — Claude Code adapter

Implements the novel-writing syndicate `mondegreen` command.

The canonical, tool-agnostic spec lives at:
`syndicates/novel-writing/commands/mondegreen.md`
(→ `~/Development/anthro/syndicates/novel-writing`, the one source of truth)

Read that spec and follow it exactly. This file holds no
logic of its own — it exists only to expose the command as
a Claude Code skill. All behaviour, forte lineup, and
governance come from the spec; if the spec and this adapter
ever disagree, the spec wins.

Chapter argument: $ARGUMENTS
