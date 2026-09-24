# Codex CLI

Codex reads `~/.codex/config.toml`, one section per server. Global scope only.

## With the token in an environment variable (recommended)

```toml
[mcp_servers.meridiaan-myproject]
url = "https://mcp.meridiaan.io/mcp/<workspace-id>"
bearer_token_env_var = "MERIDIAAN_TOKEN"
```

```bash
export MERIDIAAN_TOKEN="<token>"
```

## With the token written in the file

```toml
[mcp_servers.meridiaan-myproject]
url = "https://mcp.meridiaan.io/mcp/<workspace-id>"
http_headers = { "Authorization" = "Bearer <token>" }
```

Status: the connection is verified; this exact block is not yet. If it works for you, or if it does not, [tell us](../../../issues/new?template=client_report.yml).
