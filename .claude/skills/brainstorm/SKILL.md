---
name: brainstorm
description: Explore plot possibilities for undrafted or stuck scenes — identify narrative gaps, propose options with consequences.
argument-hint: "[scope or thread] — e.g. part Uninvested, chapter 42, the disc mystery"
---

# /brainstorm — Claude Code adapter

Implements the novel-writing syndicate `brainstorm` command.

The canonical, tool-agnostic spec lives at:
`syndicates/novel-writing/commands/brainstorm.md`
(→ `~/Development/anthro/syndicates/novel-writing`, the one source of truth)

Read that spec and follow it exactly. This file holds no
logic of its own — it exists only to expose the command as
a Claude Code skill. All behaviour, forte lineup, and
governance come from the spec; if the spec and this adapter
ever disagree, the spec wins.

Scope / thread argument: $ARGUMENTS
