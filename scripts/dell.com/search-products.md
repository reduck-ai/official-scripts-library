# Search Dell products

Automatically search Dell products on dell.com. Search the Dell US store and return one page of products with id, name, link, price, list price, rating and review count.

- Site: dell.com
- Address: `reduck/dell.com/search-products`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/dell.com/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/dell.com/search-products
```

## Input

- `query` (string, required): Words to search for, e.g. "xps 13".
- `page` (integer, optional): Results page, 1 for the first.

## Output

- `page` (integer, required)
- `items` (array, required)
- `query` (string, required)
- `total_pages` (integer | null, required)
- `has_next_page` (boolean, required)
- `total_results` (integer | null, required)

## FAQ

### What does "Search Dell products" do?

Search the Dell US store and return one page of products with id, name, link, price, list price, rating and review count.

### How do I automatically search Dell products on dell.com?

Ask an AI agent connected to Reduck to run reduck/dell.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/dell.com/search-products

### Is there a dell.com API to search Dell products?

You do not need one. "Search Dell products" drives the real dell.com pages in a browser, so it works whether or not dell.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: page.

### What does it return?

It returns page, items, query, total_pages, has_next_page, total_results.

### Do I need to be logged in to dell.com?

No. It only uses pages of dell.com that are reachable without signing in.

### Does it change anything on dell.com, or only read data?

It only reads. It looks things up on dell.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/dell.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/dell.com/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/dell.com/search-products
