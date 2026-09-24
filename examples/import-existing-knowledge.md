# Bring in what you already have

You probably already have project knowledge somewhere: a `CLAUDE.md` or `AGENTS.md` that grew too long, a README, a `docs/` folder, decision notes. A native importer is not available yet, but your agent can do the job today: it reads the files in your repository and writes them into the Workspace as Documents.

## Prompt

Run it from an agent that has both your repository and the Workspace connected:

```text
Read the instructions files and the documentation in this repository:
CLAUDE.md, AGENTS.md, README.md and the docs/ folder, whichever exist.

Then look at how the Meridiaan Workspace is organised and propose how
to split that material into Documents: which Collection each piece
belongs to, with a title and a one-line summary. Decisions and their
reasons go to decisions, how things are built goes to the technical
wiki, open questions go to open points. One topic per Document.

Show me the plan before writing anything. After I confirm, create the
Documents and link related ones by id.

Do not copy secrets, tokens or credentials, even if you find them.
```

## After the import

- Keep the local instructions file short: what the agent must always do in this repository, plus a line saying that project knowledge lives in the Meridiaan Workspace.
- Run the [two-session test](two-session-test.md) with a question whose answer was buried in the old file.

Moving from a specific tool (Notion, Obsidian, Linear)? Write to support@meridiaan.io with its name: it helps us decide which native importer comes first.
