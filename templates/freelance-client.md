# Template: freelance client

One Workspace per client. Clients never mix, and at the end of the engagement the Workspace is what you hand over, or what you keep.

Your own conventions, the ones that belong to no client, go in your personal Workspace (every account has one) so they follow you into every project without being rewritten.

## Collections

| Collection | Type | Statuses | What goes in |
|---|---|---|---|
| Requirements | `requirement` | proposed, active, deprecated | What the client asked for, in their words, and what was agreed. |
| Decisions | `decision` | proposed, accepted, superseded | Choices, especially the ones the client signed off. |
| Meetings | `meeting` | active | Who was there, what was discussed, what was decided. |
| Todos | `todo` | open, in_progress, done | The work. |
| Handover | `how_to` | current, outdated, deprecated | What the client needs to run the thing without you. |

## Setup prompt

```text
Set up this Workspace for a client engagement. First read the
Collection types available, then open these Collections with these
statuses and instructions, in plain text without Markdown.

1. Requirements (requirement): proposed, active, deprecated.
   Instructions: One Document per requirement, in the client's words
   first, then what was agreed. Mark deprecated when the client drops
   it, never delete it.

2. Decisions (decision): proposed, accepted, superseded.
   Instructions: The choice, the reason, and whether the client
   approved it and when. Link the Requirement it answers by id.

3. Meetings (meeting): active.
   Instructions: Title with date and participants. What was discussed,
   what was decided (each decision also as a Decision, linked by id),
   who does what next.

4. Todos (todo): open, in_progress, done.
   Instructions: Link the Requirement or Decision the Todo comes from.

5. Handover (how_to): current, outdated, deprecated.
   Instructions: What the client needs to operate, deploy and recover
   the project without us. Keep it current as the project changes, not
   only at the end.

When you are done, list what you created.
```
