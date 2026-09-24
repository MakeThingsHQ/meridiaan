# LM Studio

LM Studio has a single `mcp.json` in the user folder (no project scope) and follows Cursor's notation.

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

A local model on the same Workspace is a good way to keep the easy questions free, and send the hard ones to a paid model.

## One-click install

The Connection page offers an **Add to LM Studio** link. With a token, the token travels inside the link.

Status: not yet verified. [Report](../../../issues/new?template=client_report.yml) how it went.
