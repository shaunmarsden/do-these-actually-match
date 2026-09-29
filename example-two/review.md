# Review: Fernbank Runners Reconciliation

I checked the [output](output.md) against the harder traps I built into [the membership spreadsheet](membership-spreadsheet.md) and [the payment export](payment-processor-export.md).

## Did It Catch the Traps?

The duplicate-line trap, Marcus Oduya's two payments. The output saw both payment rows as one member before comparing. It didn't treat the second payment as an extra unmatched row or a second disagreement. It also raised the duplicate as a separate, minor follow-up, without letting it distort the main comparison.

The name trap, J. Whitcombe and Jamie Whitcombe. The names look like a match, but the emails don't back it up. The output refused to decide either way. It labelled the pair "could not confidently match" rather than guessing yes or no to make the numbers tidier.

The status conflict, Tomasz Kowalski. He's lapsed on one side and has a live payment on the other. The output reported this as a real disagreement and didn't guess which record is right.

The capture-gap trap. The two records were taken three weeks apart. The output says so plainly in its opening section and comes back to it when discussing Helena Byrne, rather than mentioning it once and then ignoring it.

The new-name trap, Helena Byrne. She's in the payments only. The output offers the likely reading, "joined since the spreadsheet was last updated", but says clearly that it isn't confirmed, rather than stating it as settled.

## What Worked

It treated the duplicate row and the unclear name as two different problems. It didn't fold them into one vague "these do not line up" comment.

Every suggested follow-up names a specific action and a specific person to check with, rather than a general "investigate discrepancies" note.

## What Needed Checking

This evidence alone can't settle whether J. Whitcombe and Jamie Whitcombe are the same person. A real version of this comparison would need to ask the club secretary. The output leaves that as a step for a person, which is right.

This is still one fictional run. A real membership and payment reconciliation will probably have more than one unclear name at once. This example has only one, to keep it readable.

## Next Test

Run a case with more than one unclear name at once. Include a three-way split, where one person appears under two different names across three or more rows. That checks whether the method still keeps each unclear match separate once there's more than one.
