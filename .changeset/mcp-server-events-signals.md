---
'@mastra/code-sdk': minor
---

Added live MCP updates to Mastra Code.

**Tool list refresh** — when a connected MCP server announces that its tools changed, Mastra Code re-lists that server's tools so the agent sees them without `/mcp reload`.

**MCP Events (experimental)** — when MCP servers are configured, the agent gets the `mcp_events_list`, `mcp_events_subscribe` and `mcp_events_unsubscribe` tools. It can subscribe the current thread to a server's events, with the arguments the event needs, and each occurrence arrives in the thread as an untrusted notification.
