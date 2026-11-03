# Tendrils MCP Server

A public **remote MCP server** exposing real commerce tools over JSON-RPC / Streamable HTTP — from systems running on a live retail deployment (42,000+ products, 12 vendor feeds, 4 storefronts).

**Endpoint:** `https://tendrils.io/mcp`
**Transport:** Streamable HTTP (JSON-RPC 2.0)
**Auth:** none required for the public tool surface — rate-limited per IP
**Server card:** `https://tendrils.io/.well-known/mcp`
**API spec:** `https://tendrils.io/openapi.json`
**Docs:** `https://tendrils.io/developers`

## Call it

```json
POST https://tendrils.io/mcp
{ "jsonrpc": "2.0", "id": 1, "method": "tools/list" }
```

## What agents can do

- Discover and read commerce tools (`tools/list`, `tools/call`)
- Read agent-facing resources (`resources/list`, `resources/read`) — docs, llms-full content
- Query the site/service catalog, developer docs and enquiry flows

## Links

- Site: https://tendrils.io
- llms.txt: https://tendrils.io/llms.txt
- OpenAPI: https://tendrils.io/openapi.json
