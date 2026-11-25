# Search Castorama products

Automatically search Castorama products on castorama.fr. Search castorama.fr by free-text query, with the site's own sort orders and filters (brand, type, seller, delivery option, price band, rating and the product attributes of the category). Returns one page of about 48 results: total result count, current page and has_next_page, the items (product id, name, link, price and struck-through list price in euros, rating, review count, seller, availability, image) and the filters and sort orders the page offers, each with the value to pass back. Prices are those shown to this browser, which can depend on the store or postcode chosen on the site. A search that matches a category opens that category's product list. Stop paging when has_next_page is false. Pass a product id or link to Get Castorama product.

- Site: castorama.fr
- Address: `reduck/castorama.fr/search-products`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/castorama.fr/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/castorama.fr/search-products
```

## Input

- `query` (string, required): Free-text search, for example perceuse sans fil.
- `page` (integer, optional): Result page, starting at 1. Stop when has_next_page is false.
- `sort` (string | null, optional): A sort value from the sorts of a previous result, for example product.price for ascending price. Leave empty for the site's relevance order.
- `filters` (array, optional): Filters to apply, each one exactly as the param of a filter value of a previous result (for example Vendu+par=Castorama). Several filters combine.

## Output

- `page` (integer, required)
- `items` (array, required)
- `has_next_page` (boolean, required)
- `query` (string, optional)
- `sorts` (array, optional)
- `filters` (array, optional)
- `page_size` (integer | null, optional)
- `total_results` (integer | null, optional)

## FAQ

### What does "Search Castorama products" do?

Search castorama.fr by free-text query, with the site's own sort orders and filters (brand, type, seller, delivery option, price band, rating and the product attributes of the category). Returns one page of about 48 results: total result count, current page and has_next_page, the items (product id, name, link, price and struck-through list price in euros, rating, review count, seller, availability, image) and the filters and sort orders the page offers, each with the value to pass back. Prices are those shown to this browser, which can depend on the store or postcode chosen on the site. A search that matches a category opens that category's product list. Stop paging when has_next_page is false. Pass a product id or link to Get Castorama product.

### How do I automatically search Castorama products on castorama.fr?

Ask an AI agent connected to Reduck to run reduck/castorama.fr/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/castorama.fr/search-products

### Is there a castorama.fr API to search Castorama products?

You do not need one. "Search Castorama products" drives the real castorama.fr pages in a browser, so it works whether or not castorama.fr offers an API for this.

### What information do I need to provide?

Required: query. Optional: page, sort, filters.

### What does it return?

It returns page, items, query, sorts, filters, page_size, has_next_page, total_results.

### Do I need to be logged in to castorama.fr?

No. It only uses pages of castorama.fr that are reachable without signing in.

### Does it change anything on castorama.fr, or only read data?

It only reads. It looks things up on castorama.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/castorama.fr/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/castorama.fr/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/castorama.fr/search-products
