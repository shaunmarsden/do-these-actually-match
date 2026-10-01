# Review: Kestrel Hardware Stock Reconciliation

I checked the [output](output.md) against the traps I built into [the physical count](physical-count.md) and [the POS export](pos-system-export.md).

## Did It Catch the Traps?

The units trap, Wood Screws 40mm. At a glance, 3 boxes of 200 against 600 single screws looks like a big disagreement. The output converted the units before comparing and found they agree.

The formatting trap, Masonry Drill Bit 8mm. 12 and 12.0 are the same value. The output didn't report this as a mismatch, and didn't quietly ignore it either. It named it as a presentation difference it had resolved.

The new-delivery trap, Cordless Screwdriver Bit Set. This is in the physical count only, because nobody had logged it into the till yet. The output reported it as "only in one record," not as a conflict. It also explained why, rather than treating the till as simply wrong.

The incomplete-count trap, Fence Post Caps. This is in the POS export only, because the counter never reached that shelf. The output didn't suggest the stock is zero or missing. It said the count was incomplete for this item.

The two real conflicts, Galvanised Hinges 75mm and Paint Brushes 2 inch. These are real gaps in opposite directions, with no units or formatting to explain them. The output reported both plainly, gave the size and direction of each gap, and didn't guess a cause for either.

## What Worked

It sorted all five traps correctly. It didn't lump any of them into one general "these do not match" statement.

It never says which record is right, only that there's a gap and how big it is.

Its "what this comparison cannot tell you" section admits it doesn't know why the two conflicts exist.

## What Needed Checking

The suggested recount for the two conflicting items is a sensible next step. It's offered as a suggestion, not an instruction, so a person still decides whether to act on it.

This is one fictional run. I haven't tested it on a real reconciliation, and a real one will probably have messier names and codes than this deliberately clean example.

## Next Test

Try a harder case. Give it names or codes that don't match between the two records, and a real gap between when each was taken. Add a duplicated line in one source that has to be sorted out before you can compare. [The second worked example](../example-two/) is that case.
