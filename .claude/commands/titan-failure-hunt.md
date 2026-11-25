---
description: Compare every model workbook against the reference answer and build the Titan failure list
argument-hint: "[path to the outputs and inputs, or leave blank to use attached/most recent files]"
---

Hunt the **model failures** in: $ARGUMENTS

Delegate to the `project-titan-excel-tasks` agent via the Agent tool. Brief it to:

- Read `skills/project-titan-excel-tasks/SKILL.md` and, in `references/`, `05_failure_taxonomy.md`, `10_worked_examples.md` and template D of `09_output_templates.md` before reporting anything.
- Have open: the prompt and input files, the expert's reference answer and headline checks if they exist, and each model's workbook and reply.
- Walk the best workbook cell by cell first. Its obvious problems are already fixed, so whatever is still wrong there is what the rubric most needs to catch. Then take each other output and record each way it falls short of the best.
- Never accept a summary of the differences, its own included, as the failure list. Open the cells.
- Run the tests rather than assuming: change a key input in a test copy and trace it through; build in a deliberate mismatch and see whether a check row catches it; add rows and a new period; refresh what should refresh; open the file in the Excel version the job needs; read the reply and test each claim against the file.
- Recompute every important value from the inputs, and check how each model handled every place where two sources disagree.
- For each failure record what is wrong, what should happen instead, where it can be seen by sheet and label, and why it matters, then classify it under the six modes and the four categories in reference 05.
- Count one underlying error once. Roll repeated symptoms up under the cause that produced them and say which cause. A wrong source input flowing consistently through the workbook is one source error; a summary that independently stops updating is a separate linking error.
- Mark each failure as a candidate criterion or not, and name any failure none of the four categories fits.
- If every failure found is minor, say so plainly: that is a finding about the task, not the rubric.
- Answer inline under T1 to T8 in SKILL.md, in template D's order, closing with the count of independent failures and how many are candidate criteria.

Re-verify every failure before relaying, testing it against the file rather than against the model's own account of it.
