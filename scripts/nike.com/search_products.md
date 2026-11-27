# Search Nike products

Automatically search Nike products on nike.com. Search Nike.com products by free-text query. Returns query, count, and results (each with title, subtitle, url, price, fullPrice, styleColor, colorwayCount, imageUrl, messaging). Results are capped at 120 per call.

- Site: nike.com
- Address: `reduck/nike.com/search_products`
- Updated: 2026-11-25 (v7)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/nike.com/search_products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/nike.com/search_products
```

## Input

- `query` (string, required)
- `max` (integer, optional): Return at most this many products of the page (kept for older callers).
- `page` (integer, optional): Result page, 24 products per page. Nike loads results as you scroll; page N is results (N-1)*24+1 to N*24.

## Output

- `page` (integer, required)
- `count` (integer, required): Number of cards returned on this page.
- `query` (string, required)
- `results` (array, required)
- `has_next_page` (boolean, required)
- `total` (integer | null, optional): How many results Nike itself reports for this query. Nike matches loosely: a query it cannot match well still returns lower-relevance products and counts them here, so a non-zero total is not a promise that the products relate to the query.

## FAQ

### What does "Search Nike products" do?

Search Nike.com products by free-text query. Returns query, count, and results (each with title, subtitle, url, price, fullPrice, styleColor, colorwayCount, imageUrl, messaging). Results are capped at 120 per call.

### How do I automatically search Nike products on nike.com?

Ask an AI agent connected to Reduck to run reduck/nike.com/search_products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/nike.com/search_products

### Is there a nike.com API to search Nike products?

You do not need one. "Search Nike products" drives the real nike.com pages in a browser, so it works whether or not nike.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: max, page.

### What does it return?

It returns page, count, query, total, results, has_next_page.

### Do I need to be logged in to nike.com?

No. It only uses pages of nike.com that are reachable without signing in.

### Does it change anything on nike.com, or only read data?

It only reads. It looks things up on nike.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/nike.com/search_products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/nike.com/search_products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/nike.com/search_products
