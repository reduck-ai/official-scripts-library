# Search AutoZone products

Automatically search AutoZone products on autozone.com. Search the AutoZone catalogue by keyword or part number and return one page of 24 products with price, rating, brand, part number and stock, as the site's search page lists them.

- Site: autozone.com
- Address: `reduck/autozone.com/search-products`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/autozone.com/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/autozone.com/search-products
```

## Input

- `query` (string, required): Search text: keywords ("oil filter") or a part number ("S16XL").
- `page` (integer, optional): Result page, 24 products per page.

## Output

- `page` (integer, required)
- `items` (array, required)
- `query` (string, required)
- `total_pages` (integer | null, required)
- `has_next_page` (boolean, required)
- `total_results` (integer, required)
- `redirect_url` (string | null, optional): The page the site opens instead of a result list (for example a product id), or null.
- `corrected_query` (string | null, optional): The text the site searched instead, when it corrected the query.

## FAQ

### What does "Search AutoZone products" do?

Search the AutoZone catalogue by keyword or part number and return one page of 24 products with price, rating, brand, part number and stock, as the site's search page lists them.

### How do I automatically search AutoZone products on autozone.com?

Ask an AI agent connected to Reduck to run reduck/autozone.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/autozone.com/search-products

### Is there a autozone.com API to search AutoZone products?

You do not need one. "Search AutoZone products" drives the real autozone.com pages in a browser, so it works whether or not autozone.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: page.

### What does it return?

It returns page, items, query, total_pages, redirect_url, has_next_page, total_results, corrected_query.

### Do I need to be logged in to autozone.com?

No. It only uses pages of autozone.com that are reachable without signing in.

### Does it change anything on autozone.com, or only read data?

It only reads. It looks things up on autozone.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/autozone.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/autozone.com/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/autozone.com/search-products
