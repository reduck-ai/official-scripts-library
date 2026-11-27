# Search Carrefour products

Automatically search Carrefour products on carrefour.fr. Search Carrefour.fr by free-text query, one page of 30 at a time: total results and pages, has_next_page, and for each product its barcode number, title, brand, link, price in euros and unit price, availability, category, image, whether Carrefour or a marketplace seller sells it, and how many other offers it has. A page past the last returns an empty list. Pass the barcode number to Get Carrefour product.

- Site: carrefour.fr
- Address: `reduck/carrefour.fr/search-products`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/carrefour.fr/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/carrefour.fr/search-products
```

## Input

- `query` (string, required): Free-text search, e.g. "lait".
- `page` (integer, optional): Results page, from 1.

## Output

- `page` (integer, required)
- `items` (array, required)
- `query` (string, required)
- `has_next_page` (boolean, required)
- `total_results` (integer | null, required)
- `total_pages` (integer | null, optional)

## FAQ

### What does "Search Carrefour products" do?

Search Carrefour.fr by free-text query, one page of 30 at a time: total results and pages, has_next_page, and for each product its barcode number, title, brand, link, price in euros and unit price, availability, category, image, whether Carrefour or a marketplace seller sells it, and how many other offers it has. A page past the last returns an empty list. Pass the barcode number to Get Carrefour product.

### How do I automatically search Carrefour products on carrefour.fr?

Ask an AI agent connected to Reduck to run reduck/carrefour.fr/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/carrefour.fr/search-products

### Is there a carrefour.fr API to search Carrefour products?

You do not need one. "Search Carrefour products" drives the real carrefour.fr pages in a browser, so it works whether or not carrefour.fr offers an API for this.

### What information do I need to provide?

Required: query. Optional: page.

### What does it return?

It returns page, items, query, total_pages, has_next_page, total_results.

### Do I need to be logged in to carrefour.fr?

No. It only uses pages of carrefour.fr that are reachable without signing in.

### Does it change anything on carrefour.fr, or only read data?

It only reads. It looks things up on carrefour.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/carrefour.fr/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/carrefour.fr/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/carrefour.fr/search-products
