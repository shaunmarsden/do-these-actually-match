# Review: Kestrel Hardware Stock Reconciliation

This checks the [output](output.md) against the deliberate traps built into [the physical count](physical-count.md) and [the POS export](pos-system-export.md).

## Did It Catch the Traps?

- **The unit-of-measure trap (Wood Screws 40mm).** 3 boxes of 200 versus 600 individual screws looks like a huge disagreement at a glance. The output correctly converted units before comparing and resolved it as agreeing, not as a conflict.
- **The formatting trap (Masonry Drill Bit 8mm).** 12 versus 12.0 is the same value. The output correctly resolved this without reporting it as a mismatch, and without silently ignoring it either; it is named explicitly as a resolved presentation difference.
- **The new-delivery trap (Cordless Screwdriver Bit Set).** Present in the physical count only, because it had not yet been logged into the till. The output correctly reported this as "only in one record," not as a conflict, and correctly explained why rather than treating the till as simply wrong.
- **The incomplete-count trap (Fence Post Caps).** Present in the POS export only, because the counter never reached that shelf. The output correctly avoided implying the physical stock is actually zero or missing, and named the count itself as incomplete for this item.
- **The two genuine conflicts (Galvanised Hinges 75mm, Paint Brushes 2 inch).** Real gaps in opposite directions, with no unit or formatting explanation available. The output reported both plainly, stated the size and direction of each gap, and did not guess a cause for either.

## What Worked

- Every one of the five traps was classified correctly and none were merged into a single generic "these do not match" statement.
- The output never states which record is correct, only that a gap exists and how large it is.
- The "what this comparison cannot tell you" section is honest about not knowing why the two genuine conflicts exist.

## What Needed Checking

- The suggested recount for the two genuinely conflicting items is a sensible next step, but it is presented as a suggestion, not an instruction; a person still decides whether to act on it.
- This is one fictional run. It has not been tested against a real reconciliation, and a real one is likely to have messier identifiers than this deliberately clean example.

## Next Test

Use a harder case with mismatched identifiers between the two records, a meaningful gap between when each record was captured, and a duplicated line in one source that has to be resolved before any comparison is possible. See [the second worked example](../example-two/) for that case.
