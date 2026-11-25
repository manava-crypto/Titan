---
description: Screen a Project Titan task idea against Real, Fair and Hard before it is proposed
argument-hint: "[path to the task pack, or leave blank to use attached/most recent files]"
---

Screen the **Titan task** at: $ARGUMENTS

If no path is given, inventory the files attached or most recently referenced and confirm the pack before screening.

Delegate to the `project-titan-excel-tasks` agent via the Agent tool. Brief it to:

- Read `skills/project-titan-excel-tasks/SKILL.md` and, in `references/`, `02_task_design_standards.md`, `03_prompt_standards.md`, `04_file_preparation_and_integrity.md`, `12_checklists.md`, `13_human_voice_and_ai_tells.md` and template A of `09_output_templates.md` before any verdict.
- Paste into the brief, verbatim, the expert's own prompt, scenario, headline checks and any screening feedback already received.
- Read every supplied file in full, including hidden sheets, comments, external links and file properties. Previews and filenames are not evidence.
- Name the task type from the prompt and the files, not from what the expert called it.
- Judge Real, Fair and Hard separately. Fair means another expert, given only this prompt and these files, reaches the same answer with no web access and no questions. Where it fails Fair, name the two defensible answers and give the wording the prompt needs. Hard means leading models get it wrong; say which failure modes in reference 05 the difficulty sits on, and say plainly if the only failures available are minor.
- Run the before-you-submit list in 12 A: reference answer, cold read, scenario, three to five headline checks each with its source, period or scenario and an agreed tolerance, the allowed edit range for edit and fix tasks, delivery constraints, and the defect map for fix tasks.
- On a fix task, check the allowed range does not double as a defect map and that the solver's copy carries no leakage: no correct figure beside the defect it would expose, no change log, no checks block, no open-items list, no explanatory notes, no comments, no defined names.
- Check that every rule the answer turns on is in the prompt, and that no figure in the prompt is stated to a precision the files do not carry.
- Run the voice and build check in 13 over the prompt, the scenario and every file, and give the exact change for each tell.
- Recompute every headline check from the inputs. Mark anything you cannot check PENDING INPUT, naming the file.
- Answer inline under T1 to T8 in SKILL.md, in template A's order, with a single READY or NOT READY line naming the blocking items.

Re-verify every finding that drives a NOT READY before relaying, and relay one to one without stripping the replacement wording. List any change you made to the agent's calls in one lead line.
