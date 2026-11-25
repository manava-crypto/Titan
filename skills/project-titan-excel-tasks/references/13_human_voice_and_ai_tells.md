# 13 · Human voice: making everything read as expert-built

Every surface of a Titan task is read by someone deciding whether a practitioner made it: the prompt, the input workbooks and documents, the scenario, the criteria, and anything the expert writes back. Reviewers check for AI language, and the tells are consistent enough to list. This reference is applied at every stage, not only when prose is being written.

The target is not "polished". It is **a file and a message that look like they came out of someone's working week**.

## Part 1 · Prose: the prompt, the scenario, the criteria, any memo or email in the file set

### Words and constructions to strike

Furthermore, moreover, additionally, in addition, notably, importantly, it is worth noting, it should be noted, that said, crucially, ultimately, fundamentally, comprehensive, robust, seamless, streamline, leverage, utilise, facilitate, delve, navigate, underscore, ensure (where "make sure" is meant), foster, holistic, granular, actionable insights, key takeaways, best practices, align with, in order to, a wide range of, plays a crucial role, serves as, stands as, is designed to.

Also strike: em dashes used as a rhythm device, three-adjective lists, a sentence that opens by restating the request, a closing sentence that summarises what was just said, and any "I hope this helps" register.

### Shapes to avoid

- **Parallel bullets of equal length.** Real notes have a long point, a short one, and a fragment.
- **Headers on a short message.** Nobody puts a heading on a four-sentence email.
- **Uniform hedging.** "Generally", "typically", "where appropriate", "as needed" sprinkled evenly.
- **Explaining the field's own vocabulary.** A practitioner writes "the TB" and moves on; they do not write "the trial balance (TB)".
- **No specifics.** No entity, no system name, no period, no deadline, no file name, no person.
- **Perfect consistency.** Every sentence the same length, contractions used or avoided with machine regularity.

### What to put in instead

- Field shorthand used without explaining it: the TB, the rota, the CLN register, band 6, DSCR, the close pack.
- Named specifics: the system an export came from, the period, the version, the day it is needed.
- A reason attached to a constraint: "board pack goes out Friday", not "there is a deadline".
- A reference to prior context: "same layout as June", "the one we talked about last week".
- Unround numbers: 11,764 and 10,997, not 12,000 and 11,000.
- One sentence that is not a full sentence. One aside in brackets. The odd abbreviation.
- The sender's own ordering: the thing they care about most first, not the thing a template would put first.

### Criteria specifically

Criteria are short and factual, so they carry fewer tells, but three stand out. **Hedged criteria** — "should ideally show, where appropriate" — read as generated and fail rule 6.4 as well. **Uniform sentence shape** across twenty criteria, every one starting "The workbook shows…", reads as generated; real sets vary between "The Series A share price is £80.46", "Each holder's shares on Cap Table match the Register tab" and "The reply states that the founder email and the register give different option pool sizes". **Generic nouns** — "the output", "the model", "the data" — where a practitioner names the tab, the column, the report.

## Part 2 · Workbooks: what makes a file look generated

A workbook built or filled by a machine is usually identifiable before any formula is read.

### Structure and naming

- A generic tab trio: Assumptions, Calculations, Output. Practitioners use the names their team uses — Inputs, TB, Wkgs, Summary, Sch 3, Old (do not use).
- Every tab in the same Title Case style, with no abbreviations and no leftovers.
- No stale tab, no superseded version, no tab anyone forgot to delete.
- Title blocks of identical structure on every sheet.

### Formatting and file state

- Default column widths everywhere; no frozen panes; no print area; no page setup.
- Number formats left at General, or applied with perfect uniformity across unlike columns.
- No colour convention at all, or a convention applied with machine consistency to every single cell.
- In a finance model: negatives not in parentheses, no units row, no £m or $k in the header.
- Cursor left on A1 on every sheet, every sheet at 100% zoom, no sheet scrolled.
- No defined names, no filters left on, no hidden helper column, no comment.

### Data

- Round numbers and clean ratios: growth at exactly 5.0%, a headcount of 100, a rate of 10%.
- Dates on perfectly regular spacing, all month-ends, no stub period, no weekend, no late adjustment.
- Sequential or hash-like IDs; descriptive slugs that name the thing they identify (ACME_CUST_001).
- A status column with an even mix and no outliers; a population with no duplicates, no blanks, no trailing spaces.
- Values that reconcile exactly with no rounding difference anywhere.
- No manual override row, no "adj per JS" line, no comment explaining why a number was forced.

### File properties

- Author blank or a default such as "Microsoft Office User"; Company blank; Manager blank.
- Created and last-modified within seconds of each other; revision number 1; total editing time zero.
- No earlier print date, no earlier saved-by, nothing a file that has been passed around would carry.

### What a real file carries

Keep the mess. An export with a code the lookup does not recognise. A column someone widened by hand. A filter left on. A note in a cell saying why a figure was overridden. A tab called "old" that nobody deleted. A number format applied to one block and not the one below it. Dates that run to the 28th because that is when the data was pulled. A total that is 3 out because of rounding, with a line to absorb it.

That mess is also where the difficulty lives: tidy inputs are exactly where models already do well.

## Part 3 · The check

Run this on the whole task before submission, and on anything drafted here before it is used.

1. Read every sentence aloud. Any that would not survive being sent to a colleague is rewritten or cut.
2. Search the prose for the strike list above. Each hit is either removed or replaced with the plain word.
3. Check that at least one sentence per message carries a specific: a name, a date, a system, a number.
4. Open each workbook and look at structure, formatting, file state, data and properties against the lists above.
5. Set file properties to something a real file would have, and save the file so the timestamps are not identical.
6. Check that every number that should be unround is unround, and every date series has at least one irregularity a real pull would have.
7. Read the criteria as a set: do they vary in shape, and do they name tabs and columns rather than "the output"?
8. Ask the final question: if this landed in an inbox, would anyone think twice about where it came from?

Each failed item is a finding, named with the surface it is on and the exact change.
