# Search Galeries Lafayette products

Automatically search Galeries Lafayette products on galerieslafayette.com. Search galerieslafayette.com by keyword.

- Site: galerieslafayette.com
- Address: `reduck/galerieslafayette.com/search-products`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/galerieslafayette.com/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/galerieslafayette.com/search-products
```

## Input

- `query` (string, required): Search words, e.g. "sac cuir".
- `page` (integer, optional): Results page, 48 products per page.

## Output

- `page` (integer, required)
- `items` (array, required)
- `query` (string, required)
- `total_pages` (integer, required)
- `has_next_page` (boolean, required)
- `total_results` (integer, required)

## FAQ

### What does "Search Galeries Lafayette products" do?

Search galerieslafayette.com by keyword.

### How do I automatically search Galeries Lafayette products on galerieslafayette.com?

Ask an AI agent connected to Reduck to run reduck/galerieslafayette.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/galerieslafayette.com/search-products

### Is there a galerieslafayette.com API to search Galeries Lafayette products?

You do not need one. "Search Galeries Lafayette products" drives the real galerieslafayette.com pages in a browser, so it works whether or not galerieslafayette.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: page.

### What does it return?

It returns page, items, query, total_pages, has_next_page, total_results.

### Do I need to be logged in to galerieslafayette.com?

No. It only uses pages of galerieslafayette.com that are reachable without signing in.

### Does it change anything on galerieslafayette.com, or only read data?

It only reads. It looks things up on galerieslafayette.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/galerieslafayette.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/galerieslafayette.com/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/galerieslafayette.com/search-products
