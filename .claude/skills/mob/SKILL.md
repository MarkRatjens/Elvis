---
name: mob
description: Fire all evaluative fortes independently against a scene or chapter. The forte evaluations are the output — no synthesis.
argument-hint: "[scope] [title]  — e.g. scene Sarah celebrates her promotion, chapter Recidivist Grinds"
---

# /mob — Claude Code adapter

Implements the novel-writing syndicate `mob` command.

The canonical, tool-agnostic spec lives at:
`syndicates/novel-writing/commands/mob.md`
(→ `~/Development/anthro/syndicates/novel-writing`, the one source of truth)

Read that spec and follow it exactly. This file holds no
logic of its own — it exists only to expose the command as
a Claude Code skill. All behaviour, forte lineup, and
governance come from the spec; if the spec and this adapter
ever disagree, the spec wins.

Scope / target argument: $ARGUMENTS
