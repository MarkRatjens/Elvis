# Compile pagination post-mortem — 2026-08-06

The 2nd Draft docx compile broke pages seemingly at random from Episode 1
onward. This records the root cause, the fix, and where the backups are, so
it never has to be re-diagnosed.

## Root cause

The project style definitions in `Files/styles.xml` — **Body, Notes, Quote** —
carried Scrivener's "Keep with Next ¶" paragraph attribute, stored as a
`<$ScrKeepWithNextSplittable>` marker inside each style's definition.

Consequences, in order:

1. Scrivener stamps the marker into every styled paragraph of `content.rtf`
   when it saves a document. A bulk restyle at 10:25 on 2026-08-06 spread it
   to 161 of 170 draft scenes — 7,567 paragraphs — plus 2,272 more in
   front matter and notes.
2. Compile folds the attribute into the exported docx's Body style as
   `keepNext`: every prose paragraph tells Word "do not separate me from the
   next paragraph."
3. Word cannot honour an unbroken chain, so it breaks pages early wherever
   the chain forces it — arbitrary-looking breaks with ragged white space.

The defect is invisible at paragraph level in the docx (paragraphs show no
pagination properties); it lives in `word/styles.xml`. Diagnosis of compile
pagination must always check the exported style definitions.

## Fix applied (all verified byte-level)

- `Files/styles.xml`: markers removed from the three style definitions.
- 235 `content.rtf` files: 9,839 per-paragraph markers stripped.
- One inert remnant remains in a `content.pre-rewrite-bak` file (not compiled).

## Backups (straight copy back to restore)

- `backups/edits/2026-08-06-keepnext-markers/{UUID}/content.rtf` — all 235
  content files, pre-strip.
- `backups/edits/2026-08-06-compile-headings/queued3-pre/styles.xml` —
  pre-fix style definitions.

## Recurrence vectors (the only two)

1. Redefining a style while its sample paragraph has "Keep with Next ¶" set
   (Format ▸ Paragraph). Check `Files/styles.xml` for
   `<$ScrKeepWithNextSplittable>` if pagination misbehaves again.
2. Pasting styled text from Word that carries keep-with-next — arrives as a
   per-paragraph attribute.

## Same-day related fixes (separate causes, same compile)

- 73 stale per-item section-type overrides removed from the binder (chapters
  compiling as season pages; scenes as episodes with page breaks).
- 30 scenes had a trailing empty paragraph causing occasional blank pages
  (`backups/edits/2026-08-06-trailing-blanks/`).
- Compile format: season/episode heading layouts, separators, Heading 1/2
  style export (`backups/edits/2026-08-06-compile-headings/`).
