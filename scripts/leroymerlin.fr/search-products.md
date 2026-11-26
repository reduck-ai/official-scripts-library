# Search Leroy Merlin products

Automatically search Leroy Merlin products on leroymerlin.fr. Search leroymerlin.fr by free-text query, with the site's sort order, one page at a time of about 48 products. Returns the page number, the page count, has_next_page, the result count the site shows (it stops counting at 10000), and for each product its reference, offer id, name, brand, link, price in euros, rating, review count, seller and image. Prices are those the site shows for the browser's current store, or the online price when no store is chosen. Stop paging when has_next_page is false. Pass the link to Get Leroy Merlin product or Add Leroy Merlin product to cart.

- Site: leroymerlin.fr
- Address: `reduck/leroymerlin.fr/search-products`
- Updated: 2026-11-24 (v6)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/leroymerlin.fr/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/leroymerlin.fr/search-products
```

## Input

- `query` (string, required): Free-text search, for example vis a bois.
- `page` (integer, optional): Result page, starting at 1. Stop when has_next_page is false.
- `sort` (string, optional): Sort order of the site: relevance, lowest price first or highest price first.

## Output

- `page` (integer, required)
- `items` (array, required)
- `query` (string, required)
- `page_count` (integer | null, required)
- `has_next_page` (boolean, required)
- `sort` (string | null, optional): Sort order the page applied.
- `total_results` (integer | null, optional): Result count the site shows, capped at 10000.

## FAQ

### What does "Search Leroy Merlin products" do?

Search leroymerlin.fr by free-text query, with the site's sort order, one page at a time of about 48 products. Returns the page number, the page count, has_next_page, the result count the site shows (it stops counting at 10000), and for each product its reference, offer id, name, brand, link, price in euros, rating, review count, seller and image. Prices are those the site shows for the browser's current store, or the online price when no store is chosen. Stop paging when has_next_page is false. Pass the link to Get Leroy Merlin product or Add Leroy Merlin product to cart.

### How do I automatically search Leroy Merlin products on leroymerlin.fr?

Ask an AI agent connected to Reduck to run reduck/leroymerlin.fr/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/leroymerlin.fr/search-products

### Is there a leroymerlin.fr API to search Leroy Merlin products?

You do not need one. "Search Leroy Merlin products" drives the real leroymerlin.fr pages in a browser, so it works whether or not leroymerlin.fr offers an API for this.

### What information do I need to provide?

Required: query. Optional: page, sort.

### What does it return?

It returns page, sort, items, query, page_count, has_next_page, total_results.

### Do I need to be logged in to leroymerlin.fr?

No. It only uses pages of leroymerlin.fr that are reachable without signing in.

### Does it change anything on leroymerlin.fr, or only read data?

It only reads. It looks things up on leroymerlin.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/leroymerlin.fr/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/leroymerlin.fr/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/leroymerlin.fr/search-products
