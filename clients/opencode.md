# opencode

`opencode.json` in the project. opencode uses its own shape: key `mcp`, and each server declares `type: "remote"`.

```json
{
  "$schema": "https://opencode.ai/config.json",
  "mcp": {
    "meridiaan-myproject": {
      "type": "remote",
      "url": "https://mcp.meridiaan.io/mcp/<workspace-id>",
      "headers": {
        "Authorization": "Bearer <token>"
      }
    }
  }
}
```

Status: not yet verified. [Report](../../../issues/new?template=client_report.yml) how it went.
