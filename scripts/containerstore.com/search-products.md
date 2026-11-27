# Search Container Store products

Automatically search Container Store products on containerstore.com. Search The Container Store (containerstore.com, US) products by keywords, 60 a page: id, name, link, price text and lowest price in USD, list price, rating, colors and stock flag of each, plus the total count and the number of pages. A search with no match gives an empty list, and so does a page past the last one.

- Site: containerstore.com
- Address: `reduck/containerstore.com/search-products`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/containerstore.com/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/containerstore.com/search-products
```

## Input

- `query` (string, required): Keywords, for example "bin".
- `page` (integer, optional): Results page, 60 products a page.

## Output

- `page` (integer, required)
- `query` (string, required)
- `total` (integer | null, required): Number of products that match, on all pages.
- `products` (array, required)
- `last_page` (integer | null, optional)
- `did_you_mean` (string | null, optional)
- `redirect_url` (string | null, optional): The page the site sends these keywords to, when it does.

## FAQ

### What does "Search Container Store products" do?

Search The Container Store (containerstore.com, US) products by keywords, 60 a page: id, name, link, price text and lowest price in USD, list price, rating, colors and stock flag of each, plus the total count and the number of pages. A search with no match gives an empty list, and so does a page past the last one.

### How do I automatically search Container Store products on containerstore.com?

Ask an AI agent connected to Reduck to run reduck/containerstore.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/containerstore.com/search-products

### Is there a containerstore.com API to search Container Store products?

You do not need one. "Search Container Store products" drives the real containerstore.com pages in a browser, so it works whether or not containerstore.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: page.

### What does it return?

It returns page, query, total, products, last_page, did_you_mean, redirect_url.

### Do I need to be logged in to containerstore.com?

No. It only uses pages of containerstore.com that are reachable without signing in.

### Does it change anything on containerstore.com, or only read data?

It only reads. It looks things up on containerstore.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/containerstore.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/containerstore.com/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/containerstore.com/search-products
