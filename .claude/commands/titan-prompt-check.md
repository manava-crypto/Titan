---
description: Audit a Project Titan prompt line by line and return the replacement wording
argument-hint: "[path to the prompt and files, or leave blank to use attached/most recent files]"
---

Audit the **Titan prompt** at: $ARGUMENTS

Delegate to the `project-titan-excel-tasks` agent via the Agent tool. Brief it to:

- Read `skills/project-titan-excel-tasks/SKILL.md` and, in `references/`, `03_prompt_standards.md`, `13_human_voice_and_ai_tells.md` and template B of `09_output_templates.md` before any verdict.
- Paste the prompt into the brief verbatim, with the file list and the task type.
- Walk the prompt sentence by sentence. Each sentence is context, a constraint, or a choice the answer depends on. Anything else is prescribing a method or pointing at a trap, and both remove the difficulty.
- List everything the answer depends on — scenario, period, units, rounding, what must not change, output format, Excel version, features — and say for each whether it is in the prompt or does not matter.
- Apply the test for a choice: if two good professionals could reasonably choose differently and the answer changes, the prompt states it; if everyone would do it the same way, it stays out. House style counts as a choice.
- Cold read it: reading only the prompt and the files, name the answer. If two readings survive, the prompt is underspecified, not hard.
- Check no figure in the prompt is stated to a precision the files do not carry, and that every constraint built into the workbook appears in the prompt.
- Run the voice check in 13 over every sentence, and give the rewrite for each tell.
- For every finding, head the entry with the quoted phrase, give the rule in one plain sentence, say what a model or grader does with it, then write out the replacement wording in full.
- Answer inline under T1 to T8 in SKILL.md, in template B's order, with a single READY or NOT READY line.

Re-verify every finding that drives a NOT READY before relaying, and relay the replacement wording verbatim.
