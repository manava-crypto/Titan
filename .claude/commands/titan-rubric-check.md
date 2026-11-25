---
description: Audit a drafted Project Titan rubric criterion by criterion and stress-test the set
argument-hint: "[path to the rubric, prompt, files and outputs, or leave blank to use attached/most recent files]"
---

Audit the **Titan rubric** at: $ARGUMENTS

Delegate to the `project-titan-excel-tasks` agent via the Agent tool. Brief it to:

- Read `skills/project-titan-excel-tasks/SKILL.md` and, in `references/`, `06_rubric_criterion_craft.md`, `07_tagging_and_coverage.md`, `08_rubric_stress_tests.md`, `11_failure_patterns_and_lessons.md`, `13_human_voice_and_ai_tells.md` and template F of `09_output_templates.md` before any verdict.
- Paste the expert's criteria into the brief verbatim, in their numbering, with the prompt, the file list, the task type and the failure list.
- Judge each criterion as the grader will: it sees the prompt, the input files, the model's workbook and its reply, and nothing else. Anything not written down does not exist for it.
- Give each criterion KEEP, REWRITE or DROP. On a REWRITE, quote the phrase that breaks the rule, name the rule, say what a grader or model does with it, then write out the replacement sentence with its tag. On a DROP, say why: on the universal list, a duplicate of another criterion, analysis nobody asked for, or written to fail one particular output.
- Run the twelve rules in 06 and the full probe battery in 11 on every criterion before any KEEP, including: would a correct workbook fail this; would a wrong workbook pass it; can the grader mark it without asking what the expert meant; does it survive a row insertion; has the number been recomputed from the inputs; was the tolerance agreed rather than defaulted to.
- Recompute every figure in the rubric from the input files, not from the golden or the best output.
- Check the tags against the four questions in 07 in order, remembering that question one does most of the work: anything the prompt, an input file or the template fixes is Outcome even when it feels like a judgement call.
- Check coverage against the matrix in 07 for this task type, and on an edit or fix task confirm the three standing criteria and the allowed range.
- Then the set: the count against the task's complexity, contradictions between criteria, any single realistic mistake failing more than two criteria, and the four whole-rubric tests — passes the best work, fails what the expert would send back, cannot be gamed, accepts good alternatives.
- Run the shortcuts table and the three last tests in 08.
- Write a MISSING entry, with the criterion written out, for each uncovered item on the expert's step-one list, each real model mistake with no criterion, and each Core area with none.
- Run the voice check in 13 over the set: hedging, uniform sentence shape, generic nouns in place of named tabs and columns.
- Answer inline under T1 to T8 in SKILL.md, in template F's order, with a single READY or NOT READY line naming the blocking items.

Re-verify every DROP and every REWRITE before relaying, re-testing the rule it rests on rather than only the quoted phrase, and relay the replacements verbatim.
