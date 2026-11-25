# Project Titan — Excel Task Authoring Framework

Project Titan is an Aptura programme in which an expert builds a real Excel job that leading AI models get wrong, then writes a rubric of pass/fail criteria that scores each model's attempt. This repository is the operating kit for that work: an agent, a skill, seven stage commands and thirteen references, built from the Titan task guide, the Titan rubric guide and the Excel rubric one-pager, with the Stellantis credit model repair as the worked fix-task example.

## How Titan works

The expert hands a model the files they would hand a colleague, plus one prompt asking for the work. The model does the job in Excel, with no follow-up questions and no web access. The expert compares the model's workbook with their own answer and writes the rubric.

| | |
|---|---|
| The task | the exam |
| The prompt and files | the question |
| The model's output | a student's attempt |
| The rubric | the answer key |

An AI grader then opens each workbook, recalculates it, reads the reply, and marks one criterion at a time: met or not met. The score is the share of criteria met, each counting the same. The grader sees the prompt, the input files, the workbook and the reply, and nothing else — so anything the expert did not write down does not exist for it.

### The pipeline

Task side: the expert proposes the task → Aptura screens it → the expert builds it on the task platform → the models run it → the expert writes the rubric → review and final QA.

Rubric side: the expert submits the rubric → a second reviewer rebuilds their numbers and tries the rubric on broken copies of the best output → the expert changes what comes back → final QA → task complete.

### A task has to be Real, Fair and Hard

**Real** — based on work the expert or their team have actually done, sanitised, testing how someone works in Excel. **Fair** — another expert, given only this prompt and these files, reaches the same answer, with no web access and no questions. **Hard** — leading models get it wrong; a one-formula exercise will not do it.

Fair and hard pull against each other. If two experts could defend different answers, the task is ambiguous rather than hard, and it will not be accepted: a model failing a vague brief says nothing about its capabilities.

### Three task types

**Build from scratch** — a brief and source documents; the model designs and builds the workbook, and it has to keep working when the inputs change. **Edit or extend** — a working workbook and a new input or requirement, taken forward in the workbook's own style, changing only what the request needs. **Fix a messy workbook** — an inherited, broken or half-finished workbook with a private defect list; the model finds and repairs the problems without breaking what already worked.

## The stages, and what the copilot does at each

| Stage | Command | What it does |
|---|---|---|
| Task screening | `/titan-task-check` | Judges Real, Fair and Hard; names the type; runs the before-you-submit list; checks the allowed range does not double as a defect map |
| Prompt check | `/titan-prompt-check` | Walks the prompt sentence by sentence, lists everything the answer depends on, cold-reads it, and writes the replacement wording |
| File check | `/titan-files-check` | Sweeps hidden sheets, comments, metadata, links and connections; checks provenance, features and format; runs the leakage sweep and the build check |
| Failure hunt | `/titan-failure-hunt` | Walks the best workbook cell by cell, then the others; classifies each failure by mode and category; counts one underlying error once |
| Rubric draft | `/titan-rubric-write` | Writes the criteria from the failure list, the prompt and the files, each tagged, with every figure recomputed from the inputs |
| Rubric check | `/titan-rubric-check` | KEEP, REWRITE or DROP on every criterion, then coverage, tags, contradictions and the four whole-rubric tests |
| Final QA | `/titan-final-qa` | Rebuilds every number, breaks the best output one defect at a time, tests a second valid approach, and runs the hand-over lists |

## The rules the framework enforces

**Write every criterion so a correct workbook passes it.** Describe what good looks like, not the mistake that was seen. A criterion that names the mistake can be passed by a different wrong answer; one that names the right result cannot.

**One check per criterion, one sentence, eight to twenty words**, readable on its own, naming things by their label and never by cell reference, with exact numbers to three significant figures — counts, dates, IDs and labels matching exactly, everything else within one per cent, a band for values near zero — the source named wherever inputs could conflict, and a Method criterion for every calculated key value.

**Tag Outcome or Quality**, adding Domain Specific only where a field convention applies and the prompt sets that audience. Four questions settle it, and the first does most of the work: if the prompt, an input file or the template fixes it, it is Outcome even when it feels like a judgement call.

**Never write a criterion for anything already checked on every task** — live formulas, formula hygiene, working checks, merged cells and units, hashes and cut-off text, file basics. A broken one of those is an escalation to the platform, not a criterion.

**A rubric has to pass the best work, fail what would be sent back, resist pasted values and IFERROR, and accept a defensible alternative.** At least ten criteria, around twenty for a complex task — starting points, never targets.

**Count one underlying error once.** A wrong source input flowing consistently through the workbook is one source error, not one per affected cell. A summary that independently stops updating is a separate linking error.

**Everything has to read as expert-built.** The prompt, the scenario, every input file, the workbook and the criteria. Reference 13 lists what reads as generated — in prose and in a workbook's structure, formatting, data and file properties — and what a real working file carries instead.

## Repository structure

```text
project-titan/
├── README.md                           # this file
├── CLAUDE.md                           # routing and house rules
├── .claude/
│   ├── agents/
│   │   └── project-titan-excel-tasks.md
│   ├── commands/                       # one slash command per stage
│   │   ├── titan-task-check.md
│   │   ├── titan-prompt-check.md
│   │   ├── titan-files-check.md
│   │   ├── titan-failure-hunt.md
│   │   ├── titan-rubric-write.md
│   │   ├── titan-rubric-check.md
│   │   └── titan-final-qa.md
│   └── skills/
│       └── project-titan-excel-tasks -> ../../skills/project-titan-excel-tasks
├── rules/
│   └── project-titan-excel-tasks.mdc   # Cursor rule, always applied
└── skills/
    └── project-titan-excel-tasks/
        ├── SKILL.md                    # operative rules for every stage
        └── references/
            ├── 01_titan_program_and_workflow.md     # pipeline, scoring, hand-overs
            ├── 02_task_design_standards.md          # Real, Fair, Hard; the three types
            ├── 03_prompt_standards.md               # say, leave out, worked contrasts
            ├── 04_file_preparation_and_integrity.md # sanitisation, provenance, tricks
            ├── 05_failure_taxonomy.md               # six modes, five areas, four categories
            ├── 06_rubric_criterion_craft.md         # the pattern and the twelve rules
            ├── 07_tagging_and_coverage.md           # tags, four questions, coverage matrix
            ├── 08_rubric_stress_tests.md            # shortcuts, broken copies, last tests
            ├── 09_output_templates.md               # templates A to H
            ├── 10_worked_examples.md                # Series A cap table; Stellantis repair
            ├── 11_failure_patterns_and_lessons.md   # how rubrics go wrong; probe battery
            ├── 12_checklists.md                     # task, rubric and final QA checklists
            └── 13_human_voice_and_ai_tells.md       # making everything read as expert-built
```

## Using it

In Claude Code, open this repository, type the stage command and attach the pack:

```bash
/titan-rubric-check
```

Elsewhere, the skill and its references are self-contained: point any agent at `skills/project-titan-excel-tasks/SKILL.md` and it will load what each stage needs. For Cursor, `rules/project-titan-excel-tasks.mdc` applies automatically.

## Sources

Built from the Titan task guide (eight sections: the idea, a good task, task types, the prompt, example, model failures, files, before you submit), the Titan rubric guide (nine sections: what a rubric is, five habits, what good looks like, four steps, find the failures, write each criterion, tag each criterion, good versus bad, before you submit), and the Excel failures and good rubrics one-pager (five failure areas, good versus weak criteria, the two criterion types, how many criteria). The Stellantis credit model repair supplies the worked fix-task example and the screening lessons in reference 11.
