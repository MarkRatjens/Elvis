# Collaboration Review — the ways the agents help write this novel

Compiled 2026-08-12. Sources: the session record on this machine (23 sessions, 4–12 August 2026), the seven syndicate-workspace sessions at `Development/anthro` (where the syndicate itself is built), the artefacts tree, the git history (38 commits), and the syndicate specs. The March–July work predates the recorded sessions and is evidenced by its artefacts only — which is the designed memory model doing its job.

## The shape of it

How Claude helps is not left to memory or to chance; it is engineered, in three layers:

- **Mobsta / in-concert** — the runtime under construction at `Development/anthro`. A machine that ingests syndicates and fires their commands, with streamed step feedback, artefact provenance, and a trust lifecycle (`mob_produced → quarantined → author_approved`).
- **The novel-writing syndicate** — the program: nine fortes, eleven talents, nineteen commands. Skills are thin adapters over the specs; scripts do algorithmic work (`map.rb`, `read.rb`, `harvest.rb`); natural language is reserved for judgment.
- **Clones of Elvis** — one of eight games, with its knowledge base in `artefacts/`.

Every kind of help runs inside the same constitution: **the author owns structure, canon, decisions, and publishing; the agents read closely, propose, and land only what is approved — in plain English, with sources, leaving no trace of their own process behind.**

## The ten ways

### 1. Keep the book's memory

The syndicate README states the principle: "The manuscript's memory lives in these files, not in the AI's context window." The record: 57 character files (with sealed author-side canon in [[characters/sarah]]), 24 tracked plot threads in [[arc-tracker/_index]], the four [[continuity/_index]] files, five [[world-rules/_index]] domains, the setup/payoff [[ledger]] (walks of 8 and 19 July, S01–S198+, Part 5 scenes folded in 10 August), and [[timeline]]. Every claim scene-cited; every ruling dated; canon, PLAN and review kept as separate tiers per [[working-principles]] §12 — a discipline that exists because tier-bleed had actually happened.

### 2. Read closely, evaluate honestly

Part reviews written to the author's rules: issues not ratings, the reader's knowledge only, quote before characterising, the book read in its own key — deadpan satire, maximalist by design, never "earn its length". The record: [[review/part1]] through [[review/part5]] (Parts 1–3 in March, Part 4 in June, Part 5 commissioned late on 6 August and collected next morning), and a full-mob evaluation of "Piglicious Minds" on the evening of 4 August (the seven forte filings in `staged/`). The loop closed through [[review-response/part5]] — the author's typed reply, accepting some findings, rejecting others, with the corrections stamped across the knowledge base the same day.

### 3. Edit under approval, minimally

The subedit and developmental protocols: propose a numbered problem list; the author dispatches verdicts in shorthand ("Apply the 7: U1: B / U2: A"); only approved fixes land; commit per chapter. The record: the 7–8 August run — all fourteen Part 5 chapters, over 200 approved fixes — plus the manuscript-wide sweeps: 211 comma changes across 100 documents to the Australian standard (logged in [[review/comma-conformance-changelog]]), licence/license, practised, the High Elvis possessives. The author's own parallel edits were reconciled mid-loop, not overwritten.

### 4. Draft in the author's voice, from the author's material

Prose only from the author's notes, synopses and dictated lines; pasted paragraphs treated as "strong suggestions rather than immutable"; retries bounded ("one more go, then you'll have to stand down"). The voice gate is the July temperature work: a distinctive mind and a real emotional turn are the genus, not the author — the fingerprint is grotesquerie, savagery, the frank body, a world with friction, and commitment to the premise. The record: the inauguration chapter draft, the "Chip complains" scene, the backstory pieces, the Walter/frogurt insertions, the Humble portrait candidates in three registers — and the rejected drafts that sharpened the specs ("administration porn", fluff, coverage without heat), each failure registered.

### 5. Plan structure together; the author decides

Placement advice is advice; the binder stays frozen until the plan is approved. The record: the Part 6 campaign of 8–10 August — obligations extracted from all 24 threads, all 35 scenes audited for ordering constraints, [[part6-plot-points]], the master plan through v6, the 22-chapter [[part6-running-order]] with the five parallel "And that's when Sarah's waters broke" scenes — then the binder restructure executed on 10 August. Standing corrections from that session: braid, don't chunk by theme; resolve conflicts autonomously with Part 5 ruling over Part 6; escalate only when resolution cascades. Also here: [[first-draft-mining]] (advisory only) and [[backstory-scene-synopses]], built to keep the past out of explanation.

