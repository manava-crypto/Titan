# 06 · Writing and judging a single criterion

## What a criterion is

One short, plain sentence about the finished workbook or the reply, in the expert's own words. The grader reads each criterion on its own, so it has to make sense without the others. The answer has to be a clear yes or no.

The test the one-pager gives: can another reviewer read the criterion, inspect the workbook, and reach the same pass-or-fail decision?

## The pattern

> [the thing, by its label] + [is / shows / matches / includes] + [the expected result]

- The Series A share price is £80.46.
- The cap table shows the existing unallocated pool of 767 options on its own line.

## The one rule to remember

Write every criterion so that a correct workbook passes it. Describe what good looks like, not the mistake that was seen. A criterion that names the mistake can be passed by a different wrong answer. A criterion that names the right result cannot.

> What the model did: labelled the 767-option gap "Unreconciled options" and created too many new options.
> What it should have done: treated the 767 as the existing unallocated pool, already in the plan but not yet granted.
> The criterion: *The cap table shows the existing unallocated pool of 767 options on its own line.*
> Not: *The model flags the 767 as a variance.* That describes the mistake, so a different wrong answer would pass.

## The twelve rules

**6.1 One check per criterion.**
Weak: The chart has axis titles and a legend and uses the right data range.
Good: The chart's data range covers all twelve months. (Titles and legend get their own criteria.)

**6.2 Describe the result, not the action or the mistake.**
Weak: Add a summary tab.
Good: The Summary tab shows the Series A price and fully diluted ownership by holder.

**6.3 Name things by their label, never by cell reference.**
Weak: Returns!F20 is 21.4%.
Good: Equity IRR in the base case is 21.4%.
A correct edit that inserts a row moves F20 and fails the weak version.

**6.4 Keep it short and human, about eight to twenty words.**
Weak: The Summary should ideally show, where appropriate, a clearly labelled post-money valuation.
Good: The Summary shows post-money valuation in £m.

**6.5 Make it readable on its own.**
Weak: That total matches the register.
Good: Total shares on Cap Table match the total on the Register tab.

**6.6 Say where the evidence is.**
Weak: The model flags the conflicting figures.
Good: The reply states that the founder email and the register give different option pool sizes.

**6.7 Give exact numbers.**
Weak: The Series A share price is about £80.
Good: The Series A share price is £80.46.
Use three significant figures. Counts, dates, IDs and labels must match exactly. Everything else is judged within one per cent. For values near zero, give a band: "within £0.01m of zero".

**6.8 Name the source when inputs could conflict.**
Weak: The option pool is correct.
Good: The total option pool on Cap Table is 11,764, from the founder email.

**6.9 Give each calculated key value its own Method criterion.**
Weak: The unallocated pool is calculated correctly.
Good: The unallocated pool equals the pool in the founder email less the options granted in the register.
State the relationship, not the function; reviewers use it to rebuild the number from the inputs. Only root values from the inputs carry a fixed number. Anything calculated from them gets the Method criterion alone, so one wrong input fails one criterion, not two.

**6.10 Check the result, not the method.**
Weak: The model uses XLOOKUP to pull holdings from the register.
Good: Each holder's shares on Cap Table match the Register tab.
Fix a method only when it changes the number. If the prompt leaves it open, list each accepted value.

**6.11 Check the value, not whether it is live.**
Weak: The Series A share price is £80.46 and is calculated by formula.
Good: The Series A share price is £80.46.
Live formulas are already checked on every key output. If the link itself is the point, say so: "The Summary price links to Cap Table."

**6.12 When the prompt asks for a feature, test that it works.**
Weak: Rounds above £10m are shown in green.
Good: A conditional formatting rule on Cap Table shows rounds above £10m in green. (Hand-filled colour does not count.)

## What makes a criterion good, and what makes one weak

Good: specific — it names what is being checked; observable — it describes a result that can be verified; focused — one meaningful property; grounded — it comes from the task, its inputs or a justified professional standard; useful — it catches something the recipient would care about; self-contained — it makes sense without the other criteria.

Weak: vague words such as "correct", "clean" or "professional" with no explanation; unrelated checks combined in one sentence; a favourite formula or style required without a reason; a check already covered elsewhere; an unverified expected value or an invented tolerance; a sentence written just to make one particular output fail.

## The three standing criteria for edit and fix tasks

Every edit and fix task carries these three. Fill in the allowed range, named by sheet and row or column labels rather than cell addresses, and the input file.

- **Outcome:** Every cell outside [allowed range] keeps its formula, constant and number format from [input file], except cells the reply names as fixing a further error.
- **Quality:** The reply lists every range it edited, and the list matches the cells that changed.
- **Quality:** Where the reply names a further error, the error is real and the fix is correct.

## How many criteria

At least ten for a straightforward task, covering the important requirements and the possible failures. Around twenty for a more complex task with several distinct calculations, behaviours or deliverables.

These are starting points, not targets. Add a criterion only when it covers an important, separate check. Never pad the set to reach a number, and never remove an essential check to come under one.

## Verifying before the criterion is used

- Verify the expected result against the inputs and the calculations, not against any model's workbook.
- Cover the important requirements without penalising the same error twice.
- Keep an important check even when every sample output passes it.
- Agree any tolerance before using it; do not fall back on a default.
- Explain a material change before changing what passes or fails.

## A note on voice

The rubric guide says reviewers check for AI-written criteria. Drafted criteria are fine to work from; read each one back and put it in the words you would use with a colleague before you submit, so the set reads as one person's.
