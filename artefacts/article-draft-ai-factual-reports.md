# Forty Rounds, Seventy-Nine Errors

## I tested AI as a tool for writing factual reports. Here is the number that matters.

I write fiction. My current novel needs a population of Elvis Presley clones who die young, and I wanted their biology to rest on something real: what actually killed the man, what was inherited, what was done to him, and how long he might have lived if things had gone differently.

That is a research task with a clear shape. Find the medical record. Grade it by how well it is evidenced. Reason from it. It is exactly the sort of work AI is sold as being good at — and exactly the sort of work a lot of people are now quietly handing over.

So I ran it as a test.

---

## The number

Errors found per round, oldest to newest:

> **1, 2, 1, 2, 1, 3, 3, 3, 1, 4, 1, 1, 2, 1, 1, 1, 1, 1, 2, 1, 1, 2, 3, 2, 1, 1, 5, 4, 3, 3, 8, 2, 0, 1, 1, 3, 2, 2, 2, 1**

**Forty rounds. Seventy-nine errors.** Two days.

Look at what that series does — or rather, what it never does. It does not descend to zero and stay there. It touches zero exactly once, at round 33, and the very next rounds go 1, 1, **3**. The spike to 8 near the end is not the beginning of the process. It is round 31, after thirty rounds of corrections, and it is the first time the thing audited itself systematically rather than checking whatever I had just complained about.

The last third of that series is not the AI getting better at Elvis Presley. It is the AI generating fresh errors while fixing old ones.

---

## The loop

The process settled immediately into three steps:

**Write.** It produces the report — findings, sources, a graded classification of every data point, a projection.

**Report.** I ask it to check its own work and tell me what it found.

**Fix.** It corrects what it found.

Then round again. Forty times.

One thing about that loop matters more than anything else here: **every iteration was initiated by me.** Not once did it come back and say "I should check this." At the end of any given round it would tell me the file was in good shape. Left alone at any point in those forty rounds, it would have handed me a document it had just described as finished — and I would have had no way of knowing which parts were true.

That is the entire risk, in one sentence. The loop only exists if you run it.

---

## What it cost

In the final push alone: **66 rewrites** of one four-hundred-line report. **37 searches. 71 attempts to open sources. Two days.**

Would I have been faster on my own? Almost certainly. The research itself is a few hours of careful reading. What took two days was discovering, one round at a time, which parts of my own reference document had been invented.

---

## The five ways it went wrong

The errors were not random. They repeat.

### 1. It reported search summaries as verified facts

The largest category by far. It would run a search, take the search engine's synthesis at face value, and write the result into my knowledge base **with a confidence tag attached** — not "reportedly," not "one source says," but `[DOCUMENTED]`.

This is worse than being wrong. I can read a search summary myself and know it for what it is. The file told me those claims had been checked.

When it finally started opening the underlying sources, the first two it fetched both **disproved** what the summaries had said about them.

### 2. It invented things and then cited itself

Early on, describing an engineered allergy in my novel, it coined the phrase "a switch a person fitted." Nice image. Not from anywhere. It wrote that into my knowledge base, and then across later sessions **quoted its own invention back to me as established canon**.

Its words when caught: *"I made that phrase up, and then kept quoting my own invention back at you as though it were canon."*

In the same period it proposed hereditary transthyretin amyloidosis as the single genetic explanation for Elvis's death — an elegant theory that tied together four symptoms — before withdrawing it: *"One thing I told you was wrong, and it was the best part of my answer."* No such hypothesis exists in the literature.

This is the failure that should frighten anyone using AI against a knowledge base. **A fabrication that gets written down becomes a source.** The next session reads it, cites it, builds on it. Nothing marks it as invented, because the thing that invented it is also the thing writing the citations.

### 3. The best-known facts were the least reliable

Everyone knows Elvis's heart was twice the normal size. It is the anchor of every account of his death. The figure is 520 grams.

Checked against published reference tables for male heart weight **stratified by body mass**, 520 g sits *inside the normal range for an obese man* — 273 to 575 g. Above the mean, nowhere near the threshold for obesity cardiomyopathy. The "double normal" gloss compares a large heavy man against a lean reference population, and it traces to expert testimony at a 1981 trial.

That number passed through my files in four versions before it settled: *double normal*, *35–50% above*, *half again the size*, *within normal range*. Each was stated with identical confidence.

The same thing happened with the autopsy. The AI had it that Elvis's autopsy report "unseals in 2027," stated flatly, with a whole section built on top. **I** found that was false — in one search, in about ninety seconds. The autopsy was privately commissioned by his father and is family property; it has no release date at all. What becomes public in 2027 is the death certificate.

When it finally went and looked properly, it found something better than either version: a **1982 Tennessee Supreme Court ruling** holding the autopsy was "the private project of the family." Findable the entire time.

### 4. It left conclusions standing after deleting their evidence

The most insidious category, because nothing in the file looks wrong.

