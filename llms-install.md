# Install electroatlas (instructions for agents)

Remote MCP server, Streamable HTTP, no sign-in, no API key, nothing to build or download.

Server URL: `https://electroatlas.ru/mcp`

## Cline

```sh
cline mcp install electroatlas https://electroatlas.ru/mcp --transport http --yes
```

Or add this to `cline_mcp_settings.json`, keeping the servers already listed there:

```json
{
  "mcpServers": {
    "electroatlas": {
      "transport": {
        "type": "streamableHttp",
        "url": "https://electroatlas.ru/mcp"
      }
    }
  }
}
```

## Check

The client lists the tools `search` and `fetch`.
