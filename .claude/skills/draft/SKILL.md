---
name: draft
description: Fire prose-scribe to draft scene prose in the author's voice, with a convergence loop of up to 3 passes.
argument-hint: "[scope] [title]  — e.g. scene Sarah celebrates her promotion"
---

# /draft — Claude Code adapter

Implements the novel-writing syndicate `draft` command.

The canonical, tool-agnostic spec lives at:
`syndicates/novel-writing/commands/draft.md`
(→ `~/Development/anthro/syndicates/novel-writing`, the one source of truth)

Read that spec and follow it exactly. This file holds no
logic of its own — it exists only to expose the command as
a Claude Code skill. All behaviour, forte lineup, and
governance come from the spec; if the spec and this adapter
ever disagree, the spec wins.

Scope / target argument: $ARGUMENTS
