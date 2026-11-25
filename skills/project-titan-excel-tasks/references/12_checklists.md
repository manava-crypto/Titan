# 12 · Checklists

Hand-over lists, in the guides' own order. Each is a gate, not a suggestion.

---

## A · Before the task is submitted

- [ ] **Reference answer built.** Solved in Excel and recalculated. Private; the model never sees it. Inputs, method and working noted behind each headline result.
- [ ] **Cold read done.** Another expert could reach the answer from the prompt and files alone. Rounding, periods, units and the active scenario are all settled.
- [ ] **Scenario written.** Who needs this, what exists, what changed, and what they expect back.
- [ ] **Three to five headline checks listed.** Each a result visible in the finished workbook, each naming its source, period or scenario, each with an agreed tolerance.
- [ ] **What the model may change is marked** (edit and fix tasks). Tabs and ranges. Everything else stays as it is. The range is not a list of the defect cells.
- [ ] **Delivery constraints checked.** Output format, Excel version, required features. Nothing in the task depends on something that cannot be returned.
- [ ] **Defects mapped** (fix tasks). Where each problem is, what is wrong, what the fix looks like. Private.
- [ ] **Files sanitised.** Hidden sheets, comments, metadata, external links, data connections, embedded objects. Renaming consistent. Permission to share confirmed.
- [ ] **Provenance stated** for each file.
- [ ] **No leakage in the solver's copy.** No correct figure beside the defect it would expose, no change log, no checks block, no open-items list, no explanatory notes, no comments, no defined names.
- [ ] **Nothing invented.** No figure, rate, price or contractual term that is not in the pack.
- [ ] **Voice and build checked** against reference 13, on the prompt, the scenario and every file.

---

## B · Before the rubric is submitted

From the rubric guide's own checklist.

- [ ] Every item on the step-one list is a criterion.
- [ ] Every output asked for has its value checked, not just its presence, and every feature asked for is tested to work.
- [ ] Each real model mistake has a criterion that describes the right answer.
- [ ] Each criterion is one short sentence, checks one thing, reads on its own, and has no cell reference.
- [ ] Numbers have three significant figures, and each names its source where inputs could conflict.
- [ ] Every calculated key value has a Method criterion, and only root values carry a fixed number.
- [ ] Nothing repeats what is already covered: live formulas, hygiene, merged cells, cut-off text, file basics.
- [ ] Each criterion is tagged Outcome or Quality, with Domain Specific where it applies.
- [ ] There are at least ten criteria, and no two contradict each other.
- [ ] Edit and fix tasks: the allowed range is listed and the three standing criteria are in.
- [ ] The reference answer, if built, passes every criterion.
- [ ] Every criterion reads in the expert's own voice (reference 13).

### The three last tests

- [ ] If a workbook passed every criterion, would you still send it back? If yes, a criterion is missing.
- [ ] Would the laziest workbook that could pass — pasted values, IFERROR everywhere — still score well? If yes, a criterion is missing.
- [ ] In an open task, do at least a third of the Quality criteria test a decision the model had to make?

---

## C · Final QA, before anything is handed over

- [ ] Every figure in the rubric recomputed from the input files, not from a workbook.
- [ ] Every tolerance agreed and recorded, with any residue explained.
- [ ] Every criterion changed since the last pass still reads on its own, still passes the best workbook, still tagged right.
- [ ] Broken copies tested, one break at a time, and every break is caught by a named criterion.
- [ ] A second defensible approach worked through, and every criterion still passes it.
- [ ] Scenario independence confirmed: perturbing a downside input does not move the base-case outputs.
- [ ] Both workbooks, where there are two, recalculate with zero formula errors and zero circular references.
- [ ] Every defect-map cell differs between the solver's copy and the golden.
- [ ] Leakage sweep clean.
- [ ] Every platform field matches the file: tab count, ranges, file names, deliverable list.
- [ ] File properties cleared and timestamps realistic on every file.
- [ ] Voice and build check run across every surface (reference 13).

---

## D · What is handed over

Task:

- The prompt.
- The input files, sanitised, each with its source stated.
- The scenario.
- Three to five headline checks, each with source, period or scenario and tolerance.
- The allowed edit range, for edit and fix tasks.
- Delivery constraints.
- Privately: the reference answer, and for fix tasks the defect map.

Rubric:

- At least ten criteria, each a yes or no.
- An Outcome or Quality tag on every one.
- A Domain Specific tag where a field convention applies.
- The key outputs: the figures the workbook exists to produce.
- The allowed edit range again, for edit and fix tasks.
