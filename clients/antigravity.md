# Antigravity

Editor, command line and app share the same MCP configuration. Same `mcpServers` key as most clients, but the address field is called `serverUrl`, not `url`.

```json
{
  "mcpServers": {
    "meridiaan-myproject": {
      "serverUrl": "https://mcp.meridiaan.io/mcp/<workspace-id>",
      "headers": {
        "Authorization": "Bearer <token>"
      }
    }
  }
}
```

Status: not yet verified. [Report](../../../issues/new?template=client_report.yml) how it went.
