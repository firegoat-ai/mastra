---
'@mastra/code-sdk': minor
---

Added live MCP updates to Mastra Code.

**Tool list refresh** — when a connected MCP server announces that its tools changed, Mastra Code re-lists that server's tools so the agent sees them without `/mcp reload`.

**MCP Events (experimental)** — set `events` on a server in `mcp.json` to subscribe to its events. Each occurrence arrives in the active thread as a notification and starts or joins an agent turn. Off by default.

```json
{
  "mcpServers": {
    "github": { "url": "https://example.com/mcp", "events": ["push"] },
    "alerts": { "command": "npx", "args": ["alerts-mcp"], "events": true }
  }
}
```
