# Search Nike products

Automatically search Nike products on nike.com. Search Nike.com products by free-text query. Returns query, count, and results (each with title, subtitle, url, price, fullPrice, styleColor, colorwayCount, imageUrl, messaging). Results are capped at 120 per call.

- Site: nike.com
- Address: `reduck/nike.com/search_products`
- Updated: 2026-09-11 (v5)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/nike.com/search_products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/nike.com/search_products
```

## Input

- `query` (string, required)
- `max` (integer, optional)

## Output

- `count` (integer, required): Number of cards returned in results, capped by max.
- `query` (string, required)
- `results` (array, required)
- `total` (integer | null, optional): How many results Nike itself reports for this query, which can be far larger than count. Nike matches loosely: a query it cannot match well still returns lower-relevance products and counts them here as results, so a non-zero total is not a promise that the products relate to the query.

## FAQ

### What does "Search Nike products" do?

Search Nike.com products by free-text query. Returns query, count, and results (each with title, subtitle, url, price, fullPrice, styleColor, colorwayCount, imageUrl, messaging). Results are capped at 120 per call.

### How do I automatically search Nike products on nike.com?

Ask an AI agent connected to Reduck to run reduck/nike.com/search_products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/nike.com/search_products

### Is there a nike.com API to search Nike products?

You do not need one. "Search Nike products" drives the real nike.com pages in a browser, so it works whether or not nike.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: max.

### What does it return?

It returns count, query, total, results.

### Do I need to be logged in to nike.com?

No. It only uses pages of nike.com that are reachable without signing in.

### Does it change anything on nike.com, or only read data?

It only reads. It looks things up on nike.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/nike.com/search_products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/nike.com/search_products

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/nike.com/search_products
