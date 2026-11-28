# Search Cultura products

Automatically search Cultura products on cultura.com. Search cultura.com by keyword.

- Site: cultura.com
- Address: `reduck/cultura.com/search-products`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/cultura.com/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/cultura.com/search-products
```

## Input

- `query` (string, required): Search words, e.g. "harry potter".
- `page` (integer, optional): Results page, 40 products per page.

## Output

- `page` (integer, required)
- `items` (array, required)
- `query` (string, required)
- `total_pages` (integer, required)
- `has_next_page` (boolean, required)
- `total_results` (integer, required)

## FAQ

### What does "Search Cultura products" do?

Search cultura.com by keyword.

### How do I automatically search Cultura products on cultura.com?

Ask an AI agent connected to Reduck to run reduck/cultura.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/cultura.com/search-products

### Is there a cultura.com API to search Cultura products?

You do not need one. "Search Cultura products" drives the real cultura.com pages in a browser, so it works whether or not cultura.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: page.

### What does it return?

It returns page, items, query, total_pages, has_next_page, total_results.

### Do I need to be logged in to cultura.com?

No. It only uses pages of cultura.com that are reachable without signing in.

### Does it change anything on cultura.com, or only read data?

It only reads. It looks things up on cultura.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/cultura.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/cultura.com/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/cultura.com/search-products
