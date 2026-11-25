# Search emag.ro products

Automatically search emag.ro products on emag.ro. Search emag.ro by free-text query and return one page of results in emag's own order: the total result count, whether a next page exists, and the items (product id, offer id, product code, title, link, price in lei (RON), rating, review count, stock status). Results include sponsored products. Stop paging when has_next_page is false. Pass a product code or link to Get emag.ro product.

- Site: emag.ro
- Address: `reduck/emag.ro/search-products`
- Updated: 2026-11-24 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/emag.ro/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/emag.ro/search-products
```

## Input

- `query` (string, required): Free-text search, for example cablu usb. The site is in Romanian, so Romanian terms match best.
- `page` (integer, optional): Result page, 1 for the first. About 60 products per page.

## Output

- `page` (integer, required)
- `items` (array, required)
- `query` (string, required)
- `has_next_page` (boolean, required)
- `total_results` (integer | null, required): Number of products the site says match.

## FAQ

### What does "Search emag.ro products" do?

Search emag.ro by free-text query and return one page of results in emag's own order: the total result count, whether a next page exists, and the items (product id, offer id, product code, title, link, price in lei (RON), rating, review count, stock status). Results include sponsored products. Stop paging when has_next_page is false. Pass a product code or link to Get emag.ro product.

### How do I automatically search emag.ro products on emag.ro?

Ask an AI agent connected to Reduck to run reduck/emag.ro/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/emag.ro/search-products

### Is there a emag.ro API to search emag.ro products?

You do not need one. "Search emag.ro products" drives the real emag.ro pages in a browser, so it works whether or not emag.ro offers an API for this.

### What information do I need to provide?

Required: query. Optional: page.

### What does it return?

It returns page, items, query, has_next_page, total_results.

### Do I need to be logged in to emag.ro?

No. It only uses pages of emag.ro that are reachable without signing in.

### Does it change anything on emag.ro, or only read data?

It only reads. It looks things up on emag.ro and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/emag.ro/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/emag.ro/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/emag.ro/search-products
