# 11 · Failure patterns and lessons

What goes wrong when experts build Titan tasks and write Titan rubrics, what each mistake costs, and the probes that catch it before a reviewer does.

---

## Part 1 · How rubrics go wrong

Straight from the rubric guide. Each row is a check to run on any drafted set.

| Mistake | What it costs | Instead |
| Writing up what you notice first, usually formatting | Formula, structure and judgement problems go untested | Walk the cells with the checklist first |
| Describing the mistake, not the right answer | A different wrong answer passes | State what the correct workbook has |
| Requiring a method when several are standard | A correct workbook fails | Check the result and accept any method the prompt leaves open |
| Requiring analysis nobody asked for | A model that did what was asked loses points | Leave it out, or put the purpose in the prompt |
| Judging structure by counting tabs, rows or columns | The fuller answer is not always the better one | Judge whether the structure fits the task |
| Merging many checks into one long criterion | You cannot tell what went wrong | One criterion per independent mistake |
| Counting one mistake several times | One slip fails four criteria | Keep the one or two that capture it best |
| Copying the layout of the one output you saw | The rubric rewards that output's habits | Accept any layout the prompt leaves open |

---

## Part 2 · The probe battery

Run every one of these on every criterion before a KEEP. A yes to any question is a finding.

**Would a correct workbook fail this?** Picture the most defensible alternative route to the same answer — a different function, a different layout, a different but valid method — and check it passes. This is the single most common reason a rubric comes back.

**Would a wrong workbook pass this?** Picture a workbook that gets the right number by pasting it in, by a plug, or by wrapping a broken calculation in IFERROR. If it passes, the criterion checks the value and nothing else.

**Can the grader mark this without asking what you meant?** The grader has the prompt, the files, the workbook and the reply. Nothing else. Any word that needs the expert's intent to interpret — "appropriate", "clear", "professional", "reasonable" — is a finding.

**Does it still work if a row is inserted?** Any cell reference fails this.

**Has the number been recomputed from the inputs?** Not from the golden, not from the best model output, not from the expert's memory. From the input files.

**Was the tolerance agreed, or defaulted to?** Three significant figures; counts, dates, IDs and labels exact; everything else within one per cent; near-zero values get a band. A tolerance that just appeared is a finding.

**Does it name the source where inputs conflict?** If two files give different figures for the same thing, the criterion says which one governs.

**Is it one check?** If a failure could be caused by two unrelated things, it is two criteria.

**Does it repeat another criterion, or the universal list?** Both are findings. The universal list belongs on an escalation line, not in the rubric.

**Does it exist only because one output failed it?** A criterion written to catch a specific model's specific slip is a finding unless it also describes what good looks like.

**Would you have written it before you saw the outputs?** If the answer is no and it is not a real failure the outputs revealed, it is probably a preference.

---

## Part 3 · Lessons from built tasks

Each of these came out of a real build or a real screening response. They generalise.

**The allowed edit range must not double as a defect map.** On a fix task, listing the defect cells as the editable range tells the solver where to look. Give whole sheets, plus permission to insert one if the deliverable needs it, and let the scope criteria catch edits that went too far. Some defects — a missing row, for instance — cannot be expressed as cells anyway.

**Never put a figure in the prompt that the files do not carry.** A coupon stated to a precision the filing does not disclose, or a maturity given to the day where the source gives only the month, is unfair: the solver cannot tell whether their own reading is wrong. Drop to the precision the pack actually gives.

**Every rule the answer turns on lives in the prompt.** When a constraint gets added to the workbook late — a second exposure limit, a new house rule — the prompt has to carry it or the task becomes unsolvable. Check this every time either side changes.

**Leave tie-out cells empty, not wrong.** In a fix task, a correct figure sitting next to the defect it would expose hands over the answer. So does a note explaining the right treatment, a change log, a checks block, an open-items list, a cell comment or a defined name. The solver's copy carries none of them.

**Clear the file properties.** A generator leaves its own name in the file. So does the expert's employer. Both get cleared, and the timestamps should look like a file that has been worked on.

**Invent nothing the pack does not contain.** No price, yield, spread, rating or contractual term that is not in a source document. If a proposed complication needs data the pack does not have, the complication is held, not fabricated.

**Build the task around the conflicts, not around hiding them.** Where two sources genuinely disagree and no disclosure resolves it, say in the prompt what to do when something cannot be tied. That turns an unresolvable gap into a gradeable judgement, and it is exactly the judgement models get wrong.

**One underlying error, one criterion, however many symptoms.** A misclassification that breaks a balance sheet by a visible amount is one defect. The broken balance is a symptom. Writing both gives one slip two criteria.

**Chain the defects on a fix task.** The strongest fix tasks have a load-bearing defect: fix it and several downstream conclusions change; miss it and the workbook reaches a confident wrong answer. Independent defects of equal weight make a long task, not a hard one.

**Agree the tolerance on the spine before writing any criterion.** Cross-foot the figures the task rests on first, decide the band, and record the residue and where it comes from. A criterion written against a number nobody rebuilt is the thing a second reviewer finds first.

**Where several answers are defensible, define the feasible set.** A sale allocation, a trade date, a choice of basis — the criterion names the set and the rule that bounds it, not one value.

**Match every platform field to the file.** A field saying three tabs when the workbook has four is a finding before anyone opens the model.

**Figures traced to a source are not the same as a file that reads as human.** Labels, working notes and any supporting write-up are where generated text survives. Compress them to the terse notes a practitioner would actually leave, strip templated phrasing, and read everything back in the voice of the person who would have written it. Reference 13 has the full list.

---

## Part 4 · Pre-send checks

Before any answer from this copilot goes back to the expert:

- Every entry maps to something the expert actually gave you.
- Every verdict word matches the words beneath it.
- Every finding names the rule it rests on and quotes the locator.
- Every REWRITE carries its replacement sentence and its tag.
- Every number stated has been recomputed from the inputs, or is marked NOT VERIFIABLE.
- Nothing contradicts another entry.
- No criterion is proposed for anything on the universal list; those are escalation lines.
- Nothing claims a test that was not run.
- The closing verdict names the blocking items, not a count.
