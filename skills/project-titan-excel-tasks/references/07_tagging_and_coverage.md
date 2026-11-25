# 07 · Tagging and coverage

## The two tags

Every criterion is tagged Outcome or Quality. A third tag, Domain Specific, is added to Quality criteria where a field convention applies. Every criterion counts the same, so there is no importance level to choose.

**Outcome — the files fix it.** The prompt, the input files or the template settle the answer: values, what is included, the method asked for, scope, planted errors.
Example: *The Series A share price is £80.46.*

**Quality — experts expect it.** A judgement call: the files do not settle the answer, but experts in the field would agree on structure, flags, assumptions, conventions.
Example: *Cap Table shows each funding round in its own column.*

**Domain Specific — a field convention.** An extra tag, on Quality criteria only, for a convention of the field, used only when the prompt sets that audience.
Example: *Negatives are in parentheses* in a model for a bank.

An AI assigns each criterion's area — the four categories in reference 05 — after submission. The expert tags the type and the domain tag only.

## The four questions, in order

**1. Can you name the prompt line, input file or template that fixes it?**
Yes → **Outcome.** Cite the source. No Domain Specific tag. If it is a calculated value, it also gets a Method criterion (rule 6.9).
No ↓

**2. Is it on the list of things checked on every task?**
Yes → **Already covered: do not write it.**
No ↓

**3. Is it a convention every expert in this field expects, and is the workbook for that audience?**
Yes → **Quality, tagged Domain Specific.**
No ↓

**4. Would experts in this field agree the prompt, or its purpose, calls for it?**
Yes → **Quality.**
No → **Do not write it.** A personal preference, or analysis nobody asked for.

Question one does most of the work. If the prompt or files already fix it, it is an Outcome criterion even when it feels like a judgement call. Tagging it Quality hides that it has a right answer.

## The universal list: already covered, do not write

Checked on every task by the shared automated and Excel-testing layers:

- Key outputs are live formulas, not typed values.
- No assumptions or names typed into formulas, and formulas consistent along a row.
- Checks that can actually fail.
- No merged cells inside tables, and units stated.
- Nothing shows ####, nothing is cut off, formats are consistent.
- The file opens cleanly, with no error values, circular references, new external links or broken names.

If one of these is broken in a model output, flag it on the platform so the shared check gets tuned. It does not become a criterion in this rubric. In this copilot's output it is an escalation line, never a MISSING entry.

## The coverage matrix

Core (●) on almost every task of that type; Light (○) where the task makes it material; not used (–).

| Area | Build | Edit | Fix | Type |
| **Correctness** | | | | |
| Completeness — every item asked for, filled through | ● | ● | ● | Outcome |
| Values — within tolerance | ● | ● | ● | Outcome |
| Live formulas — key outputs trace back to the inputs | ● | ● | ● | Universal, do not write |
| Input handling — hidden rows, colour meaning, conflicts | ● | ● | ● | Outcome |
| Reconciliation — totals tie, balance sheet balances | ● | ● | ● | Outcome |
| Method — method asked for, how values are derived | ● | ○ | ○ | Outcome or Quality |
| **Craft** | | | | |
| Formula hygiene — no typed assumptions or names in formulas | ● | ● | ● | Universal, do not write |
| Structure and flow — inputs, drivers, outputs kept apart | ● | ○ | ○ | Quality |
| Working checks — checks that could actually fail | ○ | ○ | ● | Universal, do not write |
| Editability — no merged cells, units in headers | ● | ○ | ○ | Universal, do not write |
| Presentation — formats consistent, nothing cut off | ○ | ○ | – | Universal, plus Quality for field conventions |
| Features, if asked — charts, pivots, rules: native, working | ○ | ○ | – | Outcome |
| **Scope** | | | | |
| Change is targeted — no edits outside the allowed range | – | ● | ● | Outcome |
| Edits disclosed — reply lists every range edited | – | ● | ● | Quality |
| Change propagates — every dependent output updates | – | ● | ● | Outcome |
| Planted errors — each fixed at its source | – | – | ● | Outcome |
| Over-engineering — nothing the recipient must delete | ○ | ○ | ○ | Quality |
| Prohibitions — correct cells and items left alone | ○ | ● | ● | Outcome or Quality |
| **Judgement and communication** | | | | |
| Judgement — errors flagged, assumptions stated | ● | ○ | ● | Quality |
| Domain knowledge — field conventions, technical facts | ○ | ○ | ○ | Quality, tagged Domain Specific |
| Communication — reply states the answer, matches the file | ● | ● | ● | Quality |

Write at least one criterion for every Core area of the task's type. Skip the universal rows: the shared checks cover them and the coverage check reads their tags.

## Using the matrix in a coverage check

1. Identify the task type, from the prompt and the files, not from what the expert called it.
2. List the Core areas for that type.
3. Map each of the expert's criteria to an area. A criterion that maps to no area is either a universal row or something nobody asked for.
4. Any Core area with no criterion is a MISSING entry.
5. Any area with four or more criteria is worth a second look for double-counting.
6. For edit and fix tasks, confirm the three standing criteria in reference 06 are there and that the allowed range is named by sheet and row or column labels, not cell addresses.
