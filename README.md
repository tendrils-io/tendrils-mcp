# Tendrils MCP Server

A public **remote MCP server** exposing real commerce tools for AI agents over JSON-RPC / Streamable HTTP — backed by a live furniture-retail deployment (42,000+ products, 12 vendor feeds, 4 storefronts).

**Endpoint:** `https://tendrils.io/mcp`
**Transport:** Streamable HTTP (JSON-RPC 2.0)
**Auth:** none required — rate-limited per IP
**Server card:** `https://tendrils.io/.well-known/mcp`
**API spec:** `https://tendrils.io/openapi.json`
**Docs:** `https://tendrils.io/developers`

## Call it

```json
POST https://tendrils.io/mcp
{ "jsonrpc": "2.0", "id": 1, "method": "tools/list" }
```

## Tools

| Tool | What it does |
|---|---|
| `find_products_by_constraints` | Search the catalog by category, budget, material, features, stock availability |
| `get_product_details` | Full specs, parsed dimensions, materials, care, variant matrix |
| `check_variant_availability` | Live per-variant stock quantities for option combos |
| `compare_products` / `compare_products_deep_matrix` | Side-by-side spec matrices across frame, fabric, dimensions |
| `create_checkout_handoff` | Turn selected variants into a 1-click Shopify checkout URL |
| `calculate_room_fit_and_clearance` | Will-it-fit math for sofas/sectionals with walking clearance |
| `generate_room_floorplan` | 2D SVG architectural floorplan with furniture placement |
| `match_fabric_and_lighting` | Match upholstery to room paint and light exposure |
| `get_product_ar_model` | Apple QuickLook (.usdz) / Android (.glb) AR model paths |
| `build_coordinated_room_bundle` | Anchor piece + matching ottoman/accent chair bundles |

## Links

- Site: https://tendrils.io
- llms.txt: https://tendrils.io/llms.txt
- OpenAPI: https://tendrils.io/openapi.json
