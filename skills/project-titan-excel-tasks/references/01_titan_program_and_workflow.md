# 01 · The Titan programme and its workflow

## What Titan is

Project Titan builds a benchmark out of real Excel work. An expert hands an AI model the files they would hand a colleague, plus one prompt asking for the work. The model does the job in Excel, with no follow-up questions and no web access. The expert then compares the model's workbook with their own answer and writes a rubric: a list of pass/fail checks describing what a good workbook gets right.

The exam analogy the rubric guide uses is worth holding on to:

| The task | the exam |
| The prompt and files | the question |
| The model's output | a student's attempt |
| The rubric | the answer key |

The task is only as good as the expert's idea of good. Anything the rubric does not check counts as fine; anything it gets wrong fails a good answer.

## The pipeline

Task side, from the task guide:

1. The expert proposes the task.
2. Aptura screens it.
3. The expert builds it on the task platform.
4. The models run it.
5. The expert writes the rubric.
6. Review and final QA.

If the idea is accepted, the expert gets feedback to work into the build, and from then on has a named reviewer and a Slack channel for questions.

Rubric side, from the rubric guide:

1. The expert submits the rubric.
2. A second reviewer rebuilds the expert's numbers and tries the rubric on broken copies of the best output.
3. The expert changes what comes back.
4. Final QA.
5. Task complete.

A criterion that rejects a workbook a second expert would send as it is, or that lets a broken copy through, comes back to the expert. That is the single most common reason work returns.

## How a rubric is scored

The expert writes the criteria after the models have run. An AI grader then opens the workbook, recalculates it, reads the reply, and marks one criterion at a time: met or not met. The score is the share of criteria met, each counting the same.

Three consequences follow, and they drive most of the rules in these references:

- The grader sees the prompt, the input files, the model's workbook and its reply, and nothing else. It cannot ask what the expert meant. Anything not written down does not exist.
- If the model should have produced something a criterion looks at and did not, that counts as not met.
- Every criterion counts the same, so a vague criterion costs as much as a sharp one. There is no importance level to set.

## The three QA layers

Work is checked in three ways, and knowing which layer catches what stops an expert writing criteria that are already covered:

- Automated checks flag file differences and formula patterns.
- Excel testing verifies recalculation, refresh and interactive features.
- Expert review judges source interpretation, professional assumptions and materiality.

The universal list in reference 07 is what the first two layers already handle on every task.

## What the expert hands over

For the task:

- The prompt, written by the expert without AI.
- The input files, sanitised, with the source of each one stated.
- The scenario: who needs this, what exists, what changed, what they expect back.
- Three to five headline checks, each with its source, period or scenario and an agreed tolerance.
- The allowed edit range, for edit and fix tasks.
- Delivery constraints: output format, Excel version, required features.
- Privately: the reference answer, and for fix tasks the defect map.

For the rubric:

- At least ten criteria, each a yes or no.
- An Outcome or Quality tag on every criterion.
- A Domain Specific tag where a field convention applies.
- The key outputs: the figures the workbook exists to produce.
- The allowed edit range again, for edit and fix tasks.

## Where this copilot sits

The copilot checks the expert's work at each stage and never produces the work itself. The stages map to the commands:

| Stage | Command | Template |
| Screening a task idea before it is proposed | `/titan-task-check` | A |
| Auditing the prompt | `/titan-prompt-check` | B |
| Checking the file set | `/titan-files-check` | C |
| Hunting the failures in the model outputs | `/titan-failure-hunt` | D |
| Auditing the drafted rubric | `/titan-rubric-check` | E |
| The pass before submission | `/titan-final-qa` | F |

The house voice rules in SKILL.md and reference 13 apply at every one of them.
