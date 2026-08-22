---
name: do-these-actually-match
description: Compare two independently-kept records of the same thing and surface only where they genuinely disagree, instead of a full side-by-side or picking whichever source seems more convenient. Use when two systems, people, or documents are each supposed to reflect the same reality, a count, a status, a set of dates, and you need to know where they have actually diverged. Do not use this to judge whether one document's own claims are backed by evidence; use claims-vs-evidence-checker for that. Do not use this to find a repeated cause across many similar entries in one log; use is-this-really-a-pattern for that. This is for two records that are meant to agree with each other.
---

# Do These Actually Match?

You do not need to install anything to try this once. The lines between the dashes at the very top are just this file's label; leave them in. On GitHub, copy this using the **Raw** button near the top of the page rather than selecting the rendered text, so the tables and links below paste in cleanly. Send the whole file as your first message in any AI chat tool, then paste in both records.

Two records that are each supposed to reflect the same reality drift apart more often than anyone checks. Comparing them by eye either misses the real disagreements in a wall of near-identical rows, or invents disagreements that are really just two different ways of writing the same fact. This finds what genuinely disagrees, and states plainly what could not be matched at all, rather than forcing every row to line up.

## Gather the Inputs

- Both records, each from its own independent source
- What each record is actually supposed to represent, and as of when
- Whatever identifier, name, or description links a row in one record to its counterpart in the other, if that is not already obvious

## Match Before You Compare

Decide what counts as the same thing across the two records before comparing any values. A different identifier does not automatically mean a different thing, and a matching identifier does not automatically mean the same thing either, two systems can reuse a code for different items over time. State plainly which rows could not be confidently matched to anything in the other record, rather than guessing a partner for them to force the totals to line up.

## Tell a Real Disagreement From a Presentation Difference

The same real fact can be written two different ways: a unit conversion, a rounding difference, a date format, a status word that means the same thing in both systems. Check for this before reporting anything as a mismatch. A resolved presentation difference is not a disagreement and should not be reported as one.

## Classify Every Comparison

Assign every row exactly one label:

- **Agrees:** the same fact, once presentation differences are resolved
- **Genuinely conflicting:** the same thing, but the two records disagree on a fact about it
- **Only in one record:** present in one source and not found in the other at all
- **Could not confidently match:** a row that might correspond to something in the other record, but the evidence given is not strong enough to say so; do not force this into a match or an "only in one record" just to remove the ambiguity

Do not blend these categories, and do not let a large "agrees" count bury a small but real "genuinely conflicting" one.

## Apply the Guardrails

- Never report a mismatch that turns out to be a presentation or format difference once resolved
- Never force a match between two rows just to make the totals come out even
- Never silently drop a row that only appears in one record; report it as its own category, not as an error in the other
- Never state which source is correct; only that they disagree, and by how much
- Never invent a reason for a genuine disagreement that is not actually in the evidence

## Stop When the Task Is Unsafe

Do not produce a comparison when:

- The two records do not actually describe the same thing or the same period, comparing them would not mean anything
- Most rows cannot be matched with any confidence, meaning any resulting comparison would be built on guessed pairings
- The gap between when each record was captured is large enough that an apparent disagreement more plausibly reflects real change between the two dates than an actual error, and the evidence given cannot tell the difference

Explain the limitation and name the minimum missing detail rather than producing a confident-looking comparison anyway.

## Require Human Review

This reports where two records agree, disagree, or could not be matched. It does not decide which source is correct, or what to do about a genuine disagreement. A person makes that call and carries out any resulting correction.

For a fictional worked example, a shop's physical stock count against its point-of-sale system, read [the worked example](example/). For a harder case, mismatched identifiers, a stale count, and a duplicated line that has to be resolved before any comparison is possible, read [the second worked example](example-two/). Use [the blank template](templates/reconciliation-template.md) for your own comparison, and [the review checklist](checks/checklist.md) before acting on any finding.
