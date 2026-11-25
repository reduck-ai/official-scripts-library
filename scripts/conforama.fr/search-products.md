# Search Conforama products

Automatically search Conforama products on conforama.fr. Search Conforama.fr by free-text query. Returns one page of results with the total result and page counts, has_next_page, the items (product id, name, url, price and struck-through list price in euros, eco-participation, rating, review count, image, marketplace flag, badges and main characteristics), the sort orders and the filters the site offers for this search, each with the id to pass back in sort or filters and its result count. A query that matches a category of the shop lists that category. Pass page for further pages and stop when has_next_page is false. Pass a product id or url from the items to Get Conforama product.

- Site: conforama.fr
- Address: `reduck/conforama.fr/search-products`
- Updated: 2026-11-24 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/conforama.fr/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/conforama.fr/search-products
```

## Input

- `query` (string, required): Free-text search, for example "table basse".
- `page` (integer, optional): Result page, starting at 1. Pages after the first take a second page load.
- `sort` (string, optional): Sort order id from the sorts of a previous search, such as /TW-4145 for price ascending. Leave out for the site's relevance order.
- `filters` (array, optional): Filter ids from the filters of a previous search, such as /NW-12689-vendu-par~conforama. Each one narrows the results.

## Output

- `page` (integer, required)
- `items` (array, required)
- `query` (string, required)
- `sorts` (array, required)
- `filters` (array, required)
- `total_pages` (integer | null, required)
- `has_next_page` (boolean, required)
- `total_results` (integer | null, required)
- `applied_filters` (array, optional)

## FAQ

### What does "Search Conforama products" do?

Search Conforama.fr by free-text query. Returns one page of results with the total result and page counts, has_next_page, the items (product id, name, url, price and struck-through list price in euros, eco-participation, rating, review count, image, marketplace flag, badges and main characteristics), the sort orders and the filters the site offers for this search, each with the id to pass back in sort or filters and its result count. A query that matches a category of the shop lists that category. Pass page for further pages and stop when has_next_page is false. Pass a product id or url from the items to Get Conforama product.

### How do I automatically search Conforama products on conforama.fr?

Ask an AI agent connected to Reduck to run reduck/conforama.fr/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/conforama.fr/search-products

### Is there a conforama.fr API to search Conforama products?

You do not need one. "Search Conforama products" drives the real conforama.fr pages in a browser, so it works whether or not conforama.fr offers an API for this.

### What information do I need to provide?

Required: query. Optional: page, sort, filters.

### What does it return?

It returns page, items, query, sorts, filters, total_pages, has_next_page, total_results, applied_filters.

### Do I need to be logged in to conforama.fr?

No. It only uses pages of conforama.fr that are reachable without signing in.

### Does it change anything on conforama.fr, or only read data?

It only reads. It looks things up on conforama.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/conforama.fr/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/conforama.fr/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/conforama.fr/search-products
