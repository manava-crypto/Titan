---
description: Sweep a Project Titan file set for leakage, confidential content and anything that reads as machine-built
argument-hint: "[path to the file set, or leave blank to use attached/most recent files]"
---

Sweep the **Titan file set** at: $ARGUMENTS

Delegate to the `project-titan-excel-tasks` agent via the Agent tool. Brief it to:

- Read `skills/project-titan-excel-tasks/SKILL.md` and, in `references/`, `04_file_preparation_and_integrity.md`, `13_human_voice_and_ai_tells.md` and template C of `09_output_templates.md` before any verdict.
- Open every file in full. For each workbook: every sheet including hidden ones, hidden rows and columns, every comment and note, defined names, external links, data connections, embedded objects, pivot caches and file properties. Open it twice, once for formulas and once for cached values.
- Check the sanitisation is complete and consistent: client names, people and account numbers gone from the visible cells, the hidden ones, the comments and the metadata, and every reference to a renamed entity still resolving so the task still works.
- Check the stated provenance of each file, and flag any file with none.
- Check the inputs are real and messy rather than tidied, since tidy inputs are where models already do well.
- Check the features and the file format match the job, including a macro-capable format where macros are needed, and that nothing in the task depends on something the deliverable format cannot carry.
- Check for artificial tricks: inputs in white font, meaningless tab names, bans on normal functions.
- On a fix task, run the leakage sweep: no correct figure beside the defect it would expose, no change log, no checks block, no open-items list, no explanatory notes, no comments, no defined names in the solver's copy.
- Run the build check in reference 13 part 2 over every file: tab naming and structure, column widths, panes and page setup, number formats and colour conventions, date series regularity, round numbers, ID realism, status mixes, and the file properties including author, company, revision count and editing time. Each tell is a finding with the exact change.
- Answer inline under T1 to T8 in SKILL.md, one entry per file in template C's order, with a single READY or NOT READY line.

Re-verify every blocking finding before relaying, and keep the exact change on each one.
