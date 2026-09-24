# Claude Desktop and claude.ai

Remote MCP servers are added from the app, not from a file. `claude_desktop_config.json` is only for local servers.

Custom connectors are available on Anthropic paid plans.

## With OAuth

1. Open **Settings**, then **Connectors**.
2. **Add custom connector**.
3. Paste the Workspace address: `https://mcp.meridiaan.io/mcp/<workspace-id>`.
4. Connect: a browser opens, you confirm on Meridiaan, done.

## With the Workspace token

1. Open **Settings**, then **Connectors**, then **Add custom connector**.
2. Paste the Workspace address.
3. Set authentication to **None**.
4. Add a header named `authorization` with value `Bearer <token>`. Keep the word `Bearer` and the space: Claude sends the value exactly as written.
5. Save.

Every Workspace has a different address, so you can add one connector per Workspace.

Status: verified.
