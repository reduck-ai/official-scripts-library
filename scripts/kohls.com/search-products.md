# Search Kohl's products

Automatically search Kohl's products on kohls.com. Search Kohls.com by free-text query, 120 products a page plus the sponsored ones Kohl's mixes in (marked). Returns the total result count and pages, and for each product its id, link, name, current and regular price ranges in US dollars, price label, rating, review count, colors, whether it ships or can be picked up, and image. When nothing matches, Kohl's still shows products from a related department, and they are returned as the page shows them. Pass a product id to Get Kohl's product.

- Site: kohls.com
- Address: `reduck/kohls.com/search-products`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/kohls.com/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/kohls.com/search-products
```

## Input

- `query` (string, required): Free-text search, e.g. "towels".
- `page` (integer, optional): Result page, 120 products each (plus sponsored ones).

## Output

- `page` (integer, required)
- `items` (array, required)
- `query` (string, required)
- `total_pages` (integer | null, required)
- `total_results` (integer | null, required)
- `has_next_page` (boolean, optional)

## FAQ

### What does "Search Kohl's products" do?

Search Kohls.com by free-text query, 120 products a page plus the sponsored ones Kohl's mixes in (marked). Returns the total result count and pages, and for each product its id, link, name, current and regular price ranges in US dollars, price label, rating, review count, colors, whether it ships or can be picked up, and image. When nothing matches, Kohl's still shows products from a related department, and they are returned as the page shows them. Pass a product id to Get Kohl's product.

### How do I automatically search Kohl's products on kohls.com?

Ask an AI agent connected to Reduck to run reduck/kohls.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/kohls.com/search-products

### Is there a kohls.com API to search Kohl's products?

You do not need one. "Search Kohl's products" drives the real kohls.com pages in a browser, so it works whether or not kohls.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: page.

### What does it return?

It returns page, items, query, total_pages, has_next_page, total_results.

### Do I need to be logged in to kohls.com?

No. It only uses pages of kohls.com that are reachable without signing in.

### Does it change anything on kohls.com, or only read data?

It only reads. It looks things up on kohls.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/kohls.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/kohls.com/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/kohls.com/search-products
