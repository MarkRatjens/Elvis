---
name: developmental
description: Full developmental edit — evaluate, propose changes, author approval gate, redraft, verify voice, deliver with change log.
argument-hint: "[scope] [title]  — e.g. scene Sarah celebrates, chapter Recidivist Grinds, scenes Recidivist Grinds"
---

# /developmental — Claude Code adapter

Implements the novel-writing syndicate `developmental` command.

The canonical, tool-agnostic spec lives at:
`syndicates/novel-writing/commands/developmental.md`
(→ `~/Development/anthro/syndicates/novel-writing`, the one source of truth)

Read that spec and follow it exactly. This file holds no
logic of its own — it exists only to expose the command as
a Claude Code skill. All behaviour, forte lineup, and
governance come from the spec; if the spec and this adapter
ever disagree, the spec wins.

Scope / target argument: $ARGUMENTS
