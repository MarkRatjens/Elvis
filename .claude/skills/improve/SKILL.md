---
name: improve
description: Read session learnings and propose modifications to forte and talent specs. Continuous improvement for the syndicate.
---

# /improve — Claude Code adapter

Implements the novel-writing syndicate `improve` command.

The canonical, tool-agnostic spec lives at:
`syndicates/novel-writing/commands/improve.md`
(→ `~/Development/anthro/syndicates/novel-writing`, the one source of truth)

Read that spec and follow it exactly. This file holds no
logic of its own — it exists only to expose the command as
a Claude Code skill. All behaviour, forte lineup, and
governance come from the spec; if the spec and this adapter
ever disagree, the spec wins.

Note: the spec proposes changes to the canonical specs in
the syndicate repo — edits land in the source of truth, not
in this adapter.

Argument(s), if any: $ARGUMENTS
