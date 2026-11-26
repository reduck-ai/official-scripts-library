# Search GameStop products

Automatically search GameStop products on gamestop.com. Search GameStop products by keyword and return one page of results with prices, ratings and availability.

- Site: gamestop.com
- Address: `reduck/gamestop.com/search-products`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/gamestop.com/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/gamestop.com/search-products
```

## Input

- `query` (string, required)
- `page` (integer, optional)

## Output

- `page` (integer, required)
- `items` (array, required)
- `query` (string, required)
- `total_pages` (integer | null, required)
- `has_next_page` (boolean, required)
- `total_results` (integer | null, required)

## FAQ

### What does "Search GameStop products" do?

Search GameStop products by keyword and return one page of results with prices, ratings and availability.

### How do I automatically search GameStop products on gamestop.com?

Ask an AI agent connected to Reduck to run reduck/gamestop.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/gamestop.com/search-products

### Is there a gamestop.com API to search GameStop products?

You do not need one. "Search GameStop products" drives the real gamestop.com pages in a browser, so it works whether or not gamestop.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: page.

### What does it return?

It returns page, items, query, total_pages, has_next_page, total_results.

### Do I need to be logged in to gamestop.com?

No. It only uses pages of gamestop.com that are reachable without signing in.

### Does it change anything on gamestop.com, or only read data?

It only reads. It looks things up on gamestop.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/gamestop.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/gamestop.com/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/gamestop.com/search-products
