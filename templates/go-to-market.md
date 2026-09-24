# Template: go-to-market

For launching and distributing a product: what you publish, who you talk to, what they told you, and the work that is not code. It is the structure we opened for Meridiaan's own launch, next to the product Collections.

## Collections

| Collection | Type | Statuses | What goes in |
|---|---|---|---|
| Plans | `plan` | draft, active, done | The launch as numbered steps, ticked off as they are done. |
| Todo Marketing | `todo` | open, blocked, in_progress, done | Actions that bring people to the product and are not code. |
| Content | `article` | draft, ready, published | Every piece of public content, one Document each. |
| Contacts | `profile` | active, dormant, closed | One card per person or organisation, in target or not. |
| Conversations | `conversation` | active | Calls, interviews, feedback, with quotes kept verbatim. |

## Setup prompt

```text
Set up the go-to-market part of this Workspace. First read the
Collection types available, then open these Collections with these
statuses and instructions, in plain text without Markdown.

1. Plans (plan): draft, active, done.
   Instructions: One Document per plan: the steps in order as a
   numbered list, ticked as they are done. When a step becomes work of
   its own, open a Todo and cite its id in the step.

2. Todo Marketing (todo): open, blocked, in_progress, done.
   Instructions: Actions that bring people to the product and are not
   code: accounts, content to produce, outreach, campaigns, directory
   submissions. Each cites the Plan step it comes from. Never write
   credentials. Close it with a link to what it produced.

3. Content (article): draft, ready, published.
   Instructions: One Document per piece: social post, video script,
   outreach message template, article, comparison page. Title with
   channel and topic. When published, add the URL and the date.

4. Contacts (profile): active, dormant, closed.
   Instructions: One card per person or organisation, in target or
   not. First line: the kind of relationship. For leads, also the
   stage. Minimum data: name, role, channel, where we met. No phone
   numbers or emails unless needed. History as dated lines.

5. Conversations (conversation): active.
   Instructions: Title with date and who. Important sentences quoted
   verbatim, kept apart from our interpretation. Link the Contact.

When you are done, list what you created.
```
