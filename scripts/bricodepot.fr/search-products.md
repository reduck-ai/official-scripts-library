# Search Brico Depot products

Automatically search Brico Depot products on bricodepot.fr. Search the Brico Depot catalogue (bricodepot.fr) by free text, with the site's sort orders and an optional category. Returns one page of 24 results: total result and page counts, has_next_page, and for each product its sku, name, link, price in euros (taxes included), struck-through price, price without tax, unit, brand, image, stock status and categories with their ids. Prices and stock depend on the depot: without a depot id the site's default prices are returned and stock quantity is null; pass a depot id from Search Brico Depot depots to get that depot's price and stock. Stop paging when has_next_page is false. A search with no match returns an empty list. A category id that the site rejects fails with an error that says so. Pass a sku to Get Brico Depot product.

- Site: bricodepot.fr
- Address: `reduck/bricodepot.fr/search-products`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/bricodepot.fr/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/bricodepot.fr/search-products
```

## Input

- `query` (string, required): Free-text search, for example "ruban adhésif".
- `page` (integer, optional): Result page, 24 products per page. Stop when has_next_page is false.
- `sort` (string, optional): Sort order of the results.
- `category` (string, optional): Category id to restrict the search to, taken from the categories of a result (for example ODk5MA== for Adhésif).
- `depot_id` (integer, optional): Depot whose price and stock to show, the depot_id returned by Search Brico Depot depots. Without it the site's default prices apply and stock is not reported.

## Output

- `page` (integer, required)
- `items` (array, required)
- `query` (string, required)
- `depot_id` (integer | null, required)
- `total_pages` (integer | null, required)
- `has_next_page` (boolean, required)
- `total_results` (integer | null, required)

## FAQ

### What does "Search Brico Depot products" do?

Search the Brico Depot catalogue (bricodepot.fr) by free text, with the site's sort orders and an optional category. Returns one page of 24 results: total result and page counts, has_next_page, and for each product its sku, name, link, price in euros (taxes included), struck-through price, price without tax, unit, brand, image, stock status and categories with their ids. Prices and stock depend on the depot: without a depot id the site's default prices are returned and stock quantity is null; pass a depot id from Search Brico Depot depots to get that depot's price and stock. Stop paging when has_next_page is false. A search with no match returns an empty list. A category id that the site rejects fails with an error that says so. Pass a sku to Get Brico Depot product.

### How do I automatically search Brico Depot products on bricodepot.fr?

Ask an AI agent connected to Reduck to run reduck/bricodepot.fr/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/bricodepot.fr/search-products

### Is there a bricodepot.fr API to search Brico Depot products?

You do not need one. "Search Brico Depot products" drives the real bricodepot.fr pages in a browser, so it works whether or not bricodepot.fr offers an API for this.

### What information do I need to provide?

Required: query. Optional: page, sort, category, depot_id.

### What does it return?

It returns page, items, query, depot_id, total_pages, has_next_page, total_results.

### Do I need to be logged in to bricodepot.fr?

No. It only uses pages of bricodepot.fr that are reachable without signing in.

### Does it change anything on bricodepot.fr, or only read data?

It only reads. It looks things up on bricodepot.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/bricodepot.fr/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/bricodepot.fr/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/bricodepot.fr/search-products
