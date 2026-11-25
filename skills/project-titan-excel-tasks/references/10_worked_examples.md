# 10 · Worked examples

Two tasks, worked end to end. The first is the guide's own build-from-scratch example, with the criterion walkthrough and the weak-and-strong pairs that go with it. The second is a real fix-a-messy-workbook task taken through screening.

---

# A · Build from scratch · Pro forma Series A ownership model

## The prompt

> "Attaching my emails with the founders on deal context. The register of members has the current shareholdings. The convertible loan note register lists the notes. Can you build the pro forma Series A ownership model?"

Files: two founder emails, the register of members, the convertible loan note (CLN) register.

## The trap, in the files

| Option pool, per founder email | 11,764 |
| Options granted, per register | 10,997 |
| Difference | 767 |

The answer: the 767 is the existing unallocated pool — options already in the plan but not yet granted.

## What happened

The reviewed outputs treated the 767 as an unexplained variance, so they created too many new options for the post-round pool. That threw off the share counts and, in some outputs, the price per share.

## Why it works

The prompt is short and sounds real. It does not mention the gap; finding it is part of the job. Any experienced VC analyst would read the gap the same way, so the failure is clear-cut.

A gap between two sources is not always an unallocated pool. Here the founder emails support that reading. Without that context, the prompt or the files would need to say how to treat it.

## Nine things you might check, and how each is settled

| # | Criterion | What decides it | Tag |
| 1 | Each shareholder's pre-round shares match the register of members. | Q1: the register fixes it. | Outcome |
| 2 | The Series A share price is £80.46. | Q1: the inputs fix it. | Outcome |
| 3 | The unallocated pool equals the pool in the founder email less the options granted in the register. | Q1: the inputs fix it. It is a calculated value, so it is a Method criterion. | Outcome |
| 4 | Cap Table shows each funding round in its own column. | Q1 no, Q2 no, Q3 no. Q4: experts expect that layout. | Quality |
| 5 | The reply says how the 767-option gap between the email and the register was treated. | Q4: experts expect the gap to be explained. No file fixes the wording. | Quality |
| 6 | Negative figures are in parentheses. | Q3: a banking convention, and the prompt sets that audience. | Quality · Domain Specific |
| 7 | Every key output is a live formula. | Q2: checked on every task already. | Do not write |
| 8 | There are no merged cells in the cap table. | Q2: checked on every task already. | Do not write |
| 9 | The Summary uses my firm's navy header colour. | Fails all four. It is a preference. | Do not write |

Row 6 only earns a Domain Specific tag because the prompt names the audience. If the prompt itself asked for parentheses, it would be an Outcome criterion with no tag.

## Eight weak criteria and their strong versions

**1 · Vague.** Weak: *The model builds an accurate cap table.* Strong: *Each shareholder's pre-round shares match the register of members.* Nobody can mark "accurate" yes or no.

**2 · No number.** Weak: *The Series A share price is approximately correct.* Strong: *The Series A share price is £80.46.*

**3 · Describes the mistake.** Weak: *The model flags the 767 as a variance.* Strong: *The cap table shows the existing unallocated pool of 767 options on its own line.* A workbook that ignores the 767 completely would pass the weak version.

**4 · Demands a method.** Weak: *Uses SUMIFS to pull each holder's shares from the register.* Strong: *Each holder's shares on Cap Table match the Register tab.* A correct workbook built with XLOOKUP fails the weak version.

**5 · Cell reference.** Weak: *Cap Table!H14 shows 100%.* Strong: *Total ownership is the sum of the holders' percentages.* The weak version breaks when a row is inserted, and a typed 100% passes it.

**6 · Several checks in one.** Weak: *The cap table is correct, formatted well and the summary is clear.* Strong: three criteria — the share counts match the register, each funding round has its own column, and the Summary shows the Series A price. When the weak one fails, nobody knows which part went wrong.

**7 · Already covered.** Weak: *Formulas are live and there are no merged cells.* Strong: leave it out. It is checked on every workbook.

**8 · Hedged and wordy.** Weak: *The response should clearly and appropriately explain the treatment of any discrepancies identified.* Strong: *The reply says how the 767-option gap between the email and the register was treated.*

## The whole set

A weak rubric: five or six long criteria, each bundling several checks; mostly formatting and headline numbers; names the mistakes it saw, not the right answers; restates what every workbook is checked for anyway; fails any workbook that took a different, valid route.

