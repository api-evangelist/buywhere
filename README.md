# BuyWhere (buywhere)

Agent-native, MCP-native product catalog and price comparison API for Southeast Asia and US e-commerce. Search 1.5M+ products across Shopee, Lazada, Carousell, FairPrice, Best Denki, Amazon, Walmart, Best Buy, and 20+ retailers. AI agents and MCP clients discover and route purchases to local merchants through a hosted MCP HTTP endpoint at api.buywhere.ai/mcp or via the @buywhere/mcp-server STDIO package.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/buywhere/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/buywhere/refs/heads/main/apis.yml)

## Scope

- **Type:** Index
- **Position:** Consumer
- **Access:** 3rd-Party

## Tags

- E-commerce
- Shopping
- Price Comparison
- SEA
- Southeast Asia
- AI Agents
- Product Catalog

## Timestamps

- **Created:** 2026-05-16
- **Modified:** 2026-05-19

## APIs

### BuyWhere Product Catalog API

Agent-native REST and MCP product catalog covering 1.5M+ products across Southeast Asian and US e-commerce platforms. Operations include keyword search, side-by-side comparison, deals discovery, price history, and category browsing. Responses are Schema.org-compatible (Product, Offer, ItemList) and include normalized structured_specs and comparison_attributes so LLMs can rank and reason without scraping. Same operations are exposed to MCP clients at api.buywhere.ai/mcp.

- **Human URL:** [https://api.buywhere.ai/](https://api.buywhere.ai/)
- **Base URL:** `https://api.buywhere.ai/v1`

#### Tags

- E-commerce
- Shopping
- Price Comparison
- SEA
- Southeast Asia
- AI Agents
- Product Catalog
- MCP

#### Properties

- [OpenAPI](openapi/buywhere-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/buywhere.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/buywhere.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [OpenAPI](https://api.buywhere.ai/openapi.json) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Documentation](https://api.buywhere.ai/)
- [M C P Documentation](https://api.buywhere.ai/docs/guides/mcp)
- [M C P Endpoint](https://api.buywhere.ai/mcp)
- [Plugin Manifest](https://api.buywhere.ai/.well-known/ai-plugin.json)
- [L L Ms Txt](https://api.buywhere.ai/llms.txt)
- [JSON Schema](json-schema/buywhere-product-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/buywhere-offer-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/buywhere-price-history-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/buywhere-category-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Structure](json-structure/buywhere-product-structure.json)
- [JSON Structure](json-structure/buywhere-offer-structure.json)
- [Spectral Rules](rules/buywhere-rules.yml)
- [Example](examples/buywhere-searchProducts-example.json)
- [Example](examples/buywhere-getDeals-example.json)
- [Example](examples/buywhere-compareProducts-example.json)
- [Example](examples/buywhere-getProduct-example.json)
- [Example](examples/buywhere-getProductPrices-example.json)
- [Example](examples/buywhere-listCategories-example.json)
- [Example](examples/buywhere-getCategoryProducts-example.json)
- [Example](examples/buywhere-registerAgent-example.json)
- [Example](examples/buywhere-mcp-tools-call-example.json)

## Common Properties

- [Website](https://api.buywhere.ai/)
- [Documentation](https://api.buywhere.ai/)
- [M C P Documentation](https://api.buywhere.ai/docs/guides/mcp)
- [M C P Endpoint](https://api.buywhere.ai/mcp)
- [OpenAPI](https://api.buywhere.ai/openapi.json) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Plugin Manifest](https://api.buywhere.ai/.well-known/ai-plugin.json)
- [L L Ms Txt](https://api.buywhere.ai/llms.txt)
- [Website](https://api.buywhere.ai/us/)
- [Git Hub](https://github.com/BuyWhere)
- [Git Hub](https://github.com/BuyWhere/buywhere)
- [Plans](plans/buywhere-plans-pricing.yml)
- [Rate Limits](rate-limits/buywhere-rate-limits.yml)
- [Fin Ops](finops/buywhere-finops.yml)
- [Vocabulary](vocabulary/buywhere-vocabulary.yml)
- [JSON-LD](json-ld/buywhere-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
