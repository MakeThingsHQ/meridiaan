# Meridiaan

**Project memory for AI agents.** One knowledge base per project, shared by your whole team and every agent you use, read and kept up to date by the agents themselves over MCP.

[Website](https://meridiaan.io) · [Docs](https://docs.meridiaan.io) · [Connect a client](clients/) · [Workspace templates](templates/) · [Discussions](../../discussions)

---

## The problem

Every new agent session starts from zero. You re-explain the architecture, the decision you took six weeks ago, and why the obvious alternative was ruled out. The usual fix is an instructions file in the repository, and it works until it grows to two thousand lines that neither you nor the agent can read. It also stops at the edge of the repository and of the tool: another agent, another component, another person, and the context is gone.

## What Meridiaan does

- **One memory, any agent.** A Workspace is a remote MCP server. Claude Code, Cursor, Codex, VS Code, Copilot and anything else that speaks MCP read and write the same knowledge base. Use a cheap model for the easy tasks and a strong one for the hard ones, on the same context.
- **The agents keep it current.** Agents create and update Documents while they work: decisions, specs, open questions, todos. You read, correct and steer from the web app or from any agent.
- **The Workspace explains itself.** Every Collection carries its type, its statuses and its instructions, and the agent receives them inside the tool responses. Nobody has to re-explain how the project is organised.
- **Sized for context windows.** Each Document keeps its own size and links to the others, so an agent pulls the part it needs instead of the whole project.
- **Shared, with roles.** Owners, Editors and Viewers. People and agents work on the same Workspace, and you can see what the agents are doing.
- **Nothing to host.** No MCP server to write, deploy or keep alive.

## How it works

```
Workspace            one project, one MCP address
 └── Collections     Decisions, Features, Open Points, Wiki, Todos... each with statuses and instructions
      └── Documents  title, summary, status, body, links to other Documents
```

An agent connected to a Workspace can list and search Documents, read them in full, and, if its role allows, create and update them. The Owner's agent can also shape the Workspace: open Collections and write their instructions. The full list is in [the tools page](https://docs.meridiaan.io/tools.md).

## Quickstart

1. **Create a Workspace** at [meridiaan.io](https://meridiaan.io).
2. **Connect your agent.** Every Workspace has its own address:

   ```
   https://mcp.meridiaan.io/mcp/<workspace-id>
   ```

   Authenticate with **OAuth** (the client only needs the address, then opens a browser to confirm) or with the **Workspace token** from the Connection page, sent as `Authorization: Bearer <token>`. Ready-made configurations for each client are in [`clients/`](clients/).
3. **Let the agent set it up.** On an empty Workspace the Owner's agent is guided to ask what you are building and open the right Collections. Or start from a [template](templates/).
4. **See it work.** Follow the [two-session test](examples/two-session-test.md): tell one agent a decision, then ask a different session or a different agent why it was taken.

## Repository contents

| Folder | What is inside |
|---|---|
| [`clients/`](clients/) | Configuration for each MCP client, with what has been verified |
| [`templates/`](templates/) | Workspace structures you can hand to your agent, including the one used to build Meridiaan itself |
| [`examples/`](examples/) | Prompts to try: the two-session test, importing your existing instructions files |
| [`CHANGELOG.md`](CHANGELOG.md) | What changed in the service |

The Meridiaan service itself is not open source. This repository holds everything around it that is useful in the open: configurations, templates, examples, and the public place to ask questions and report problems.

## Help and feedback

- **Questions and ideas:** [Discussions](../../discussions)
- **Something broken, or a client configuration that does not work:** [Issues](../../issues/new/choose)
- **Account and billing:** support@meridiaan.io
- **Security:** see [SECURITY.md](SECURITY.md)

Meridiaan has just launched. If something is confusing, that is a bug in how we explain it: tell us.
