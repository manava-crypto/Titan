# Project Titan / Aptura — Excel Task Authoring

This repository is the operating framework for the Project Titan Excel Task Copilot. Titan is the Aptura programme in which an expert builds a real Excel job that leading AI models get wrong, then writes a rubric of pass/fail criteria that scores each model's attempt. Its stages are task screening, the build, the model run, the rubric, and final QA.

## Route stage work to the agent

Whenever the user asks for Titan task screening, a prompt check, a file or sanitisation sweep, a model failure hunt, rubric drafting, a rubric audit, a tagging or coverage check, a rubric stress test, or the final QA pass before submission, delegate to the `project-titan-excel-tasks` agent (`.claude/agents/project-titan-excel-tasks.md`) rather than answering directly. The slash commands `/titan-task-check`, `/titan-prompt-check`, `/titan-files-check`, `/titan-failure-hunt`, `/titan-rubric-write`, `/titan-rubric-check` and `/titan-final-qa` each set up one stage.

## Rulebook

The standards, templates and worked examples live in `skills/project-titan-excel-tasks/` (symlinked into `.claude/skills/` so the skill is discoverable, and referenced by `rules/project-titan-excel-tasks.mdc` for Cursor). Before any verdict, load `SKILL.md`, the stage's template in `references/09_output_templates.md`, `references/11_failure_patterns_and_lessons.md` and `references/13_human_voice_and_ai_tells.md`, plus whichever of 01 to 12 the stage needs: 02 to 04 for task, prompt and file work, 05 for any failure hunt, 06 to 08 for any rubric work, 10 for the worked examples, 12 for the checklists.

## House rules

Read every supplied file in full, open each workbook twice for formulas and cached values, and recompute every figure the task turns on from the inputs rather than from any workbook's cells. Previews, filenames and a model's own reply are not evidence. Mark anything you cannot check PENDING INPUT, naming the file, rather than filling the gap.

Walk the best model workbook cell by cell before the others, never accept a summary of the differences as the failure list, and count one underlying error once however many symptoms it has. Test rather than assume: change a key input and trace it, build in a deliberate mismatch, add rows and a period, refresh what should refresh, open the file in the Excel version the job needs. If every failure you can find is minor, say so: that is a finding about the task, not the rubric.

Write every criterion so a correct workbook passes it: the right result, never the mistake; one check each; eight to twenty words; readable alone; named by label, never by cell reference; exact numbers with an agreed tolerance; the source named where inputs conflict; a Method criterion for each calculated key value, with fixed numbers only on root values from the inputs. Tag Outcome or Quality using the four questions in order, with Domain Specific only where a field convention applies and the prompt sets that audience, and never write a criterion for anything on the universal "already covered" list — a broken one of those is an escalation line. A rubric has to pass the best work, fail what would be sent back, resist pasted values and IFERROR, and accept a defensible alternative; at least ten criteria, around twenty for a complex task, as a starting point and never a target.

You draft: prompts, scenarios, headline checks and criteria are written out in full, from the expert's own material and never from an invented fact. Everything shipped has to read as though a practitioner built it — the prompt, the scenario, every input file, the workbook and the criteria — so apply reference 13 at every stage, to tab naming, formatting, data realism and file properties as well as to prose.

Answers are concise and inline under T1 to T9 in SKILL.md: an optional lead of one paragraph, two at most; one entry per item in the expert's own order; a clean item in one sentence; a finding in one paragraph, two at most, ending with the replacement written out; bullets only for three or more separate points; prose, not tables. Write in plain words an experienced Excel practitioner would use, with no file internals or tool names.

Delegation briefs quote the stage's bar, the rule that every criterion must be passed by a correct workbook, the four whole-rubric tests, T1 to T9, and the expert's own text verbatim. Re-verify every finding that drives a DROP, a REWRITE or a NOT READY, and relay one to one without stripping the replacement.

Keep scratch scripts and extracts in the scratchpad directory, and never write task files, rubrics or stage output into the repository.
