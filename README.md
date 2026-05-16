# BuyWhere (buywhere)

Agent-native, MCP-native product catalog and price comparison API for Southeast Asia and US e-commerce. Search 1.5M+ products across Shopee, Lazada, Carousell, FairPrice, Best Denki, Amazon, Walmart, Best Buy, and 20+ retailers. AI agents and MCP clients discover and route purchases to local merchants through a hosted MCP HTTP endpoint at `api.buywhere.ai/mcp` or via the `@buywhere/mcp-server` STDIO package.

- **Source:** https://api.buywhere.ai/
- **OpenAPI (upstream):** https://api.buywhere.ai/openapi.json
- **MCP endpoint:** https://api.buywhere.ai/mcp
- **MCP integration guide:** https://api.buywhere.ai/docs/guides/mcp
- **AI plugin manifest:** https://api.buywhere.ai/.well-known/ai-plugin.json
- **llms.txt:** https://api.buywhere.ai/llms.txt
- **GitHub org:** https://github.com/BuyWhere
- **api-search issue:** [#25](https://github.com/api-search/network/issues/25)

## MCP positioning

BuyWhere is **MCP-native**. The same operations exposed at `https://api.buywhere.ai/v1/*` over REST are available to MCP-compatible AI agents (Claude Desktop, Cursor, ChatGPT, custom clients) at `POST https://api.buywhere.ai/mcp`, and as a local STDIO server via `npx -y @buywhere/mcp-server`. The hosted MCP server publishes the following tools:

| MCP tool | Description |
| --- | --- |
| `search_products` | Keyword search with price / region / country / merchant filters. |
| `get_product` | Full product detail by ID. |
| `compare_products` | Side-by-side comparison of 2–10 products. |
| `get_deals` | Discounted products sorted by discount percentage. |
| `list_categories` | Browse available categories. |
| `find_best_price` | Cheapest current listing for a product across all merchants. |

## Operations

The OpenAPI spec at [`openapi/buywhere-openapi.yml`](openapi/buywhere-openapi.yml) covers the BuyWhere REST surface (`https://api.buywhere.ai/v1`):

| Operation ID | Method & Path | Summary |
| --- | --- | --- |
| `registerAgent` | `POST /auth/register` | Register Agent And Issue API Key |
| `searchProducts` | `GET /products/search` | Search Products By Keyword |
| `getDeals` | `GET /products/deals` | List Discounted Products By Discount Percentage |
| `compareProducts` | `GET /products/compare` | Compare Multiple Products Side-By-Side |
| `getProduct` | `GET /products/{id}` | Get Product By ID |
| `getProductPrices` | `GET /products/{id}/prices` | Get Product Price History |
| `listCategories` | `GET /categories` | List Top-Level Product Categories |
| `getCategoryProducts` | `GET /categories/{slug}` | Get Products Within A Category |

## Pricing, rate limits, and FinOps

BuyWhere advertises three tiers keyed off API-key prefix. Pricing for the live and partner tiers is not yet on a formal pricing page (contact `api@buywhere.ai`); the profiles below are marked `reconciled: false` and capture the publicly documented limits.

| Tier | Key prefix | Rate | Monthly quota | Pricing |
| --- | --- | --- | --- | --- |
| Free | `bw_free_*` | 60 req/min | 1,000 calls/month | Free |
| Live | `bw_live_*` | 600 req/min | Not published | Contact sales |
| Partner | `bw_partner_*` | Unlimited | Negotiated | Contact sales |

See [`plans/buywhere-plans-pricing.yml`](plans/buywhere-plans-pricing.yml), [`rate-limits/buywhere-rate-limits.yml`](rate-limits/buywhere-rate-limits.yml), and [`finops/buywhere-finops.yml`](finops/buywhere-finops.yml) for the full API Commons / FOCUS-aligned profiles.

## Artifacts

| Folder | Contents |
| --- | --- |
| `openapi/` | OpenAPI 3.0 specification with title-cased summaries, tags, schemas, and examples |
| `capabilities/` | Naftiko shared capability (`shared/buywhere-product-catalog-api.yaml`) and a composed workflow capability (`price-comparison-shopping-agent.yaml`) |
| `json-schema/` | JSON Schemas for product, offer, price history, and category |
| `json-structure/` | JSON Structure docs for product and offer, mapped to Schema.org |
| `json-ld/` | JSON-LD context aligning BuyWhere fields with `schema.org/Product` and `schema.org/Offer` |
| `examples/` | Request/response examples for every REST operation plus an MCP `tools/call` example |
| `rules/` | Spectral ruleset enforcing BuyWhere's conventions (summary casing, BearerAuth, versioned servers, kebab paths, 429 on search, etc.) |
| `vocabulary/` | Vocabulary mapping operations and capability dimensions |
| `plans/` | API Commons Plans 0.1 profile |
| `rate-limits/` | API Commons Rate Limits 0.1 profile |
| `finops/` | FinOps Framework / FOCUS 1.3 profile |

## SDKs and integrations

| Package | Language | Description |
| --- | --- | --- |
| [`buywhere-mcp`](https://github.com/BuyWhere/buywhere-mcp) | JavaScript | BuyWhere MCP server |
| `@buywhere/mcp-server` (npm) | JavaScript | Published STDIO MCP server |
| [`buywhere-py`](https://github.com/BuyWhere/buywhere-py) | Python | Official Python SDK |
| [`buywhere-llamaindex`](https://github.com/BuyWhere/buywhere-llamaindex) | Python | LlamaIndex FunctionTool wrappers |
| [`buywhere-cursor-plugin`](https://github.com/BuyWhere/buywhere-cursor-plugin) | Python | Cursor AI MCP plugin |
| [`buywhere-mcp-action`](https://github.com/BuyWhere/buywhere-mcp-action) | GitHub Action | BuyWhere MCP server as a GitHub Action |

## Authentication

Pass your API key as a Bearer token. Get a free key at `POST https://api.buywhere.ai/v1/auth/register`.

```bash
curl https://api.buywhere.ai/v1/products/search?q=laptop&country_code=SG \
  -H "Authorization: Bearer bw_free_xxx"
```

For MCP usage and STDIO/HTTP setup details see [`examples/buywhere-mcp-tools-call-example.json`](examples/buywhere-mcp-tools-call-example.json) and the [BuyWhere MCP guide](https://api.buywhere.ai/docs/guides/mcp).