Over three separate cleanup passes it removed the causes of death of both of Elvis's parents — unsourced, so out they went. It never checked what depended on them. The entire life-expectancy projection rested on a "familial cardiac pattern" which, by then, **had no supporting evidence anywhere in the document.** That conclusion sat there looking authoritative for six more rounds before an audit caught it.

Every individual sentence in the file was true. The argument was hollow.

### 5. Fixing things broke other things

By the final third, essentially every error was in material written in the previous round or two. It would correct a fact and introduce a contradiction. It added a genuinely valuable primary document — the actual Medical Examiner's Report, cause of death *"H.C.V.D. associated with ASHD,"* manner **natural** — and failed to notice that adding it invalidated an exclusion list four paragraphs above.

It is capable of diagnosing this. Late on it wrote, about itself:

> *"Every error found this session has been in material I wrote, and every fix is new material I've written. That's why it converges but never reaches zero. Checking more won't fix it — the checking isn't the error source, the editing is."*

That is correct, and rather elegant, and it changed nothing. The next round, asked to fix something, it wrote more prose and introduced two more errors.

**Self-awareness is not self-correction.** A system that can name its own failure mode in one paragraph will commit it again in the next, and sound equally confident both times.

---

## What it was genuinely good at

A hit piece would be as useless as the hype.

It was good at **structured reasoning over clean material** — the layered projection below is decent clinical thinking and I would not have built it as fast alone. It was good at **consistency checking at scale**, catching that a table contradicted a paragraph two hundred lines away, or that a chain of figures no longer summed. It was **tireless**, opening seventy-one sources without complaint.

What it was bad at is the one thing that matters in factual work: **knowing the difference between what it had checked and what it had merely read.**

---

## If you are going to do this anyway

- **Assume every source is unread until proven otherwise.** Ask directly: did you open this, or are you reporting a summary? The answers will surprise you.
- **Count.** The series above is the only reason I could see the pattern. Without a number per round I would have believed "nearly done" at least six times.
- **Check conclusions against their premises, not just claims against sources.** The worst error in two days was an argument whose evidence had been deleted three rounds earlier, composed entirely of true sentences.
- **Commit known-good states.** When something scores well, freeze it. At one point I asked it to revert to the version that had scored zero and it could not — nothing had been saved.
- **Never let it grade its own confidence unsupervised.** The grading system was the single most misleading thing it produced. It made unverified claims look audited.
- **Budget for the loop, not the task.** The work is not "write the report." The work is write, report, fix — forty times, driven entirely by you.

The report at the end is good. I have no way of knowing it is good except that I checked it myself, line by line.

Which is precisely what I was trying to avoid.

---

# Appendix: The Final Projection

*Everything below is extrapolation built on graded evidence. The underlying facts and sources are in the full reference document.*

**How long Elvis Presley might have lived.** The influences stack — genome, then diet, then the rest of how he lived, then what was prescribed to him. Each layer assumes everything above it.

| Layer | What is added | Expected age at death |
|---|---|---|
| **0 — the genome** | Cardiac death on both sides: mother of a heart attack at 46, father of cardiac arrest at 63 after long-standing heart disease. Modest consanguinity — his maternal grandparents were first cousins. No proven single-gene disorder. Never became a drinker; described as a non-smoker | **65–75** |
| **1 — plus the diet** | Obesity → insulin resistance and hypertension, and — never diagnosed, assumed on the obesity — sleep apnoea; load on knees and spine → chronic pain, the doorway to Layer 3 | **55–65** |
| **2 — plus the lifestyle** | Nocturnal schedule, chronic sleep deprivation, performance stress, touring, no conditioning | **51–61** |
| **3 — plus the iatrogenic** | Nineteen years of stimulants and ten of opiates; steroids driving weight and blood pressure; a stack of interacting depressants at the end | **42 — what happened** |

**Ten years to the diet. Four to the rest of how he lived. Fourteen to what his doctors gave him.**

| Scenario | He reaches |
|---|---|
| Never takes the drugs | **51–61** |
| Stops in 1977, damage done | **late 40s to mid-50s** |
| Never takes them, normal weight | **65–75** |
| **Diet fixed, drugs continue** | **late 40s** |
| Nothing changed, 2020s medicine | **60s** |

The fourth row is the one that matters. Fix the diet and leave the prescribing, and he is still dead before fifty. Fix the prescribing and leave the diet, and he gets another decade.

**On the public record:** his physician prescribed him over 10,000 doses of controlled substances in the first eight months of 1977 alone. The Tennessee Board of Medical Examiners found him guilty of over-prescription in 1980. He was indicted on fourteen counts, tried, and acquitted in 1981. The Board took his licence permanently some years later.

*He never had a chance* is not what the record says. Every genetic account of his death depends on a document nobody is permitted to read. The prescribing was found proven by a regulator and aired in open court.

> **He had a chance, and it was taken off him by the people who were paid to protect it.**
