# 08 · Stress-testing a rubric

A rubric that reads well still has to survive four tests, a table of shortcuts, three last questions and a second reviewer. Run all of them before a rubric is submitted.

## The four things a good rubric does

**1. Passes your best work.** A workbook the expert would send as it is passes every criterion.

**2. Fails what you would send back.** A workbook the expert would send back fails at least one criterion. If one passed everything and would still be sent back, a criterion is missing.

**3. Cannot be gamed.** The laziest workbook that could pass — pasted values, IFERROR on everything — does not score well.

**4. Accepts good alternatives.** A different approach a professional would defend passes.

In size, that means at least ten criteria, together covering every ask in the prompt, every real mistake the expert saw, and the standard practice any professional in the field would follow.

## The shortcuts table

Models sometimes take a route that gives the right number for the wrong reason. A rubric that only checks values lets these through.

| Shortcut | What catches it |
| Values worked out elsewhere and pasted in | Covered for you: key outputs must be live formulas |
| A plug that forces a balance to tie | Your criterion: the balance holds with no hardcoded adjustment |
| IFERROR wrapped round broken logic | Your criterion for each planted error: fixed at its source |
| The broken block deleted in a fix task | Your criterion: every output the block fed still exists and is correct |
| Inputs overwritten so the outputs match | Your criterion: input cells unchanged unless the prompt asks for new ones |
| The workbook rebuilt from scratch in an edit task | Your standing criteria on the allowed range |
| The answer in the chat only, or the file only | Your criteria say where the evidence is, and the two must match |

## The three last tests

- If a workbook passed every criterion, would the expert still send it back? If yes, a criterion is missing.
- Would the laziest workbook that could pass, with pasted values or IFERROR everywhere, still score well? If yes, a criterion is missing.
- In an open task, do at least a third of the Quality criteria test a decision the model had to make?

## The second-reviewer protocol

This is what happens to the rubric after submission, so running it first is how work stops coming back. A second reviewer rebuilds the expert's numbers and tries the rubric on broken copies of the best output.

**Rebuild the numbers.** Take each criterion carrying a figure. Recompute that figure from the input files, using the relationship the Method criterion states, not from any workbook's cells. Any figure that does not reproduce is a finding against the criterion, not against the model.

**Break the best output, one break at a time.** Make a copy of the best model workbook and introduce one defect. Then read the rubric and ask which criterion fails. A break that no criterion catches is a gap.

Breaks worth making, chosen to match the failure modes in reference 05:

- Change one root input and leave the downstream cells as they are. (Does anything catch the broken link?)
- Paste a key output as a value over its formula.
- Replace a check row's formula with the word "Pass".
- Wrap a working formula in IFERROR so a genuine error disappears.
- Delete one required period, entity or scenario.
- Edit a cell outside the allowed range, on an edit or fix task.
- Fix a planted error by overwriting the symptom rather than the source.
- Add a helper tab the recipient would have to delete.
- Insert a row above a value a criterion names, to see whether any criterion was written against a cell reference.
- Change the reply so it claims something the workbook does not show.
- Rebuild the same answer in a different but defensible layout. (This one should *pass*; if it fails, a criterion is over-specified.)

**Test scenario independence.** Where the workbook carries scenarios, perturb a downside input and confirm the base-case outputs do not move. A model that has wired the cases together gives the right base-case number today and a wrong one the moment anybody switches case.

**Sweep for leakage** (fix tasks). Read the solver's copy as the solver: does any cell, note, comment, defined name, change log, checks block or open-items list point at a defect? A correct figure sitting beside the defect it would expose is leakage even when nothing says so.

**Try a second valid approach.** Where the prompt leaves a method open, work the answer a second legitimate way and check that every criterion still passes. A criterion that only the expert's own route satisfies is over-specified.

## The probe questions for the set

- Do any two criteria contradict each other?
- Does any single realistic mistake fail more than two criteria?
- Does any criterion exist only because one particular output failed it?
- Does any criterion rest on a number nobody has recomputed from the inputs?
- Does any criterion use a tolerance nobody agreed?
- Does any criterion name a cell reference?
- Does any criterion depend on reading another criterion?
- Does any criterion describe the mistake rather than the right result?
- Does any criterion require a method where several are standard?
- Does any criterion ask for analysis the prompt never asked for?
- Does any criterion judge structure by counting tabs, rows or columns?
- Does any criterion repeat something on the universal list?

A yes to any of these is a finding, with the criterion named.
