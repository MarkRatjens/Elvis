---
name: sync-skills
description: Copy skills from a game repo's .claude/skills/ up to the anthro project root. Workaround for Claude Code's upward-only skill resolution.
disable-model-invocation: true
argument-hint: "[game-repo-name]"
---

# Sync Skills

Workaround: Claude Code resolves skills by walking
UP the directory tree, never down. This means game
repos (which are complete holons) lose their skills
when composed into the super-project. This skill
copies them up.

## Procedure

### 1. Locate game skills

The game repo is: $ARGUMENTS

If no argument given, list all directories under
the project root that contain `.claude/skills/`
and ask the author which to sync.

Read all `SKILL.md` files under:
`[game-repo]/.claude/skills/*/SKILL.md`

### 2. Adjust relative paths

Game skills reference sibling repos with `../`
(e.g. `../blog-publishing-syndicate/`). From the
anthro root, these siblings are direct children.

For each skill file, adjust paths:
- `../[repo]/` becomes `[repo]/`

Do NOT change paths that are relative to the caper
or artefacts (these resolve from $ARGUMENTS at
runtime).

### 3. Write to project root

For each skill, write to:
`.claude/skills/[skill-name]/SKILL.md`

If a skill already exists at the root, compare
the two. If the game version is newer or more
evolved, overwrite. If they differ in ways that
suggest intentional divergence, present both to
the author and ask.

### 4. Report

List:
- Skills synced (new or updated)
- Skills unchanged (already current)
- Skills skipped (with reason)
- Any path adjustments made
