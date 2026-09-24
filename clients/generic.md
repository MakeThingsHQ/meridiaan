# Any other MCP client

If your tool is not in the list, it needs three values. How it wants them written is up to the tool.

```
Server name:  meridiaan-myproject
Address:      https://mcp.meridiaan.io/mcp/<workspace-id>
Header:       Authorization: Bearer <token>
```

Transport: Streamable HTTP. If the tool supports OAuth for remote servers, give it only the address and skip the header.

Got it working with a tool we do not list? [Tell us how](../../../issues/new?template=client_report.yml) and we will add it.
