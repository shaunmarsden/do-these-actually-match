# Review: Fernbank Runners Reconciliation

This checks the [output](output.md) against the harder traps built into [the membership spreadsheet](membership-spreadsheet.md) and [the payment export](payment-processor-export.md).

## Did It Catch the Traps?

- **The duplicate-line trap (Marcus Oduya's two payments).** The output correctly recognised both payment rows as one member before comparing, rather than treating the second payment as an unmatched extra row or a second discrepancy. It also surfaced the duplication itself as a separate, minor follow-up point, without letting it distort the main comparison.
- **The mismatched-identifier trap (J. Whitcombe versus Jamie Whitcombe).** A plausible name match with no supporting email match. The output correctly refused to resolve this either way, labelling it "could not confidently match" rather than guessing yes or no to make the numbers tidier.
- **The genuine status conflict (Tomasz Kowalski).** Lapsed on one side, a live payment on the other. The output reported this as a real disagreement and correctly declined to guess which record is right.
- **The stale-capture-gap trap.** The three-week difference between when each record was taken is stated plainly in the opening section and referenced again when discussing Helena Byrne, rather than being mentioned once and then ignored for the rest of the analysis.
- **The new-name trap (Helena Byrne).** Present in payments only. The output offers the plausible "joined since the spreadsheet was last updated" reading but is explicit that this is not confirmed, rather than stating it as settled.

## What Worked

- The duplicate row and the ambiguous identifier were handled as two clearly different problems, not folded into one vague "these do not line up" comment.
- Every suggested follow-up names a specific action and a specific person to check with, rather than a generic "investigate discrepancies" note.

## What Needed Checking

- Whether J. Whitcombe and Jamie Whitcombe are the same person genuinely cannot be settled from this evidence alone; a real version of this comparison would need to ask the club secretary directly, which the output correctly leaves as a human step.
- This remains one fictional run. A real membership and payment reconciliation is likely to have more than one ambiguous identifier at once, and this example deliberately isolates just one to keep the case readable.

## Next Test

Run a case with more than one ambiguous identifier at once, and a genuine three-way split where one person appears under two different names across three or more source rows, to check whether the method still separates each ambiguity cleanly rather than collapsing them together once there is more than one at a time.
