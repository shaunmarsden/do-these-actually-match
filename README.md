# Do These Actually Match?

<p>
  <img alt="Status: Working tool" src="https://img.shields.io/badge/status-working%20tool-2563eb">
  <a href="LICENSE"><img alt="Licence: MIT" src="https://img.shields.io/badge/licence-MIT-lightgrey"></a>
</p>

Compare two records of the same thing, kept separately, and see only where they really disagree. You don't get a full side-by-side, and it doesn't pick whichever source is easier.

## Why

Two records of the same thing drift apart more often than anyone checks: a hand count against a system export, one team's spreadsheet against another's, a membership list against who has paid.

Checking them by eye goes wrong in two ways. You miss a real disagreement hidden among near-identical rows. Or you see one where the same fact is only written two ways: a unit conversion, a rounding difference, a date format.

This takes a rule from [Practical AI Sales Workflows](https://github.com/shaunmarsden/practical-ai-sales-workflows) and uses it outside sales. When two approved sources disagree, [the method](https://github.com/shaunmarsden/practical-ai-sales-workflows/blob/main/METHODOLOGY.md) says show the disagreement rather than quietly pick one. The [approval-gated sales copilot](https://github.com/shaunmarsden/practical-ai-sales-workflows/blob/main/guides/build-an-approval-gated-sales-copilot.md) gives it its own label, Conflicting. Lumping it in with Unknown would hide that two sources disagree, rather than one saying nothing.

This tool makes the same call for a more common case: two whole records that should match.

[![Four boxes showing the possible outcomes of comparing two records: Agrees, Genuinely conflicting, Only in one record, and Could not confidently match.](assets/diagrams/01-do-these-actually-match.svg)](SKILL.md)

## Use It

Copy [SKILL.md](SKILL.md), paste it into your AI tool (ChatGPT, Claude, Gemini or similar), then paste in both records. It sorts what it finds into four groups:

- Agrees: the same fact, once differences in how it's written are cleared up
- Genuinely conflicting: a real disagreement, with no guess at which source is right
- Only in one record: in one source and not the other, without assuming that's an error
- Could not confidently match: a likely pairing the evidence can't confirm, left open rather than forced either way

<details>
<summary><strong>See what it produces</strong></summary>

1. What each record covers and when it was taken, including any real gap between the two
2. How it matched rows across the two records, and which it couldn't match at all
3. Every real disagreement, stated plainly, with no guess at a cause
4. Every row that's in only one record, kept apart from the disagreements
5. Differences in how things are written, resolved and named, not dropped or wrongly reported as mismatches
6. Suggested next steps for a person to approve, never a decision already made

</details>

[The worked example](example/) is a fictional hardware shop's stock count against its till export. It has a unit conversion, a formatting difference, a delivery not yet logged and an incomplete count, all at once. [The second worked example](example-two/) is harder. It has a name that looks like a match but can't be confirmed, a duplicated payment row, and a real conflict over a member's status.

Use [the blank template](templates/reconciliation-template.md) for your own comparison, and [the review checklist](checks/checklist.md) before you act on anything it finds.

You don't need to install anything, set up a project or write code to try it.

## Before You Use It

This reports where two records agree, disagree or couldn't be matched. It doesn't decide which record is right, or what to do about a disagreement. That call, and any fix, is yours.

## Not the Same As

- [Claims vs Evidence Checker](https://github.com/shaunmarsden/claims-vs-evidence-checker) checks whether one document's claims are backed by evidence in that same document. This tool needs two separate records to start with.
- [Is This Really a Pattern?](https://github.com/shaunmarsden/is-this-really-a-pattern) looks for a real repeated cause across many similar entries in one log. This tool compares two records with each other, not the entries within one.

## Feedback

Used it on a real reconciliation? [Start a discussion](https://github.com/shaunmarsden/do-these-actually-match/discussions) if a match or mismatch didn't fit.

## Part of a Family

This is one of a family of free tools that take patterns from [practical-ai-sales-workflows](https://github.com/shaunmarsden/practical-ai-sales-workflows) beyond sales. [sibling-projects](https://github.com/shaunmarsden/sibling-projects) lists the rest. Not sure which one fits? Try [the interactive picker](https://shaunmarsden.github.io/sibling-projects/), which shows clickable cards, or paste a description into an AI chat with [the router](https://github.com/shaunmarsden/sibling-projects/blob/main/ROUTER.md).
