# Reconciliation: Membership Spreadsheet vs Payment Processor Export

> This is a fictional worked output, produced from [membership-spreadsheet.md](membership-spreadsheet.md) and [payment-processor-export.md](payment-processor-export.md). No membership record has actually been changed.

## What Each Record Represents, and As Of When

Membership Spreadsheet: the club secretary's record of who is an active or lapsed member, last updated three weeks ago. Payment Processor Export: everyone who has made a payment, exported today. The two records were captured three weeks apart. Any member who joined, lapsed, or renewed in that window could show up as a difference here without either record being wrong.

## Matching Notes

Three rows matched directly on name and email. One pairing looks plausible by name alone, Marcus Oduya and Jamie Whitcombe, but the email addresses do not agree closely enough to treat as confirmed for Whitcombe; that one is reported as a possible match, not a confirmed one. The payment export contains two separate rows for Marcus Oduya with identical name and email; these were treated as one matched member with two payments this cycle, not two different people.

## Summary

| Category | Count |
| --- | --- |
| Agrees | 2 |
| Genuinely conflicting | 1 |
| Only in Payment Processor Export | 1 |
| Could not confidently match | 1 |

## Genuinely Conflicting

- **Tomasz Kowalski.** Membership spreadsheet: Lapsed. Payment processor: a payment made today. These directly disagree about current status. This could mean the spreadsheet is out of date, or that Tomasz has just rejoined; the evidence here does not say which.

## Could Not Confidently Match

- **J. Whitcombe (spreadsheet) and Jamie Whitcombe (payment).** The names are similar enough to plausibly be the same person, but the email addresses share no common part (j.whitcombe@fernmail.example versus jamie.w.runs@fernmail.example) and nothing else in either record confirms they are the same. Treating this as a match, or as two unrelated people, would both be guesses. A person should confirm this directly before either record is corrected.

## Only in One Record

- **Helena Byrne.** Only in the payment processor export; no corresponding row in the membership spreadsheet. Given the three-week gap between the two records, a new member joining in that window is a plausible explanation, but this is not confirmed by anything in either record and should not be stated as fact.

## Agrees

- **Priya Nazari.** Matches on name and email; Active status is consistent with a payment having been made.
- **Marcus Oduya.** Matches on name and email; Active status is consistent with payment activity. Two separate payment rows were found for this one member; that is noted below, not treated as a second discrepancy.

## Presentation Differences Resolved, Not Reported as Mismatches

None in this comparison. The one unusual detail, Marcus Oduya's duplicated payment row, is not a disagreement between the two records; it is an internal duplicate within the payment export, resolved before comparison rather than reported as a mismatch.

## Suggested Follow-Up for Human Approval

- Ask Tomasz Kowalski directly whether he intends to rejoin, and update whichever record is out of date once that is confirmed.
- Confirm with the club secretary whether Jamie Whitcombe is the same person as J. Whitcombe before changing either record.
- Confirm whether Helena Byrne is a new member and, if so, add her to the membership spreadsheet.
- Check why Marcus Oduya has two payments this cycle; that duplication was set aside for this comparison but may be worth its own review.

## What This Comparison Cannot Tell You

It cannot confirm whether Jamie Whitcombe and J. Whitcombe are the same person, why Tomasz Kowalski's status disagrees between the two records, why Marcus Oduya was charged twice, or whether Helena Byrne is a genuinely new member rather than a data-entry issue elsewhere. The three-week gap between when each record was captured means some of these differences may simply reflect real change over that time, not an error in either record.
