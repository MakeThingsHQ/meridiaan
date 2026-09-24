# Template: software product

For a product with several components (backend, frontend, infrastructure...), built alone or in a small team, with several agents working in parallel. This is a simplified version of the structure we use to build Meridiaan itself: one agent per component, all on the same Workspace.

The idea: **decisions and reasons live in one place, work lives per component, and everything links by id**. An agent working on the frontend can read why the backend chose something, without anyone explaining it.

## Collections

| Collection | Type | Statuses | What goes in |
|---|---|---|---|
| Features | `feature` | planned, blocked, in_progress, shipped | Capabilities to build. Each belongs to a Release and owns its Todos. |
| Releases | `release` | planned, in_progress, released | A release is an index: one line and the id of each Feature in it. |
| Decisions | `decision` | proposed, accepted, superseded | A choice and why it was made. |
| Open Points | `open_point` | open, closed | Questions without an answer yet, and what they block. |
| Brainstorming | `brainstorming` | open, closed | Reasoning out loud before a Decision. |
| Tech Wiki | `wiki` | current, outdated, deprecated | How things are built now. |
| Product Wiki | `wiki` | current, outdated, deprecated | What the product does now, for whom, and how it is positioned. |
| Bugs | `bug` | open, in_progress, resolved, closed | Defects. |
| Todo Backend | `todo` | open, blocked, in_progress, done | Work for one component. Repeat per component. |
| Todo Frontend | `todo` | open, blocked, in_progress, done | Same, for the frontend. |

## Setup prompt

```text
Set up this Workspace for a software product with several components.
First read the Collection types available, then open these Collections,
with these statuses and these instructions. Write the instructions in
plain text, without Markdown.

1. Features (feature): planned, blocked, in_progress, shipped.
   Instructions: A Feature belongs to one Release and owns its Todos.
   When you create it, create the Todos that are already clear. Do not
   repeat what a Todo says: one line and its id. Choices go into a
   linked Decision. When updating, rewrite the paragraph instead of
   appending a dated one.

2. Releases (release): planned, in_progress, released.
   Instructions: The body is an index: one line and the id for each
   Feature, Bug or Open Point in the release, and each of them cites
   the Release id. Do not copy what the cited Document already says.

3. Decisions (decision): proposed, accepted, superseded.
   Instructions: Record a choice and the reason for it. Link the
   Document it concerns by id, and add the Decision id to that
   Document. A Decision that replaces another marks it superseded.

4. Open Points (open_point): open, closed.
   Instructions: A question without an answer and what it blocks.
   When closed, it becomes a Decision, linked by id.

5. Brainstorming (brainstorming): open, closed.
   Instructions: Reasoning before a choice. Every Brainstorming leads
   to at least one Decision, and the two cite each other by id.

6. Tech Wiki (wiki): current, outdated, deprecated.
   Instructions: How a thing is built now, not how we got here. When
   updating, rewrite the paragraph. What changed is cited in one line
   with the id of the Decision or Feature. No commit hashes or deploy
   dates: those go in the Todo.

7. Product Wiki (wiki): current, outdated, deprecated.
   Instructions: What the product does now and for whom. Same
   rewriting rule as the Tech Wiki.

8. Bugs (bug): open, in_progress, resolved, closed.
   Instructions: Steps to reproduce, expected and actual behaviour,
   the component affected. Link the Todo that fixes it.

9. One Todo Collection per component, for example Todo Backend and
   Todo Frontend (todo): open, blocked, in_progress, done.
   Instructions: Every Todo links a Feature; if none fits, propose one.
   No code unless it shows a pattern to replicate. Close the Todo in
   the same act as the release, and if it asks another component to do
   something, do it now in that component's Collection.

Ask me which components the product has before creating the Todo
Collections. When you are done, list what you created.
```
