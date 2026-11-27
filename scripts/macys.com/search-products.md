# Search Macy's products

Automatically search Macy's products on macys.com. Search Macys.com by free-text query, one page at a time: total results and pages, has_next_page, and for each product its id, name, brand, link, price and regular price in US dollars, the price text and deal label Macy's shows, rating, review count and image. A page past the last returns an empty list. Pass a product id or link to Get Macy's product.

- Site: macys.com
- Address: `reduck/macys.com/search-products`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/macys.com/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/macys.com/search-products
```

## Input

- `query` (string, required): Free-text search, e.g. "towels".
- `page` (integer, optional)

## Output

- `page` (integer, required)
- `items` (array, required)
- `query` (string, required)
- `has_next_page` (boolean, required)
- `total_results` (integer | null, required)
- `total_pages` (integer | null, optional)

## FAQ

### What does "Search Macy's products" do?

Search Macys.com by free-text query, one page at a time: total results and pages, has_next_page, and for each product its id, name, brand, link, price and regular price in US dollars, the price text and deal label Macy's shows, rating, review count and image. A page past the last returns an empty list. Pass a product id or link to Get Macy's product.

### How do I automatically search Macy's products on macys.com?

Ask an AI agent connected to Reduck to run reduck/macys.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/macys.com/search-products

### Is there a macys.com API to search Macy's products?

You do not need one. "Search Macy's products" drives the real macys.com pages in a browser, so it works whether or not macys.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: page.

### What does it return?

It returns page, items, query, total_pages, has_next_page, total_results.

### Do I need to be logged in to macys.com?

No. It only uses pages of macys.com that are reachable without signing in.

### Does it change anything on macys.com, or only read data?

It only reads. It looks things up on macys.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/macys.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/macys.com/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/macys.com/search-products
