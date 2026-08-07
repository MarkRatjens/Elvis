---
name: survey
description: Walk scenes extracting facts to the persistent knowledge base — fire continuity-keeper, character-warden, world-auditor in extraction mode. No evaluation.
argument-hint: "[scope] [title]  — e.g. chapter Mysterious Rhymes, part Your Aunt Buffing up a Groundhog"
---

# /survey — Claude Code adapter

Implements the novel-writing syndicate `survey` command.

The canonical, tool-agnostic spec lives at:
`syndicates/novel-writing/commands/survey.md`
(→ `~/Development/anthro/syndicates/novel-writing`, the one source of truth)

Read that spec and follow it exactly. This file holds no
logic of its own — it exists only to expose the command as
a Claude Code skill. All behaviour, forte lineup, and
governance come from the spec; if the spec and this adapter
ever disagree, the spec wins.

Scope / target argument: $ARGUMENTS
