---
name: read
description: Display scene, chapter, or part content from the Scrivener project. Read-only — no evaluation, no fortes.
argument-hint: "[scope] [title]  — e.g. scene Sarah celebrates her promotion, chapter Recidivist Grinds, part Uninvested"
---

# /read — Claude Code adapter

Implements the novel-writing syndicate `read` command.

The canonical, tool-agnostic spec lives at:
`syndicates/novel-writing/commands/read.md`
(→ `~/Development/anthro/syndicates/novel-writing`, the one source of truth)

Read that spec and follow it exactly. This file holds no
logic of its own — it exists only to expose the command as
a Claude Code skill. All behaviour, forte lineup, and
governance come from the spec; if the spec and this adapter
ever disagree, the spec wins.

Scope / target argument: $ARGUMENTS
