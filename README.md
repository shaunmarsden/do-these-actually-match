# Do These Actually Match?

<p>
  <img alt="Status: Working tool" src="https://img.shields.io/badge/status-working%20tool-2563eb">
  <a href="LICENSE"><img alt="Licence: MIT" src="https://img.shields.io/badge/licence-MIT-lightgrey"></a>
</p>

Compare two independently-kept records of the same thing and surface only where they genuinely disagree, instead of a full side-by-side or picking whichever source seems more convenient.

## Why

Two records that are each supposed to reflect the same reality drift apart more often than anyone checks: a manual count against a system export, one team's spreadsheet against another's, a membership list against who has actually paid. Eyeballing them either misses a real disagreement buried in a wall of near-identical rows, or invents one out of two different ways of writing the same fact, a unit conversion, a rounding difference, a date format.

This generalises a rule that already sits at the centre of [Practical AI Sales Workflows](https://github.com/shaunmarsden/practical-ai-sales-workflows): when two approved sources disagree, [the method](https://github.com/shaunmarsden/practical-ai-sales-workflows/blob/main/METHODOLOGY.md) says show the disagreement rather than quietly picking one, and the [approval-gated sales copilot](https://github.com/shaunmarsden/practical-ai-sales-workflows/blob/main/guides/build-an-approval-gated-sales-copilot.md) gives that idea its own label, Conflicting, precisely because folding it into a generic Unknown loses the fact that two sources actively disagree rather than one being silent. This tool is that same judgement call, pulled out on its own for the much more common case of two whole records that are supposed to match.

[![Four boxes showing the possible outcomes of comparing two records: Agrees, Genuinely conflicting, Only in one record, and Could not confidently match.](assets/diagrams/01-do-these-actually-match.svg)](SKILL.md)

## Use It

Copy [SKILL.md](SKILL.md) and paste it into your AI tool (ChatGPT, Claude, Gemini, or similar), then paste in both records. It produces:

- **Agrees**, the same fact once presentation differences are resolved
- **Genuinely conflicting**, a real disagreement, with no guess at which source is right
- **Only in one record**, present in one source and not found in the other, without assuming that means an error
- **Could not confidently match**, a plausible pairing the evidence cannot actually confirm, left open rather than forced either way

<details>
<summary><strong>See exactly what it produces</strong></summary>

1. What each record represents, and as of when, including any meaningful gap between when the two were captured
2. How rows were matched across the two records, and which ones could not be matched at all
3. Every genuine disagreement, stated plainly with no guess at a cause
4. Every row present in only one record, kept separate from genuine disagreements
5. Presentation differences resolved and named, not silently dropped or wrongly reported as mismatches
6. Suggested follow-up for a person to approve, never a decision already made

</details>

See [the worked example](example/): a fictional hardware shop's physical stock count against its point-of-sale export, with a unit conversion, a formatting difference, a new delivery not yet logged, and an incomplete count all in play at once. For a harder case, a mismatched identifier that looks plausible but cannot be confirmed, a duplicated payment row, and a genuine status conflict, read [the second worked example](example-two/).

Use [the blank template](templates/reconciliation-template.md) for your own comparison, and [the review checklist](checks/checklist.md) before acting on any finding.

No installation, project, or coding required to try it once.

## Before You Use It

This reports where two records agree, disagree, or could not be matched. It does not decide which record is correct, or what to do about a genuine disagreement. That call, and any resulting correction, stays yours.

## Not the Same As

- [Claims vs Evidence Checker](https://github.com/shaunmarsden/claims-vs-evidence-checker) checks whether one document's own claims are actually backed by evidence inside that same document. This tool needs two independent records to begin with.
- [Is This Really a Pattern?](https://github.com/shaunmarsden/is-this-really-a-pattern) looks for a genuine repeated cause across many similar entries in one log. This tool compares exactly two records against each other, not many entries against themselves.

## Feedback

Used it on a real reconciliation? [Start a discussion](https://github.com/shaunmarsden/do-these-actually-match/discussions) if a match or a mismatch did not fit.

## Part of a Family

This is one of a family of free tools generalising [practical-ai-sales-workflows](https://github.com/shaunmarsden/practical-ai-sales-workflows) patterns beyond sales. See [sibling-projects](https://github.com/shaunmarsden/sibling-projects) for the rest. Not sure which one actually fits? Try [the interactive picker](https://shaunmarsden.github.io/sibling-projects/) for clickable cards, or [the router](https://github.com/shaunmarsden/sibling-projects/blob/main/ROUTER.md) if you would rather paste a description into an AI chat.
