# Connecting a client

Every Workspace has its own address, shown on its **Connection** page:

```
https://mcp.meridiaan.io/mcp/<workspace-id>
```

Two ways to authenticate, and neither excludes the other:

- **OAuth 2.1.** The client only needs the address. It registers itself, opens a browser, you confirm, and the agent receives a token bound to that Workspace that renews on its own. Nothing secret is written in your configuration. Use it wherever your client supports it.
- **Workspace token.** Copy it from the Connection page and send it as `Authorization: Bearer <token>`. It does not expire; rotate it by hand from the same page if it leaks.

Transport is Streamable HTTP. In every file below, replace `<workspace-id>` and `<token>`, and pick a server name without spaces or accents (for example `meridiaan-myproject`): some clients use it as a key or as a command argument.

## Clients

| Client | Where the configuration goes | Status |
|---|---|---|
| [Claude Code](claude-code.md) | `claude mcp add` command, or `.mcp.json` | Verified |
| [Claude Desktop and claude.ai](claude-desktop.md) | Settings, Connectors, custom connector | Verified |
| [Codex CLI](codex.md) | `~/.codex/config.toml` | Connection verified, this exact block not yet |
| [Cursor](cursor.md) | `.cursor/mcp.json` or `~/.cursor/mcp.json`, or one-click link | Not yet verified |
| [VS Code](vscode.md) | `.vscode/mcp.json`, or one-click link | Not yet verified |
| [GitHub Copilot CLI](copilot-cli.md) | `.mcp.json` or its own config | Not yet verified |
| [opencode](opencode.md) | `opencode.json` | Not yet verified |
| [Antigravity](antigravity.md) | its MCP configuration | Not yet verified |
| [LM Studio](lm-studio.md) | `mcp.json` in the user folder, or one-click link | Not yet verified |
| [Python](python.md) | code, official MCP SDK | Not yet verified |
| [LangChain and LangGraph](langchain.md) | code, `langchain-mcp-adapters` | Not yet verified |
| [Anything else](generic.md) | address plus header | |

**"Not yet verified"** means the configuration follows the client's documented format but we have not run it against the real client with the current address format. If you try one, open a [client report](../../../issues/new?template=client_report.yml) either way: it moves the row to "Verified" for everyone.

## About one-click links

Cursor, VS Code and LM Studio accept install links, and the Connection page offers them. With a Workspace token, **the token travels inside the link**, so it ends up in that client's history. Prefer OAuth where the client supports it, or rotate the token if you shared the link.
