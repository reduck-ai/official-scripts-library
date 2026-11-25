# Search Decathlon products

Automatically search Decathlon products on decathlon.fr. Search Decathlon.fr (French sports retailer and marketplace) by free-text query, with the site's own sort orders and filters. Returns one page of 40 results: the total number of results, the page count and has_next_page, then for each product its sku id, title, link, brand, price and struck-through list price in euros, discount, rating, review count, image, the seller (Decathlon or a marketplace seller), the sizes on offer and whether it can be bought online. Also returns the filters that apply and the filters the page offers for this search (brand, color, size, sport, seller and the product's own attributes), each value with its result count and the facet to pass back in facets. A query with no match gives an empty list. Pass a link to Get Decathlon product or Add Decathlon product to cart.

- Site: decathlon.fr
- Address: `reduck/decathlon.fr/search-products`
- Updated: 2026-11-24 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/decathlon.fr/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/decathlon.fr/search-products
```

## Input

- `query` (string, required): Free-text search, for example "ballon de football".
- `page` (integer, optional): Page of results, 40 per page, starting at 1. Stop when has_next_page is false.
- `sort` (string, optional): Sort order of the site: relevance, price ascending, price descending, biggest discount, best rated.
- `facets` (array, optional): Filters to apply, each one a facet string taken from the filters of an earlier search (for example "brands:ADIDAS_"). Several are combined.

## Output

- `page` (integer, required)
- `items` (array, required)
- `query` (string, required)
- `filters` (array, required)
- `total_pages` (integer | null, required)
- `has_next_page` (boolean, required)
- `total_results` (integer | null, required)
- `applied_filters` (array, required)

## FAQ

### What does "Search Decathlon products" do?

Search Decathlon.fr (French sports retailer and marketplace) by free-text query, with the site's own sort orders and filters. Returns one page of 40 results: the total number of results, the page count and has_next_page, then for each product its sku id, title, link, brand, price and struck-through list price in euros, discount, rating, review count, image, the seller (Decathlon or a marketplace seller), the sizes on offer and whether it can be bought online. Also returns the filters that apply and the filters the page offers for this search (brand, color, size, sport, seller and the product's own attributes), each value with its result count and the facet to pass back in facets. A query with no match gives an empty list. Pass a link to Get Decathlon product or Add Decathlon product to cart.

### How do I automatically search Decathlon products on decathlon.fr?

Ask an AI agent connected to Reduck to run reduck/decathlon.fr/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/decathlon.fr/search-products

### Is there a decathlon.fr API to search Decathlon products?

You do not need one. "Search Decathlon products" drives the real decathlon.fr pages in a browser, so it works whether or not decathlon.fr offers an API for this.

### What information do I need to provide?

Required: query. Optional: page, sort, facets.

### What does it return?

It returns page, items, query, filters, total_pages, has_next_page, total_results, applied_filters.

### Do I need to be logged in to decathlon.fr?

No. It only uses pages of decathlon.fr that are reachable without signing in.

### Does it change anything on decathlon.fr, or only read data?

It only reads. It looks things up on decathlon.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/decathlon.fr/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/decathlon.fr/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/decathlon.fr/search-products
