# Search L.L.Bean products

Automatically search L.L.Bean products on llbean.com. Search L.L.Bean (llbean.com, US) products by keywords, 48 a page: id, name, link, price range in USD, rating, colors and stock status of each, plus the total count. For some keywords L.L.Bean opens a category page instead of a search page: the results are then that category's products, and category_url gives its link. A search with no match gives an empty list; a page past the last one gives an empty list too.

- Site: llbean.com
- Address: `reduck/llbean.com/search-products`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/llbean.com/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/llbean.com/search-products
```

## Input

- `query` (string, required): Keywords, for example "wool socks".
- `page` (integer, optional): Results page, 48 products a page.

## Output

- `page` (integer, required)
- `query` (string, required)
- `total` (integer | null, required): Number of products that match, on all pages.
- `products` (array, required)
- `category_url` (string | null, optional): The category page L.L.Bean opened for these keywords, or null when it showed a search page.

## FAQ

### What does "Search L.L.Bean products" do?

Search L.L.Bean (llbean.com, US) products by keywords, 48 a page: id, name, link, price range in USD, rating, colors and stock status of each, plus the total count. For some keywords L.L.Bean opens a category page instead of a search page: the results are then that category's products, and category_url gives its link. A search with no match gives an empty list; a page past the last one gives an empty list too.

### How do I automatically search L.L.Bean products on llbean.com?

Ask an AI agent connected to Reduck to run reduck/llbean.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/llbean.com/search-products

### Is there a llbean.com API to search L.L.Bean products?

You do not need one. "Search L.L.Bean products" drives the real llbean.com pages in a browser, so it works whether or not llbean.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: page.

### What does it return?

It returns page, query, total, products, category_url.

### Do I need to be logged in to llbean.com?

No. It only uses pages of llbean.com that are reachable without signing in.

### Does it change anything on llbean.com, or only read data?

It only reads. It looks things up on llbean.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/llbean.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/llbean.com/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/llbean.com/search-products
