# Search Intermarché products

Automatically search Intermarché products on intermarche.com. Search Intermarché.com in one store (Intermarché prices and stock are per store) by free-text query, 40 products per page: total results and pages, has_next_page, and for each product its id, barcode number, title, brand, price in euros and unit price, availability and image. The store is its 5-digit code, as the store's page on intermarche.com shows it (for example 09571). A page past the last returns an empty list.

- Site: intermarche.com
- Address: `reduck/intermarche.com/search-products`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/intermarche.com/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/intermarche.com/search-products
```

## Input

- `query` (string, required): Free-text search, e.g. "lait".
- `store` (string, required): Store code, 5 digits, e.g. 09571.
- `page` (integer, optional)

## Output

- `page` (integer, required)
- `items` (array, required)
- `query` (string, required)
- `store` (string, required)
- `has_next_page` (boolean, required)
- `total_results` (integer | null, required)
- `total_pages` (integer | null, optional)

## FAQ

### What does "Search Intermarché products" do?

Search Intermarché.com in one store (Intermarché prices and stock are per store) by free-text query, 40 products per page: total results and pages, has_next_page, and for each product its id, barcode number, title, brand, price in euros and unit price, availability and image. The store is its 5-digit code, as the store's page on intermarche.com shows it (for example 09571). A page past the last returns an empty list.

### How do I automatically search Intermarché products on intermarche.com?

Ask an AI agent connected to Reduck to run reduck/intermarche.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/intermarche.com/search-products

### Is there a intermarche.com API to search Intermarché products?

You do not need one. "Search Intermarché products" drives the real intermarche.com pages in a browser, so it works whether or not intermarche.com offers an API for this.

### What information do I need to provide?

Required: query, store. Optional: page.

### What does it return?

It returns page, items, query, store, total_pages, has_next_page, total_results.

### Do I need to be logged in to intermarche.com?

No. It only uses pages of intermarche.com that are reachable without signing in.

### Does it change anything on intermarche.com, or only read data?

It only reads. It looks things up on intermarche.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/intermarche.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/intermarche.com/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/intermarche.com/search-products