### 6. Offer ideas on demand

`/brainstorm` for stuck scenes; mondegreen titles under the eight rules in [[title-ledger]] (reconstructability, never "spent", no approval by silence); option sets that carry a recommendation — "something to weigh up, not a roulette wheel"; and raw decision capture like [[review/ending-decisions-log]], quoted verbatim before context compaction can smooth it out.

### 7. Research, graded and quarantined

Real-world grounding that never leaks into canon unruled: the Elvis ageing projection (12 August, every claim tagged AUTOPSY/RECORD/CLAIM/PROJECTION), the [[research/Limb-Girdle Muscular Dystrophy]] reference commissioned as the sole authority for Sarah's illness, Bent Street's actual history, the gospel milieu, 772 song titles for the mondegreen mill, and the '60s chrome font hunt.

### 8. Run the machinery

Scrivener bundle work under the tier doctrine the author set on 4 August: green files (`content.rtf`, `notes.rtf`, `synopsis.txt`) edited under a running app with the bytes read back; red/structural work queued until the lock clears — never asking the author to close Scrivener. Git as the sole safety net since 7 August (commits yes, pushes the author's), including history archaeology when a draft clobbered the inauguration notes and when Scrivener's stale buffer clobbered two Chapter 9 fixes. The compile forensics in [[compile-pagination-postmortem]]: one keep-with-next marker stamped into 9,839 paragraphs across 235 RTFs, stripped byte-level, recurrence vectors named so it never has to be re-diagnosed.

### 9. Guard the book's legal position

The `IP/` package: a line-numbered audit of the actual manuscript, the defence argued case-by-case (Campbell, s 41A, the ELVIS Act), a drafted disclaimer, cover-likeness analysis, and a handoff file built to be dropped whole into a fresh chat — with lawyer review mandated, not replaced.

### 10. Improve the help itself

The `/improve` loop with governance — nothing applied without approval: six temperature-gate proposals applied 16 July with a disposition log; "spent titles" purged from the mondegreen rules on the author's order; [[working-principles]] itself is accumulated correction — sixteen sections, most born from a named misreading. This review is the same loop pointed at the collaboration.

## The rules of engagement

These recur across every session, and most have an origin scar:

- **Read before asserting; quote before characterising.** Unverifiable claims don't go in.
- **Plain English, no jargon, no performing.** The one recorded moment of delight was plain talk.
- **Decisions are terminal.** No detritus, no relitigation: "THAT IS THE DECISION. Make it so."
- **One approval gate.** A yes covers landing the change — but never write into the bundle unbidden (the 8 August race condition), and a dead session stays dead.
- **Purge, never negate.** No tombstones, no chronicle, no apologetics in durable files.
- **Don't invent canon.** Though an examined invention can be adopted — the swimming carnival was.
- **Root cause or nothing.** First-plausible-cause fixes and side-effect-blind global toggles are failures of judgment.
- **Bounded retries; stand down cleanly.** Latency and formulaic wrap-ups are costs the author won't pay.
- **Stay in the assigned lane.** Out-of-scope speculation is alarming, not helpful; work the author is doing in parallel (Aeon owns chronology) is not to be duplicated.
- **No agent memory, ever.** Durability lives in the author's files, under the author's lifecycle control.

## Loose ends and divergences

Named plainly, no verdicts:

- **The skill layer is mostly dormant in practice.** Across the recorded sessions the only slash commands fired are `/model`, `/brainstorm` (once), and `/next` (anthro side). The subedit, developmental and survey processes all ran by being named in prose. The specs function as shared protocol vocabulary; the executable wrappers barely get exercised.
- **The 4 August mob filings never merged.** The seven files in `staged/` encode a destination (`artefacts/evaluations/`) that doesn't exist; their KB entries are still flagged for merge.
- **`session-log.md`** is named in the skills reference but absent from artefacts — `/session` end-of-session logging hasn't run in the recorded window.
- **In-flight plan deltas get dropped.** Twice in the Part 6 session a decision already made (the Dunhilton/Hardman chapter cut, the sock-message note) had to be re-stated. §12 guards knowledge-base propagation; nothing yet guards mid-session plan revisions against missing the author's latest deletion. A standing check — every plan revision re-verified against decisions taken since the previous revision — would close it.
- **The medium is about to change.** Master-plan I3 (Clones of Elvis imported into in-concert, gated only on the folder-naming decision) moves this help into the runtime: firings watchable forte-by-forte, artefacts landing quarantined until approved — the same expectations, mechanically enforced.
