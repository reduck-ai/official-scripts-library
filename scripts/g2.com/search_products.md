# Search G2 software products

Automatically search G2 software products on g2.com. Search G2's software directory by free-text query, one result page at a time (page arg). Returns the products G2 lists for the query with slug, name, star rating, review count and description, deduplicated. The slug feeds g2.com/get_product. Whitespace in the query is normalised. No login required. A query G2 has no product for returns an empty list.

- Site: g2.com
- Address: `reduck/g2.com/search_products`
- Updated: 2026-10-28 (v8)
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
- `page` (integer, optional): Result page, as G2's own pager numbers it.

## Output

- `count` (integer, required)
- `query` (string, required): The normalised query actually searched.
- `products` (array, required): Empty when G2 lists no product for the query.
- `page` (integer, optional)

## FAQ

### What does "Search G2 software products" do?

Search G2's software directory by free-text query, one result page at a time (page arg). Returns the products G2 lists for the query with slug, name, star rating, review count and description, deduplicated. The slug feeds g2.com/get_product. Whitespace in the query is normalised. No login required. A query G2 has no product for returns an empty list.

### How do I automatically search G2 software products on g2.com?

Ask an AI agent connected to Reduck to run reduck/g2.com/search_products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/g2.com/search_products

### Is there a g2.com API to search G2 software products?

You do not need one. "Search G2 software products" drives the real g2.com pages in a browser, so it works whether or not g2.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: page.

### What does it return?

It returns page, count, query, products.

### Do I need to be logged in to g2.com?

No. It only uses pages of g2.com that are reachable without signing in.

### Does it change anything on g2.com, or only read data?

It only reads. It looks things up on g2.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/g2.com/search_products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/g2.com/search_products

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/g2.com/search_products
