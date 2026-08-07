---
name: audit
description: Fire continuity-keeper and world-auditor to catch cross-scene contradictions across a chapter, part, or manuscript.
argument-hint: "[scope] [title]  — e.g. chapter Recidivist Grinds, part Uninvested"
---

# /audit — Claude Code adapter

Implements the novel-writing syndicate `audit` command.

The canonical, tool-agnostic spec lives at:
`syndicates/novel-writing/commands/audit.md`
(→ `~/Development/anthro/syndicates/novel-writing`, the one source of truth)

Read that spec and follow it exactly. This file holds no
logic of its own — it exists only to expose the command as
a Claude Code skill. All behaviour, forte lineup, and
governance come from the spec; if the spec and this adapter
ever disagree, the spec wins.

Scope / target argument: $ARGUMENTS
