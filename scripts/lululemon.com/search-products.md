# Search lululemon products

Automatically search lululemon products on lululemon.com. Search shop.lululemon.com by keyword.

- Site: lululemon.com
- Address: `reduck/lululemon.com/search-products`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/lululemon.com/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/lululemon.com/search-products
```

## Input

- `query` (string, required): Search words, e.g. "align leggings".
- `page` (integer, optional): Results page, 20 products per page.

## Output

- `page` (integer, required)
- `items` (array, required)
- `query` (string, required)
- `total_pages` (integer, required)
- `has_next_page` (boolean, required)
- `total_results` (integer, required)

## FAQ

### What does "Search lululemon products" do?

Search shop.lululemon.com by keyword.

### How do I automatically search lululemon products on lululemon.com?

Ask an AI agent connected to Reduck to run reduck/lululemon.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/lululemon.com/search-products

### Is there a lululemon.com API to search lululemon products?

You do not need one. "Search lululemon products" drives the real lululemon.com pages in a browser, so it works whether or not lululemon.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: page.

### What does it return?

It returns page, items, query, total_pages, has_next_page, total_results.

### Do I need to be logged in to lululemon.com?

No. It only uses pages of lululemon.com that are reachable without signing in.

### Does it change anything on lululemon.com, or only read data?

It only reads. It looks things up on lululemon.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/lululemon.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/lululemon.com/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/lululemon.com/search-products
