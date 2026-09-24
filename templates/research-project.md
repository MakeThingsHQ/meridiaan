# Template: research project

For a research line or a deep-tech project: what you believe, how you are testing it, what came out, and, just as important, what you ruled out and why, so no agent or colleague proposes it again six months later.

## Collections

| Collection | Type | Statuses | What goes in |
|---|---|---|---|
| Hypotheses | `custom` | open, supported, rejected | What you think is true and how you would know. |
| Protocols | `how_to` | current, outdated, deprecated | How an experiment or a measurement is done. |
| Results | `note` | active | What an experiment produced, with the conditions. |
| Papers | `paper` | active | Key takeaways from the literature, with the reference. |
| Decisions | `decision` | proposed, accepted, superseded | Directions taken and directions abandoned, with the reason. |

## Setup prompt

```text
Set up this Workspace for a research project. First read the
Collection types available, then open these Collections with these
statuses and instructions, in plain text without Markdown.

1. Hypotheses (custom): open, supported, rejected.
   Instructions: One hypothesis per Document: the claim, what result
   would support it, what would reject it. Link the Results that
   decided it. Rejected hypotheses stay, with the reason.

2. Protocols (how_to): current, outdated, deprecated.
   Instructions: Step by step, with equipment, parameters and known
   pitfalls. When a protocol changes, rewrite it and cite the Decision.

3. Results (note): active.
   Instructions: Title with date and experiment. Conditions, protocol
   used (by id), raw outcome, then interpretation kept separate from
   the data. Link the Hypothesis it tests.

4. Papers (paper): active.
   Instructions: Full reference, the claim that matters for us, the
   method in two lines, and how it relates to our Hypotheses.

5. Decisions (decision): proposed, accepted, superseded.
   Instructions: Directions taken and abandoned, with the evidence (ids
   of Results and Papers). An abandoned direction is a Decision too.

When you are done, list what you created.
```
