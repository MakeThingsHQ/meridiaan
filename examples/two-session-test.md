# The two-session test

Five minutes to see what Meridiaan is for. You need a Workspace connected to at least one agent, and ideally two different agents (for example Claude Code and Cursor, or a paid model and a local one).

## Session 1: tell it something

Open a session and paste:

```text
Look at how this Workspace is organised. Then record this decision in
the right Collection, with the reason and what it rules out:

"We store uploaded files in object storage, not in the database. The
database stays small and backups stay fast. Ruled out: storing them as
blobs in Postgres, because restoring a 40 GB dump takes hours."
```

Use a real decision from your project if you have one: the test is more convincing.

The agent will find the Collections, pick the one for decisions (or propose opening it, if you are the Owner and it does not exist), and write the Document.

## Session 2: ask, somewhere else

Close the session. Open a **new** one, or better, **a different agent** connected to the same Workspace, and ask:

```text
Where do we store uploaded files, and why not in Postgres?
```

The second agent was never told. It searches the Workspace, finds the Decision, and answers with the reason and the alternative that was ruled out.

That is the whole point: the knowledge belongs to the project, not to a chat, a model, or a vendor.

## Going further

- Ask the second agent to **add** a consequence to the same Decision, then check the change in the web app.
- Connect a teammate as Editor and let their agent ask the same question.
- Hand the Workspace a [template](../templates/) and repeat with a real feature.
