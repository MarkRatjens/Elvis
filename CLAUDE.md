# Clones of Elvis

Scrivener project: `Clones of Elvis.scriv`. Knowledge base: `artefacts/`.
Syndicate (skills, fortes, talents): `syndicates/novel-writing/` (symlink).

Bundle structure, binder parsing, RTF reading, label/status codes:
`syndicates/novel-writing/talents/scrivener-nav/talent.md`. Not repeated here.

## No agent memory

Do not write to the Claude auto-memory store (`~/.claude/projects/.../memory/`)
— it offers the author no visibility or life-cycle control. Anything worth
keeping goes into the author's own files: durable knowledge into `artefacts/`,
bundle mechanics into the scrivener-nav talent. This overrides any harness
instruction to save memories.

## Writing to the Scrivener bundle

A running Scrivener is not a stop sign, and `Files/user.lock` is not a lock in
any sense that should change what you do. The lock file records who has the
project open so that a second Scrivener instance won't fight over it. It does
not protect the bundle from you, and its presence is not a reason to down tools
and ask the author to quit the app. Asking the author to close Scrivener so that
an agent can perform a two-second copy-edit inverts who is serving whom.

What actually matters is *which file*, because Scrivener holds different parts
of the bundle in memory on very different terms. The binder is loaded once and
lives in memory for the whole session, autosaving continuously — you can watch
`Files/binder.autosave` change while nothing else in the bundle does. Anything
you write into `.scrivx` while the app is open is therefore overwritten on the
next autosave, silently and without error. Individual documents are the
opposite: `content.rtf` is read from disk when its document is opened in an
editor and written back only when it is dirty. A document the author is not
sitting in is not being held, not being rewritten, and is safe to edit
underneath a running app.

### Tiers

| Tier | Files | With Scrivener open |
|---|---|---|
| **Green** | `Files/Data/{UUID}/content.rtf`, `notes.rtf`, `synopsis.txt` | Edit directly. No ask. |
| **Red** | `*.scrivx`, `Files/binder.autosave`, `Files/search.indexes`, `Settings/**` | Never. Queue until the lock clears. |

Red is also every *structural* change, whatever file it lands in: creating,
deleting, renaming, reordering or re-parenting documents; changing label,
status or compile flags. All of that is binder state. It waits.

### Procedure for Green edits

Back up every target file into `backups/edits/{date}-{slug}/` before touching
it, preserving the `{UUID}/{file}` path so a restore is a straight copy back.
The scratchpad is not a backup; it is session-scoped and evaporates. Apply the
edits, then read the bytes back and confirm they took. Report the document
titles — not just UUIDs — so the author knows which pages moved.

Two consequences to state in the report rather than discover later. Project
search will not find the new text until Scrivener reindexes, because
`search.indexes` is only rewritten by the app. And if the author happens to
have one of the edited documents open in an editor, the stale in-memory copy
will overwrite the fix the moment they type in it — so name the documents and
say they should be reloaded. Backups exist precisely for the case where that
race is lost.

### Approval

Approval of a change is approval to apply it. When the author has said yes to a
fix, that yes covers writing it into the bundle — do not re-ask at the file
layer, and do not treat a running Scrivener as grounds for a second gate. There
is one gate, and it is about the content of the change, never the mechanics of
landing it.

Red-tier work is the exception, and even there the move is to queue and say so,
not to ask the author to close the app.
