# 02 · Task design standards

## The three tests

A Titan task has to pass all three. They are from the task guide, section 2.

**Real.** Based on work the expert or their team have actually done, with anything confidential removed. It tests how well someone works in Excel: logic that holds up, formulas and features that work, and a file the end user is happy to use.

**Fair.** Another expert, given only this prompt and these files, would reach the expert's answer. Everything needed is in the files. The model has no web access and cannot ask questions.

**Hard.** Leading AI models get it wrong. A one-formula exercise will not do it, and neither will cleaning data with a single obvious method.

## Where fair and hard collide

This is the judgement that decides most screening calls, and it is worth quoting: "Fair and hard pull against each other. If two experts could defend different answers, the task is ambiguous, not hard. A model failing a vague brief tells us nothing about its capabilities, and the task won't be accepted."

The test to apply: name the two defensible answers. If you can name them and the prompt does not settle which is wanted, the task is ambiguous and the prompt has to state the choice. If you cannot — if a second expert in the field would read it the same way — the difficulty is real.

The Series A example in reference 10 is the model for this. The gap between two option figures is a trap, but every experienced VC analyst reads it the same way because the founder emails support that reading. Take the emails away and the same gap becomes ambiguity, and the prompt or files would have to say how to treat it.

## Where models actually slip

Models do well at straight calculation on tidy inputs. They slip where the job needs expert judgement or experience. A task whose whole difficulty is arithmetic on a clean table is not hard in the Titan sense, however long the arithmetic is.

The six failure modes in reference 05 are the places to look for hardness: a source conflict to read, a component that is easy to leave out, a formula that has to survive a changed input, work outside the allowed area, a workbook that has to hold up in real use, and a reply that has to be true of the file.

## The three task types

Pick one. From the task guide, section 3.

**Build from scratch.** The expert supplies a brief and source documents. The model designs and builds the workbook, and it has to keep working when the inputs change. Example: a project finance model with debt sized to a target debt service cover ratio.

**Edit or extend an existing workbook.** The expert supplies a working workbook and a new input or requirement. The model takes it forward as a piece of work: a new period, scenario or analysis, built in the workbook's own style, changing only what the request needs. A one-off tweak to a single cell is too small, but a small edit can expose a real problem if its effects have to flow through the whole model. Example: roll a month-end close pack forward using next month's trial balance.

**Fix a messy workbook.** The expert supplies an inherited, broken or half-finished workbook and keeps a private list of what is wrong. The model finds and repairs the problems without breaking what already worked. Example: a departed analyst's LBO with broken references and a hardcoded number buried in a formula.

The type decides which rubric areas are core: see the coverage matrix in reference 07. Edit and fix tasks also carry the three standing criteria in reference 06 and need an allowed edit range stated.

## Before the task is proposed

The checklist from the task guide, section 8. Each item is a screening question in template A.

- **Build the reference answer.** Solve the task in Excel and recalculate. Optional for build-from-scratch tasks, always helpful. It stays private; the model never sees it. It helps but it is not proof on its own, so note the inputs, the method and the working behind each headline result.
- **Do a cold read.** Could another expert reach the answer from the prompt and files alone? Fix anything underspecified: rounding, periods, units, which scenario is active.
- **Write the scenario.** Who needs this, what exists, what changed, and what they expect back.
- **List three to five headline checks.** Results visible in the finished workbook, such as "Equity IRR on the Returns tab is 21.4% (±0.1pp) in the base case". Say which source, period or scenario each check uses, and agree a tolerance for each number rather than falling back on a default. They give a quick first read on each model's workbook. They are a starting point, not the rubric.
- **Mark what the model may change** (edit and fix tasks). Tabs and ranges; everything else stays as it is. Values that change because the edit flows through the model are fine. Formulas or content changed without being asked are not.
- **Check delivery constraints.** Output format, Excel version and required features. If only a workbook can be returned, the task must not depend on a separate script.
- **Map the defects** (fix tasks). Where each problem is, what is wrong, and what the fix looks like. Private, like the answer.

## What gets a task screened out

- Two defensible answers and no stated choice.
- Difficulty that is only volume: more rows of the same arithmetic.
- A single obvious method with no judgement in it.
- An edit so small that nothing flows through.
- A trick rather than a job: hidden white-font inputs, meaningless tab names, a ban on a normal function.
- Inputs or prompt made or altered with AI.
- Material the expert does not have permission to share, or that is not sanitised.
- A dependency on something that cannot be returned, such as a separate script, when only a workbook can come back.
- Failures that are all minor. If the only things the expert can find are small, the task is not hard enough.
