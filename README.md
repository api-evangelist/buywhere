# BuyWhere (buywhere)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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
