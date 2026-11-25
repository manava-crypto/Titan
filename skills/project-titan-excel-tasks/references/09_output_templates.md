# 09 · Output templates

One template per stage. Follow T1–T9 in SKILL.md for length and form. Everything is inline prose; no tables, no code blocks, no file cards.

---

## Template A · Task screening

```
[Optional lead: one paragraph. The verdict, the task type, and the one or two
findings that drive it.]

Type — [Build from scratch / Edit or extend / Fix a messy workbook].

Real — [READY / NOT READY]. [One sentence if clean. If not: what it rests on
that is not real work, or what has been tidied out of it, and the change.]

Fair — [READY / NOT READY]. [If not ready, name the two defensible answers and
the choice the prompt has to state.]

Hard — [READY / NOT READY]. [Where the difficulty sits, by failure mode. If the
only failures available are minor, say so.]

Reference answer — [present / absent / PENDING INPUT]. [Whether the headline
results reproduce from the inputs.]

Cold read — [what a second expert could and could not settle from the prompt and
files alone].

Scenario — [who needs it, what exists, what changed, what they expect back:
present or missing].

Headline checks — [3 to 5 expected. Each needs a visible result, its source,
period or scenario, and an agreed tolerance. Name any that lack one.]

Allowed edit range — [edit and fix tasks only].

Delivery constraints — [format, Excel version, features; anything the task needs
that the format cannot carry].

Defect map — [fix tasks only].

Voice and build — [reference 13: anything on any surface that reads as
generated].

Optional: [at most three].

Verdict: READY to propose / NOT READY — [the blocking items, named].
```

---

## Template B · Prompt check

```
[Optional lead: one paragraph.]

[Then one entry per finding, each headed by the quoted phrase from the prompt.]

"[quoted phrase]" — [the rule it breaks, in one plain sentence. What a model or
grader does with it. Then the replacement wording, written out.]

Missing — [each thing the answer depends on that the prompt does not state:
scenario, period, units, rounding, what must not change, format, Excel version,
features. One line each, with the wording to add.]

Voice — [reference 13: tells, and the rewrite].

Verdict: READY / NOT READY — [the blocking items].
```

---

## Template C · File check

```
[Optional lead: one paragraph.]

[One entry per file, headed by the file name.]

[filename] — [READY / NOT READY]. [What was swept: sheets including hidden ones,
comments, properties, external links, data connections, embedded objects. Then
each finding: what was found, where, what it does to the task, and the exact
change.]

Provenance — [each file's stated source, and anything unstated].

Features and format — [what the job needs against what the file can carry].

Artificial tricks — [white font, meaningless tab names, bans on normal
functions: present or none].

Build quality — [reference 13 part 2: anything in structure, formatting, file
state, data or properties that reads as generated, with the change].

Verdict: READY / NOT READY — [the blocking items].
```

---

## Template D · Failure hunt

```
[Optional lead: one paragraph. How many independent failures, in which
categories, and whether the task looks hard enough.]

[Best workbook first, then each other output. One entry per independent failure.]

[Output name] · [short label for the failure]
[What is wrong. What should happen instead. Where it can be seen, by sheet and
label. Why it matters. Mode [1-6], category [Correctness / Craft / Scope /
Judgement and communication]. Candidate criterion: yes / no.]

Repeated symptoms — [symptoms rolled up under the single cause that produced
them, so nothing is counted twice].

Not in the four categories — [anything that fits none; it still gets a criterion
and goes to the reviewer].

Tests run — [input changed and traced, deliberate mismatch, rows or period
added, refresh, Excel version].

Verdict: [n] independent failures, [n] of them candidate criteria.
```

---

## Template E · Rubric draft

```
[Optional lead: one paragraph. How many criteria, how they split across the four
categories, and anything the draft could not settle.]

[Then the criteria, numbered, in the order a reviewer would read them:
correctness first, then craft, scope, judgement and communication.]

1. [The criterion, one sentence.] — [Outcome / Quality] [· Domain Specific]
2. ...

[After the list:]

Key outputs — [the figures the workbook exists to produce].

Allowed edit range — [edit and fix tasks].

Numbers used — [each figure in the criteria, with the inputs it was recomputed
from. Anything not recomputed is named here as NOT VERIFIABLE.]

Covered — [each Core area of the task type, and the criterion that covers it].

Not written — [anything deliberately left out, and why: universal list, personal
preference, analysis nobody asked for].

Before you submit: read each one back in your own words; the set should sound
like one person wrote it.
```

---

## Template F · Rubric check

```
[Optional lead: one paragraph. The verdict on the set, the count, and the two or
three findings that drive it.]

[One entry per criterion, in the expert's numbering, headed by their own text.]

1. "[their criterion]" — KEEP. [One sentence, thirty words at most, holding only
the evidence that clears it.]

2. "[their criterion]" — REWRITE. [The rule it breaks, quoted phrase, what a
grader or model does with it. Then the replacement, written out, with its tag.]

3. "[their criterion]" — DROP. [Why: on the universal list, duplicate of n,
analysis nobody asked for, or written to fail one output.]

[Then the set.]

Count — [n criteria against the bar for this task's complexity].

Tags — [any mis-tagged, with the question from the four that settles it].

Coverage — [Core areas with no criterion, named].

MISSING — [one entry per gap: the item from the expert's step-one list, the real
model mistake, or the Core area, each with the criterion written out.]

Double-counted — [any single realistic mistake failing more than two criteria].

The four tests — [passes best work / fails what you would send back / cannot be
gamed / accepts good alternatives: each with the criterion that carries it or
the gap].

Voice — [reference 13: hedging, uniform shape, generic nouns].

Verdict: READY / NOT READY — [the blocking items].
```

---

## Template G · Final QA

```
[Optional lead: one paragraph. The verdict over task and rubric together.]

Numbers — [every figure in the rubric, recomputed from the inputs. Name any that
did not reproduce.]

Changed criteria — [each one the expert changed since the last pass: still reads
on its own, still passes their best workbook, still tagged right.]

Broken copies — [each break made, and which criterion caught it. Name every
break no criterion catches.]

Second valid approach — [the alternative route worked, and whether every
criterion still passes it].

Task side — [prompt, files, scenario, headline checks, allowed range, delivery
constraints: anything still open].

Voice and build — [reference 13, across every surface].

Hand-over — [criteria count, tags complete, Domain Specific where it applies,
key outputs listed, allowed edit range listed].

Verdict: READY to submit / NOT READY — [the blocking items].
```

---

## Template H · Escalation line

One line each, the only lines with a vertical bar. Used for anything outside the
expert's control, and for every broken item on the universal "already covered"
list.

```
Escalation | [surface] | [what is wrong] | [who it is for: platform / reviewer] | [what it blocks]
```

Example:

```
Escalation | shared checks | the live-formula check passed a workbook with three pasted key outputs | platform | the rubric cannot cover this itself
```
