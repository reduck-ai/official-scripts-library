# Search Picard products

Automatically search Picard products on picard.fr. Search the products of the Picard France store (picard.fr, frozen food) by keyword, 48 products per page, in the order the site gives. For each product: its id (to pass to Get a Picard product or Add a product to the Picard cart), name, link, image, packaging, price in euros, price per kilo or per unit, rating, review count, promotion and categories, plus the total number of results. The prices are the national prices of the French web store, as shown to a guest who has not chosen a delivery postcode or a store. A search with no match, or a page past the end, returns an empty list.

- Site: picard.fr
- Address: `reduck/picard.fr/search-products`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/picard.fr/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/picard.fr/search-products
```

## Input

- `query` (string, required): Words to search for, as typed in the site's search box (for example "pizza").
- `page` (integer, optional): Results page, from 1. Each page holds up to 48 products.

## Output

- `url` (string, required): The page the site showed.
- `page` (integer, required)
- `query` (string, required)
- `total` (integer | null, required): Number of results the site states for the search, or null when the page states none (no match, or a page past the end).
- `hasMore` (boolean, required): True when a next page has products.
- `products` (array, required)

## FAQ

### What does "Search Picard products" do?

Search the products of the Picard France store (picard.fr, frozen food) by keyword, 48 products per page, in the order the site gives. For each product: its id (to pass to Get a Picard product or Add a product to the Picard cart), name, link, image, packaging, price in euros, price per kilo or per unit, rating, review count, promotion and categories, plus the total number of results. The prices are the national prices of the French web store, as shown to a guest who has not chosen a delivery postcode or a store. A search with no match, or a page past the end, returns an empty list.

### How do I automatically search Picard products on picard.fr?

Ask an AI agent connected to Reduck to run reduck/picard.fr/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/picard.fr/search-products

### Is there a picard.fr API to search Picard products?

You do not need one. "Search Picard products" drives the real picard.fr pages in a browser, so it works whether or not picard.fr offers an API for this.

### What information do I need to provide?

Required: query. Optional: page.

### What does it return?

It returns url, page, query, total, hasMore, products.

### Do I need to be logged in to picard.fr?

No. It only uses pages of picard.fr that are reachable without signing in.

### Does it change anything on picard.fr, or only read data?

It only reads. It looks things up on picard.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/picard.fr/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/picard.fr/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/picard.fr/search-products
