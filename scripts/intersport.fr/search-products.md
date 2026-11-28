# Search Intersport products

Automatically search Intersport products on intersport.fr. Search intersport.fr by keyword.

- Site: intersport.fr
- Address: `reduck/intersport.fr/search-products`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/intersport.fr/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/intersport.fr/search-products
```

## Input

- `query` (string, required): Search words, e.g. "chaussures running".
- `page` (integer, optional): Results page, 40 products per page.

## Output

- `page` (integer, required)
- `items` (array, required)
- `query` (string, required)
- `total_pages` (integer, required)
- `has_next_page` (boolean, required)
- `total_results` (integer, required)

## FAQ

### What does "Search Intersport products" do?

Search intersport.fr by keyword.

### How do I automatically search Intersport products on intersport.fr?

Ask an AI agent connected to Reduck to run reduck/intersport.fr/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/intersport.fr/search-products

### Is there a intersport.fr API to search Intersport products?

You do not need one. "Search Intersport products" drives the real intersport.fr pages in a browser, so it works whether or not intersport.fr offers an API for this.

### What information do I need to provide?

Required: query. Optional: page.

### What does it return?

It returns page, items, query, total_pages, has_next_page, total_results.

### Do I need to be logged in to intersport.fr?

No. It only uses pages of intersport.fr that are reachable without signing in.

### Does it change anything on intersport.fr, or only read data?

It only reads. It looks things up on intersport.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/intersport.fr/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/intersport.fr/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/intersport.fr/search-products
