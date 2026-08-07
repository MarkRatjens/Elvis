---
name: session
description: Start or end a writing session. Loads context for the declared scope at the start, logs what happened at the end.
argument-hint: "start [scope] [mode] | end"
---

# /session — Claude Code adapter

Implements the novel-writing syndicate `session` command.

The canonical, tool-agnostic spec lives at:
`syndicates/novel-writing/commands/session.md`
(→ `~/Development/anthro/syndicates/novel-writing`, the one source of truth)

Read that spec and follow it exactly. This file holds no
logic of its own — it exists only to expose the command as
a Claude Code skill. All behaviour, forte lineup, and
governance come from the spec; if the spec and this adapter
ever disagree, the spec wins.

Argument: $ARGUMENTS