A strong rubric: at least ten short criteria, one check each; covers every ask, every real failure and the field's standard practice; describes what the right workbook has; names the source and the number where inputs could conflict; passes any workbook you would send as it is.

---

# B · Fix a messy workbook · Stellantis credit model repair

A real task, taken through screening. It shows what a fix task looks like at full size, and where screening pushed back.

## The scenario

A €2.4bn European investment-grade corporate bond fund holds €75m nominal of Stellantis senior euro notes across three EMTN lines. The fund is IG-only. Stellantis was downgraded by both agencies in February 2026 after a €22.2bn strategic reset and now sits at the bottom investment-grade notch with a negative outlook at S&P. House rules cap exposure to such an issuer at 2% of NAV, with a second sub-limit on long-dated exposure. The autos analyst left halfway through rolling the model from H1 to Q3 2026. The PM has an investment committee on 26 November 2026 and needs the workbook repaired and a sized hold, add or reduce call.

Who needs it, what exists, what changed, what they expect back — the scenario does all four in a paragraph.

## The prompt

One message, in the PM's voice, no method given:

> Can you take over Stellantis from Luca? His model (stellantis_credit_model.xlsx) is half rolled from H1 to Q3 and I don't trust the Capitalization tab. Before IC on 26 November I need the workbook fixed and tied to the filings in the folder, keeping his layout, with a Change Log tab listing the material corrections (related cells can be grouped as a range), the affected cells or ranges, and the supporting source or rationale; and a note of no more than 500 words on whether we hold, add or reduce, with the amount by line and the trade dates. We hold €75m nominal: €30m of the 0.750% notes due Q1 2029 (XS2356040357), €25m of the 4.500% notes due January 2033 (XS3405545230) and €20m of the 5.100% notes due January 2037 (XS3405546121). House rules, since we're IG-only: both Moody's and S&P have to be at Baa3/BBB- or better, nominal exposure to any issuer at the bottom notch with a negative outlook from either agency is capped at 2% of NAV (fund is €2.4bn), and no more than 1.25% of NAV in any one issuer beyond five years' residual maturity, and any excess has to be sold, trade date, within 30 calendar days of the IC decision. The annual report, fact sheet, 2026 releases and interim reports, the hybrid and bond documents, the ratings page and the peer reports are all in the folder. Risk will reconcile the workbook to the Q3 release, so flag anything you can't tie rather than plugging it.

What it does right: names the deliverables and their limits, gives every house rule the answer turns on, names the audience and the deadline, says what must not change ("keeping his layout"), and says what to do when something cannot be tied ("flag it rather than plugging it") — which is a choice two professionals could make differently. It never says which tabs are broken, never names a defect, and never prescribes a method.

## Two prompt corrections screening forced

**Bond terms have to match the pack.** The prompt originally gave exact days — "0.750% notes due 18 January 2029" — and a 5.125% coupon. No such day appears in the source documents, and the pack gives the 2037 coupon as 5.1%. The fix was to drop to the precision the filings actually disclose: quarter for the older line, month for the 2026 issues, and 5.100%. A prompt figure that cannot be verified in the pack is unfair, because the solver cannot tell whether their own reading is wrong.

**A constraint built into the workbook has to be in the prompt.** The 1.25%-of-NAV sub-limit on exposure beyond five years was added to the model after the prompt was written. Without it in the prompt, the task is unsolvable: the sub-limit drives part of the required sale. Every rule the answer turns on lives in the prompt.

## The edit range

The allowed range is the whole of all four sheets, plus permission to insert a sheet:

> Capitalization!A1:Z200, Financial Overview!A1:Z400, Relative Value!A1:M110, Risks and Mitigants!A1:K70

Screening's first version listed the defect cells. That hands over the defect map — the solver would know exactly where to look. Two of the defects are also *missing rows*, which cannot be expressed as cells at all. On a fix task the allowed range is broad by design; the scope criteria do the work of catching edits that went too far.

## Keeping the answer out of the solver's copy

The repair copy and the golden are built from one generator with a `bad` flag, so they stay structurally identical and the defect map's cell references hold. The rules that keep the solver's copy honest:

