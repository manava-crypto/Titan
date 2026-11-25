---
description: Draft a Project Titan rubric from the failure list, the prompt and the files
argument-hint: "[path to the failure list, prompt, files and outputs, or leave blank to use attached/most recent files]"
---

Draft the **Titan rubric** for: $ARGUMENTS

Delegate to the `project-titan-excel-tasks` agent via the Agent tool. Brief it to:

- Read `skills/project-titan-excel-tasks/SKILL.md` and, in `references/`, `05_failure_taxonomy.md`, `06_rubric_criterion_craft.md`, `07_tagging_and_coverage.md`, `10_worked_examples.md`, `13_human_voice_and_ai_tells.md` and template E of `09_output_templates.md` before drafting.
- Have open: the prompt, the input files, the failure list, the expert's reference answer and headline checks if they exist, and each model's workbook and reply.
- Start from step one: read the prompt and list everything it fixes — every output, period, entity and scenario asked for, the values, the method, the scope, the template. Each item gets at least one criterion. The headline checks go in here too.
- Then the failure list: each real, independent model mistake gets a criterion that describes the right answer, never the mistake.
- Write each criterion as one short, plain sentence on the pattern: the thing by its label, then is, shows, matches or includes, then the expected result. Eight to twenty words. Readable on its own. No cell references.
- Apply the twelve rules in reference 06, in particular: exact numbers to three significant figures, with counts, dates, IDs and labels matching exactly and everything else within one per cent; a band for values near zero; the source named wherever inputs could conflict; a Method criterion for every calculated key value, stating the relationship rather than the function, with fixed numbers only on root values from the inputs.
- Recompute every figure from the input files before it goes in a criterion. Any figure that has not been rebuilt from the inputs is named NOT VERIFIABLE rather than filled with a plausible number.
- Tag every criterion Outcome or Quality using the four questions in 07 in order, adding Domain Specific only where a field convention applies and the prompt sets that audience. Write nothing for anything on the universal list.
- Cover every Core area of the task's type using the matrix in 07, and include the three standing criteria on any edit or fix task, with the allowed range named by sheet and row or column labels rather than cell addresses.
- Where several answers are defensible, define the feasible set and the rule that bounds it, not one value.
- Aim at ten or more criteria, around twenty for a complex task, as a starting point and never as a target.
- Vary the sentence shape across the set and name tabs and columns rather than "the output", so it reads as one practitioner's work; run the voice check in 13 over the finished set.
- Answer inline under T1 to T8 in SKILL.md, in template E's order, closing with the key outputs, the numbers used and their sources, the coverage map, and what was deliberately not written.

Before relaying, run the four whole-rubric tests and the probe battery in reference 11 over the draft, and say which criteria you changed as a result.
