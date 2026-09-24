# GitHub Copilot CLI

Copilot CLI reads `.mcp.json` at the root of the project, the same file Claude Code writes with `--scope project`. The transport is declared, so this block is not interchangeable with Cursor's.

```json
{
  "mcpServers": {
    "meridiaan-myproject": {
      "type": "http",
      "url": "https://mcp.meridiaan.io/mcp/<workspace-id>",
      "headers": {
        "Authorization": "Bearer <token>"
      }
    }
  }
}
```

Do not commit a token in a shared repository.

Status: not yet verified. [Report](../../../issues/new?template=client_report.yml) how it went.
