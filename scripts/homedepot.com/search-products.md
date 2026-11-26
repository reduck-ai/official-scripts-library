# Search Home Depot products

Automatically search Home Depot products on homedepot.com. Search HomeDepot.com (US) products by free-text query, one page at a time.

- Site: homedepot.com
- Address: `reduck/homedepot.com/search-products`
- Updated: 2026-11-25 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/homedepot.com/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/homedepot.com/search-products
```

## Input

- `query` (string, required): Free-text search, e.g. "cordless drill".
- `page` (integer, optional): Result page, 24 products per page.

## Output

- `page` (integer, required)
- `query` (string, required)
- `products` (array, required)
- `url` (string, optional)
- `total` (integer | null, optional)

## FAQ

### What does "Search Home Depot products" do?

Search HomeDepot.com (US) products by free-text query, one page at a time.

### How do I automatically search Home Depot products on homedepot.com?

Ask an AI agent connected to Reduck to run reduck/homedepot.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/homedepot.com/search-products

### Is there a homedepot.com API to search Home Depot products?

You do not need one. "Search Home Depot products" drives the real homedepot.com pages in a browser, so it works whether or not homedepot.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: page.

### What does it return?

It returns url, page, query, total, products.

### Do I need to be logged in to homedepot.com?

No. It only uses pages of homedepot.com that are reachable without signing in.

### Does it change anything on homedepot.com, or only read data?

It only reads. It looks things up on homedepot.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/homedepot.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/homedepot.com/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/homedepot.com/search-products