- September-2026 tie-out cells are left **empty, not wrong**, so no correct figure sits beside the defect it would expose.
- Notes explaining a correct treatment are suppressed in the repair copy.
- No Change Log, no checks block, no open-items list, no cell comments, no defined names in the solver's copy. An earlier build had an open-items list and a holiday table; both were removed as hints.
- Document properties are cleared. The generator had left `creator: openpyxl` in the file — a fingerprint that says the workbook was machine-built.

## No invented data

No price, yield, spread or rating that is not in the pack. The pack contains no prices at all, which is why the relative-value work runs on fundamentals rather than on spreads. Maturities and coupons appear exactly as disclosed and never to a precision the filings do not give.

This is also why two proposed complexity additions were held: bond prices need a real price source, and a change-of-control put does not exist in either filing, so adding one would fabricate a term.

## Conflicts flagged, not plugged

Two genuine conflicts sit inside the source pack, and the task is built around them rather than around hiding them.

The fact sheet and the Q3 interim give different Q3 2025 operating income — a €3,246m difference moving between quarters, while every AOI figure agrees on both bases. The model uses the interim basis, shows the fact-sheet split on a memo row, and flags it. Either basis is acceptable if stated.

The industrial and financial-services split of committed lines is not disclosed. The model builds industrial liquidity bottom-up, compares with the reported figure, and identifies the residual rather than forcing it to zero.

The prompt's closing line — flag anything you can't tie rather than plugging it — is what makes both of these gradeable.

## The defect chain

Twenty-four defect groups, and the ones that carry the task are chained rather than independent:

- Stale ratings make the bottom-notch test return No, so the concentration limits never engage and the workbook concludes no action is required. Everything downstream rests on this.
- The cap test demands a negative outlook at *both* agencies rather than either. The row is labelled neutrally, so the defect is the rule itself, not a mismatched label.
- The long-dated horizon is set at ten years instead of five, so the sub-limit never bites even once the ratings are fixed.
- The note register is wrong in four directions at once — stale, overstated by repaid notes and a sterling-rate error, understated by missing issues — so five corrections are needed before it reproduces the reported figure.
- Hybrids added to debt break the projected balance sheet by €2,218m. That is a visible symptom of one underlying classification error, not a separate defect.

That last point is the double-counting rule from reference 05 in its natural habitat: one classification error, one criterion, several symptoms.

## The reconciliation spine

Every figure the task rests on was cross-footed from the filings before any criterion was written. The register roll reproduces €22,045.4m against €22,045m reported — a €0.4m residue from five-decimal translation, inside a ±€1m tolerance that was agreed, not defaulted to. The mandate arithmetic is equally explicit: a €48m issuer cap against €75m held means at least €27m sold, and a €30m sub-limit against €45m held beyond five years means at least €15m of that sale comes from the two long lines.

Dates get the same treatment. Thirty days from 26 November is Saturday 26 December; TARGET is closed on 25 and 26 December, so Thursday 24 December is the last valid trade date and 23 December is the recommended one on liquidity. Settlement is T+2 and the window is measured on trade date, so settling on 29 December is compliant. The criterion accepts 24 December or earlier — a feasible set, not one date.

## Where screening pushed back, and what it teaches

| Screening item | The lesson |
| Edit range listed the defect cells | The allowed range must not double as a defect map |
| Trade-date reasoning and settlement convention not shown | A date criterion needs the calendar and the convention behind it, and an accepted range |
| Bond coupons, ISINs and dates could not be verified in the pack | Never state in the prompt a figure the files do not carry |
| Unreconciled items | Flagging is enough where disclosure genuinely does not exist; say so explicitly |
| Platform field said three tabs; the workbook has four | Every platform field has to match the file |
| Sale allocation acceptance | Where several allocations are defensible, the criterion defines the feasible set |
| AI-generated content | Figures traced to filings, but labels, notes and the supporting write-up were model-written; they were compressed to terse working notes and generator fingerprints cleared. If the requirement is read literally, a person rewrites the note text — structure, formulas and figures do not change |

## Validation before shipping

The gates this task had to pass, all of which generalise to any fix task:

- Zero formula errors and zero circular references in both files.
- Every reconciliation check inside its agreed tolerance in the golden.
- The projected balance sheet check at approximately zero in every column.
- Every defect-map cell differing between the repair copy and the golden.
- A leakage sweep: nothing in the solver's copy points at a defect.
- A scenario-independence test: perturb a downside input and confirm the base-case outputs do not move.
- Never hand-edit the workbook when it is generator-built; it breaks the defect map's cell references.
