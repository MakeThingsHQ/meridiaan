# Claude Code

## With OAuth

```bash
claude mcp add --transport http --scope project meridiaan-myproject \
  https://mcp.meridiaan.io/mcp/<workspace-id>
```

Then run `/mcp` inside Claude Code, pick the server and authenticate: a browser opens, you confirm, done.

## With the Workspace token

```bash
claude mcp add --transport http --scope project meridiaan-myproject \
  https://mcp.meridiaan.io/mcp/<workspace-id> \
  --header "Authorization: Bearer <token>"
```

## Scope

- `--scope project` writes the server into `.mcp.json` at the root of the repository, so everyone who clones it gets the same Workspace. Do not commit a token there: use OAuth for shared repositories.
- `--scope user` makes it available in all your projects.
- Without `--scope`, the server goes into a local scope that is neither of the two.

## Equivalent `.mcp.json`

```json
{
  "mcpServers": {
    "meridiaan-myproject": {
      "type": "http",
      "url": "https://mcp.meridiaan.io/mcp/<workspace-id>"
    }
  }
}
```

Status: verified.
