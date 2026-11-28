# Search SHEIN products

Automatically search SHEIN products on shein.com. Search SHEIN US (us.shein.com) products by keyword.

- Site: shein.com
- Address: `reduck/shein.com/search-products`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/shein.com/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/shein.com/search-products
```

## Input

- `query` (string, required): Free-text search, e.g. 'dress'.
- `page` (integer, optional): Results page (SHEIN shows about 20 per page on first load).

## Output

- `page` (integer, required)
- `items` (array, required)
- `query` (string, required)
- `has_next_page` (boolean, required)
- `total_results` (integer | null, required)

## FAQ

### What does "Search SHEIN products" do?

Search SHEIN US (us.shein.com) products by keyword.

### How do I automatically search SHEIN products on shein.com?

Ask an AI agent connected to Reduck to run reduck/shein.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/shein.com/search-products

### Is there a shein.com API to search SHEIN products?

You do not need one. "Search SHEIN products" drives the real shein.com pages in a browser, so it works whether or not shein.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: page.

### What does it return?

It returns page, items, query, has_next_page, total_results.

### Do I need to be logged in to shein.com?

No. It only uses pages of shein.com that are reachable without signing in.

### Does it change anything on shein.com, or only read data?

It only reads. It looks things up on shein.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/shein.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/shein.com/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/shein.com/search-products
