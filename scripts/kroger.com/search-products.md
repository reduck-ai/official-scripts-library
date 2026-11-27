# Search Kroger products

Automatically search Kroger products on kroger.com. Search Kroger.com by free-text query, one page at a time (24 results a page, plus sponsored ones, marked). Returns the total count, the store whose prices are shown, and for each product its UPC, link, name, brand, size, price in US dollars, regular price when on sale, unit price text, rating, review count and image. A query with no match, or a page past the last, returns an empty list. Pass a UPC to Get Kroger product.

- Site: kroger.com
- Address: `reduck/kroger.com/search-products`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/kroger.com/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/kroger.com/search-products
```

## Input

- `query` (string, required): Free-text search, e.g. "milk".
- `page` (integer, optional)

## Output

- `page` (integer, required)
- `items` (array, required)
- `query` (string, required)
- `total_results` (integer | null, required)
- `location_id` (string | null, optional)

## FAQ

### What does "Search Kroger products" do?

Search Kroger.com by free-text query, one page at a time (24 results a page, plus sponsored ones, marked). Returns the total count, the store whose prices are shown, and for each product its UPC, link, name, brand, size, price in US dollars, regular price when on sale, unit price text, rating, review count and image. A query with no match, or a page past the last, returns an empty list. Pass a UPC to Get Kroger product.

### How do I automatically search Kroger products on kroger.com?

Ask an AI agent connected to Reduck to run reduck/kroger.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/kroger.com/search-products

### Is there a kroger.com API to search Kroger products?

You do not need one. "Search Kroger products" drives the real kroger.com pages in a browser, so it works whether or not kroger.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: page.

### What does it return?

It returns page, items, query, location_id, total_results.

### Do I need to be logged in to kroger.com?

No. It only uses pages of kroger.com that are reachable without signing in.

### Does it change anything on kroger.com, or only read data?

It only reads. It looks things up on kroger.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/kroger.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/kroger.com/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/kroger.com/search-products
