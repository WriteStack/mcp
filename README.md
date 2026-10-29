# WriteStack MCP

Remote [Model Context Protocol](https://modelcontextprotocol.io) server for [WriteStack](https://www.writestack.io) — the Substack creator OS.

Connect Claude, ChatGPT, Notion, or any MCP client to a writer's WriteStack account. Draft and schedule Substack Notes, manage articles, and read statistics.

## Endpoint

- **URL:** `https://www.writestack.io/api/mcp/mcp`
- **Transport:** Streamable HTTP
- **Docs:** https://www.writestack.io/mcp
- **Privacy:** https://www.writestack.io/privacy
- **Homepage:** https://www.writestack.io

## Quick start (OAuth clients)

1. Add a custom MCP connector and paste `https://www.writestack.io/api/mcp/mcp`.
2. Sign in to WriteStack and approve access.
3. Ask in plain language, e.g. “Draft three Notes about my last post and queue them.”

Guides: [Claude](https://blogs.writestack.io/?post=2-guides-4-add-mcp-connector) · [ChatGPT](https://guides.writestack.io/?post=2-guides-add-mcp-gpt) · [Notion](https://blogs.writestack.io/?post=2-guides-add-mcp-connector-notion)

## API key clients (`mcp-remote`)

Create a key in WriteStack under **Settings → MCP**, then:

```json
{
  "mcpServers": {
    "writestack": {
      "command": "npx",
      "args": [
        "-y",
        "mcp-remote",
        "https://www.writestack.io/api/mcp/mcp",
        "--header",
        "Authorization: Bearer ws_your_api_key"
      ]
    }
  }
}
```

## Official registry metadata

See [`server.json`](./server.json) for the remote-server metadata published to the [Official MCP Registry](https://modelcontextprotocol.io/registry/about) as `io.writestack/mcp`.

## Logo

Square logo (960×960 PNG): https://cdn.writestack.io/writestack-app/og/logo.png

## License

Documentation and metadata in this repository are MIT. WriteStack the product remains proprietary.
