# 03 · Prompt standards

## The brief

Write as if to a strong colleague who knows the field but has never seen this file. Tell them what is needed and leave the method to them, unless something has to be done a particular way. That is a choice, so it is stated.

## Say

- What comes back, including the file format.
- Which files are attached and what each one is.
- Who it is for, and any deadline.
- What must not change, and any house rules.
- Any choice the answer depends on: which scenario, which period, units, rounding.
- The Excel version and any tools or features the job needs, where compatibility matters.

## Leave out

- The method, functions or formulas to use.
- Warnings about the traps in the files.
- Conventions any professional already follows.
- A tab-by-tab layout of the answer.

## The test for a choice

If two good professionals could reasonably choose differently and the answer changes, state the choice. If everyone would do it the same way, leave it out.

House style counts as a choice. Firms differ on input colours and summary layouts, so if the expert's house style matters to the grading, the prompt says so. If it does not matter, the rubric must not test it either.

## The three rules

- **4.1 It has to read like a real message.** A real set of instructions from someone in the field, in their voice. The guide's wording is to write it without AI, and reviewers check for the tells: hedged phrasing, uniform list structure, no voice. Draft it however suits, then read it back as the person who would have sent it.
- **4.2 One prompt.** Everything else the model needs goes in the files.
- **4.3 Any length is fine; vague is not.** Titan wants a mix of short and long prompts. Whatever the length, nothing the answer depends on is left out.

## Worked contrasts

### Too much hand-holding

> Build a 3-statement model. **Put assumptions on an Inputs tab in blue font. Use SUMIFS to pull the trial balance.** Make sure the balance sheet balances and **add a check row. Watch out for the FX on the cash flow statement.**

An Inputs tab in blue is what a professional would do anyway. SUMIFS and the check row prescribe the method. "Watch out for the FX" points straight at the trap.

### How a colleague would ask

> Finish the cash flow for the Q3 pack using the attached TB and FX rates. It needs to tie to cash on the balance sheet. Board pack goes out Friday.

It names the deliverable, the inputs, the one hard constraint and the audience. The FX trap is still in the task; the prompt just does not mention it.

### Too vague

> Can you do the July rota for Ward 7? **Same as June.** Leave is attached.

It leaves out the rules the answer depends on: minimum cover, limits on hours and nights. It does not say what to do if a shift cannot be filled. Two experts would build different rotas, so a model's mistake proves nothing.

### Longer, and also valid

> Please add July's rota to the workbook in the same layout as June. The staff tab has contracted hours, and the leave export has approved July leave, which replaces pencilled-in leave. Every shift needs two registered nurses, including one band 6 or above. Nobody should work more than three nights in a row or exceed their monthly contracted hours. Anyone on the last night of June cannot start July on an early shift. Leave any shift that cannot be covered within these rules unfilled and show the gap in the summary. Return an .xlsx.

Every sentence is context, a constraint, or a choice the answer depends on: minimum cover, rest rules, what to do when a shift cannot be covered. It still does not say how to build the rota — by hand, with formulas or with Solver — or where the clashes are.

## Checks to run on a prompt

1. Walk it line by line. For each sentence, is it context, a constraint, or a choice the answer depends on? If it is none of those three, it is probably prescribing a method or pointing at a trap.
2. List everything the answer depends on. Scenario, period, units, rounding, what must not change, output format, Excel version, features. Each one is either in the prompt or does not matter. If it matters and is absent, that is a finding.
3. Cold read it. Reading only the prompt and the files, name the answer. If two readings survive, the prompt is underspecified, not hard.
4. Look for the trap being named. Any sentence that warns about a conflict, a gap or an oddity in the files removes the difficulty.
5. Look for the method being named. Functions, formula patterns, tab layouts, colour conventions that are not genuinely house rules.
6. Check the deliverable. Format, and whether anything is asked for that cannot be returned in it.
7. Check it reads as human. Hedged, listy, uniformly structured prose with no voice is what AI-written prompts look like, and reviewers check for it.

## What a prompt finding looks like

Name the rule, quote the phrase, say what it does to the task, then give the replacement wording. "Watch out for the FX on the cash flow statement" points at the trap, so the difficulty is gone; the task's hardness depended on the model finding it. Cut the sentence, and if the prompt then loses a constraint the answer needs, write the constraint back in without naming where the conflict is.
