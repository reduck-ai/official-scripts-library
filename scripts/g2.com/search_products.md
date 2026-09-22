# Search G2 software products

Automatically search G2 software products on g2.com. Search G2's software directory by free-text query. Returns matching products with slug, name, star rating, review count and description, deduplicated. The slug feeds g2.com/get_product. Whitespace in the query is normalised. No login required. Fails loudly rather than returning an empty list: G2 always degrades to fuzzy matches, so zero results means the page did not render.

- Site: g2.com
- Address: `reduck/g2.com/search_products`
- Updated: 2026-09-17 (v3)
- Author: Reduck AI (reduck)

## About

Developers looking for a G2 API to search G2's software directory usually find there is none they can use: G2's API is reserved for vendors and partners. This script fills that gap. It works like an API endpoint — one call with typed arguments, a JSON response — but runs through a real browser, yours or a hosted one, so it needs no G2 developer account, API key or app review.

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/g2.com/search_products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/g2.com/search_products
```

## Input

- `query` (string, required): Free-text search query, e.g. 'email marketing' or 'notion'. Surrounding whitespace is normalised.

## Output

- `count` (integer, required)
- `query` (string, required): The normalised query actually searched.
- `products` (array, required)

## FAQ

### What does "Search G2 software products" do?

Search G2's software directory by free-text query. Returns matching products with slug, name, star rating, review count and description, deduplicated. The slug feeds g2.com/get_product. Whitespace in the query is normalised. No login required. Fails loudly rather than returning an empty list: G2 always degrades to fuzzy matches, so zero results means the page did not render.

### How do I automatically search G2 software products on g2.com?

Ask an AI agent connected to Reduck to run reduck/g2.com/search_products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/g2.com/search_products

### Is there a g2.com API to search G2 software products?

You do not need one. "Search G2 software products" drives the real g2.com pages in a browser, so it works whether or not g2.com offers an API for this.

### What information do I need to provide?

Required: query.

### What does it return?

It returns count, query, products.

### Do I need to be logged in to g2.com?

No. It only uses pages of g2.com that are reachable without signing in.

### Does it change anything on g2.com, or only read data?

It only reads. It looks things up on g2.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/g2.com/search_products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/g2.com/search_products

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/g2.com/search_products
