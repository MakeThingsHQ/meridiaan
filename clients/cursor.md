# Cursor

`.cursor/mcp.json` in the project, or `~/.cursor/mcp.json` for all projects. Cursor infers the transport from `url`: do not declare it.

```json
{
  "mcpServers": {
    "meridiaan-myproject": {
      "url": "https://mcp.meridiaan.io/mcp/<workspace-id>",
      "headers": {
        "Authorization": "Bearer <token>"
      }
    }
  }
}
```

For OAuth, remove `headers`: Cursor will ask you to authenticate.

## One-click install

The Connection page of your Workspace offers an **Add to Cursor** link. It installs globally, and with a token the token travels inside the link.

Status: not yet verified with the current address format. [Report](../../../issues/new?template=client_report.yml) how it went.
