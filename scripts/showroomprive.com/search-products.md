# Search Showroomprivé products

Automatically search Showroomprivé products on showroomprive.com. Search showroomprive.com by keyword.

- Site: showroomprive.com
- Address: `reduck/showroomprive.com/search-products`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/showroomprive.com/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/showroomprive.com/search-products
```

## Input

- `query` (string, required): Search words, e.g. "sneakers nike". Searches the products of the sales open now.
- `page` (integer, optional): Results page, 40 products per page.

## Output

- `page` (integer, required)
- `items` (array, required)
- `query` (string, required)
- `total_pages` (integer, required)
- `has_next_page` (boolean, required)
- `total_results` (integer, required)

## FAQ

### What does "Search Showroomprivé products" do?

Search showroomprive.com by keyword.

### How do I automatically search Showroomprivé products on showroomprive.com?

Ask an AI agent connected to Reduck to run reduck/showroomprive.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/showroomprive.com/search-products

### Is there a showroomprive.com API to search Showroomprivé products?

You do not need one. "Search Showroomprivé products" drives the real showroomprive.com pages in a browser, so it works whether or not showroomprive.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: page.

### What does it return?

It returns page, items, query, total_pages, has_next_page, total_results.

### Do I need to be logged in to showroomprive.com?

No. It only uses pages of showroomprive.com that are reachable without signing in.

### Does it change anything on showroomprive.com, or only read data?

It only reads. It looks things up on showroomprive.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/showroomprive.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/showroomprive.com/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/showroomprive.com/search-products
