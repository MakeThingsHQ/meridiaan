# VS Code

`.vscode/mcp.json` in the project. VS Code uses the key `servers` (not `mcpServers`) and wants the transport declared. The agent mode reads the same file: there is nothing else to configure.

```json
{
  "servers": {
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

For OAuth, remove `headers`: VS Code will ask you to authenticate.

## One-click install

The Connection page offers an **Add to VS Code** link. It installs in the user profile, not in the workspace, and with a token the token travels inside the link.

Status: not yet verified with the current address format. [Report](../../../issues/new?template=client_report.yml) how it went.
