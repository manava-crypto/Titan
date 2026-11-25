# 05 · The failure taxonomy

Three lists describe the same ground from different angles, and the guides use all three. The six **failure modes** say what the model did wrong. The five **workbook areas** say where in the file to look. The four **rubric categories** say which part of the rubric the failure belongs to. Classify each failure under all three; the mapping at the end does the translation.

## The six model failure modes

From the task guide, section 6. Wrong headline numbers are the obvious failure and are caught by the headline checks and the reference answer. These are the ones that show up most often beyond that.

**1. Gets the data or calculation wrong.** Uses the wrong source, leaves out a component, misreads a period, or applies the wrong calculation.
How to spot it: reproduce the important values from the inputs yourself, and check how the model handled any place where the sources disagree.

**2. Builds fragile or disconnected formulas.** Numbers typed over formulas, lookups that ignore the inputs, check rows that can never fail. It looks right today and breaks tomorrow.
How to spot it: in a test copy, change a key input and watch whether it flows through. Build in a deliberate mismatch to see whether a check row catches it. Text or a constant in a formula is not a mistake on its own; count it when it breaks something the job needs.

**3. Leaves work missing or damages what was there.** Skips a required period, entity or piece of detail, or changes things outside the area it was asked to work on.
How to spot it: go through the prompt line by line and find each ask in the workbook. Then compare what should be untouched with the starting file.

**4. Breaks in real use.** Works on the data in the file but not once the workbook is used for real: more rows, a new period, the Excel version the team runs, or a feature the job asked for.
How to spot it: in a test copy, add rows or a new period, refresh anything that should refresh, and open the file in the Excel version the job needs.

**5. Hard to use or misleading.** Relies on assumptions the files do not support, loses what the template was showing, hides a limitation, or buries the result under helper material.
How to spot it: ask whether you would send the file to your manager or client as it is.

**6. Claims what it did not do.** The reply says the balance sheet balances or every case is covered, and the workbook shows otherwise.
How to spot it: read the reply and test each claim against the file.

## The five workbook areas

From the rubric one-pager. Use these as the inspection route through a workbook. Not every area applies to every task.

**1. Data and calculation accuracy.** Source figures, dates, units and categories match the inputs. Calculations use the right logic, denominator and financial treatment. Look for missing inputs, boundary errors and totals that do not reconcile.

**2. Formula links and meaningful checks.** Calculated outputs link to the relevant inputs and supporting calculations. Input changes flow through the affected totals and summaries. Reconciliation checks compare values that can genuinely differ. Look for hardcoded outputs, stale links, typed "Pass" labels and checks that compare a value with itself.

**3. Completeness and preservation.** All required periods, entities, scenarios and supporting detail are included. Existing content outside the requested changes is preserved. Look for omitted results, unrequested edits and lost formulas, formatting or workbook objects.

**4. Functionality, compatibility and reuse.** Required features work in the user's Excel version. The solution handles the stated data size and future additions within the task's scope. Look for broken filters, dropdowns or refreshes, missing required add-ins and unsupported formulas. Check that fixed ranges do not cut off new data.

**5. Presentation and professional judgment.** Labels, units and visual distinctions make the result easy to interpret. Required template meaning is preserved and helper material does not obscure the output. Material assumptions are justified and explanations reflect the workbook. Look for misleading conclusions or hidden uncertainty. Judge against the task and audience, not personal taste.

## The four rubric categories

From the rubric guide, section 5. These are the headings a rubric has to cover, and an AI assigns each criterion its category after submission, so the expert does not tag them. Walk the best workbook cell by cell against these questions.

**Correctness — is it right, and is it all there?** (every task)
- Is everything asked for there, all the way through?
- Are the values and units right?
- Did it read hidden rows, colour-coded cells, stale tabs, and an email that overrides a register?
- Do the totals tie?
- Is the method the one asked for?

**Craft — is it built the way people in the field expect?** (every task)
- Are inputs, drivers and outputs kept apart?
- Is the layout what someone in the field would expect?
- Do the field's colour and format conventions and the template's styling hold?
- Does a chart, pivot or rule the prompt asked for actually work?

**Scope — did it change only what it should?** (edit and fix tasks)
- Did edits stay inside the allowed range?
- Did every dependent output update?
- Is each planted error fixed at its source, not covered up?
- Was anything correct left alone?
- Is anything added that the recipient would need to delete?

**Judgement and communication — did it flag, explain and describe the file truthfully?** (every task)
- Did it flag input errors and false premises?
- Did it state its assumptions?
- Does the reply give the answer, and match what is in the file?
- Does it get the field's technical content right?

If a problem fits none of the four, write the criterion anyway and tell the reviewer.

## The mapping

| Failure mode | Workbook areas to inspect | Rubric category |
| 1 Data or calculation wrong | 1 | Correctness |
| 2 Fragile or disconnected formulas | 2 | Correctness, and Craft where it is structure |
| 3 Work missing or damaged | 3 | Correctness for missing, Scope for damaged |
| 4 Breaks in real use | 4 | Craft |
| 5 Hard to use or misleading | 5 | Craft, and Judgement where it is a hidden limitation |
| 6 Claims what it did not do | 5 | Judgement and communication |

## Counting mistakes once

This is where failure lists go wrong, and it feeds straight into the rubric, because counting a mistake several times means one slip fails four criteria.

- A wrong source input that flows consistently through the workbook is **one source error**. It is not one error per affected cell.
- A summary that independently stops updating is a **separate linking error**, even if it shows the same wrong number.
- Several visible symptoms can come from one underlying issue. Name the issue, list the symptoms under it, and write the criterion against the issue.
- One independent mistake earns one criterion. If a single error would fail four criteria, keep the one or two that capture it best.
- Style counts only where the audience or an agreed standard calls for it.

## Finding the failures in practice

Walk the best workbook cell by cell first. Its obvious problems are already fixed, so whatever is still wrong there is what the rubric most needs to catch. Then go through the other outputs: each way one falls short of the best is a candidate criterion too.

Do not rely on an AI summary of the differences. It misses the subtle problems in formulas, structure, scope and judgement — which is most of what Titan is testing.

For each mistake, record four things: what is wrong, what should happen, where it can be seen, and why it matters.

If all that turns up is minor, say so: the task is probably not hard enough. That is a finding about the task, and it goes back to the task stage, not into the rubric.
