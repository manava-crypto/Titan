---
description: Run the Project Titan final QA pass over the task and the rubric before submission
argument-hint: "[path to the full pack, or leave blank to use attached/most recent files]"
---

Run **final QA** on the Titan pack at: $ARGUMENTS

Delegate to the `project-titan-excel-tasks` agent via the Agent tool. Brief it to:

- Read `skills/project-titan-excel-tasks/SKILL.md` and, in `references/`, `08_rubric_stress_tests.md`, `12_checklists.md`, `13_human_voice_and_ai_tells.md` and template G of `09_output_templates.md` before any verdict.
- Have open: the prompt, every input file, the expert's reference answer, the rubric, the model outputs, and for a fix task the defect map and both workbooks.
- Rebuild every figure in the rubric from the input files, using the relationship each Method criterion states, never from a workbook's own cells. Name every figure that does not reproduce, and say what tolerance was agreed and where any residue comes from.
- Confirm every criterion changed since the last pass still reads on its own, still passes the expert's best workbook, and is still tagged right.
- Run the second-reviewer protocol: make a copy of the best model workbook and introduce one break at a time — a root input changed with the downstream left alone, a key output pasted as a value, a check row replaced with the word Pass, IFERROR hiding a genuine error, a required period deleted, a cell edited outside the allowed range, a planted error fixed at the symptom rather than the source, a helper tab the recipient would delete, a row inserted above a value a criterion names, a reply claiming something the workbook does not show. Say which criterion catches each break, and name every break none catches.
- Rebuild the same answer in a second defensible layout or by a second valid method and confirm every criterion still passes it. A criterion only the expert's own route satisfies is over-specified.
- Run the scenario-independence test where the workbook carries scenarios: perturb a downside input and confirm the base-case outputs do not move.
- On a fix task, run the leakage sweep over the solver's copy, confirm every defect-map cell differs between the two workbooks, and confirm both recalculate with zero formula errors and zero circular references.
- Check every platform field against the file: tab count, ranges, file names, deliverable list.
- Run the voice and build check in 13 across every surface — prompt, scenario, each input file, each workbook, the criteria — including file properties and timestamps.
- Work the task checklist, the rubric checklist and the final QA checklist in 12 and report any unticked item.
- Answer inline under T1 to T8 in SKILL.md, in template G's order, closing with the hand-over list and a single READY to submit or NOT READY line.

Re-verify every blocking finding before relaying. Where a break went uncaught, say which criterion should cover it and write that criterion out.
