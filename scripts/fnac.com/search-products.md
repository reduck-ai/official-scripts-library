# Search Fnac products

Automatically search Fnac products on fnac.com. Search Fnac.com by free-text query, with Fnac's own sort order and filters (price band, brand, sold by Fnac and the product's attributes). Returns one page of 20 results: the total result and page counts, has_next_page, the items (id, title, url, price, list_price, rating, review_count, image_url, brand, seller, seller_type, condition, availability as Fnac writes it, badges such as Black Friday, and the number of other offers shown under the card), and the filters the page offers for this search, each value with the id to pass back in filters. Prices are in euros. Results include marketplace sellers. A search with no match gives an empty items list with total_results 0, and a page past the last one gives an empty list too. Pass an id to Get Fnac product.

- Site: fnac.com
- Address: `reduck/fnac.com/search-products`
- Updated: 2026-11-27 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/fnac.com/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/fnac.com/search-products
```

## Input

- `query` (string, required): Free-text search query.
- `page` (integer, optional): Result page, 20 results a page. has_next_page and total_pages say when to stop.
- `sort` (string, optional): Sort order: relevance (the default), price_asc (lowest price first), price_desc (highest price first), best_sellers, rating (customer rating).
- `filters` (array, optional): Filter ids from the filters of an earlier result for the same query, for example "20 à 50€!attributes.price_range" (a price band), "JBL!attributes.brand__Marque" (a brand) or "1!13" (sold by Fnac). Values of one filter are alternatives; different filters all apply.

## Output

- `url` (string, required)
- `page` (integer, required)
- `items` (array, required): The results in page order.
- `query` (string, required)
- `filters` (array, required): Filters the page offers for this search, in page order.
- `total_pages` (integer | null, required)
- `has_next_page` (boolean, required)
- `total_results` (integer | null, required): Number of products that match, as Fnac states it.
- `applied_filters` (array, required)

## FAQ

### What does "Search Fnac products" do?

Search Fnac.com by free-text query, with Fnac's own sort order and filters (price band, brand, sold by Fnac and the product's attributes). Returns one page of 20 results: the total result and page counts, has_next_page, the items (id, title, url, price, list_price, rating, review_count, image_url, brand, seller, seller_type, condition, availability as Fnac writes it, badges such as Black Friday, and the number of other offers shown under the card), and the filters the page offers for this search, each value with the id to pass back in filters. Prices are in euros. Results include marketplace sellers. A search with no match gives an empty items list with total_results 0, and a page past the last one gives an empty list too. Pass an id to Get Fnac product.

### How do I automatically search Fnac products on fnac.com?

Ask an AI agent connected to Reduck to run reduck/fnac.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/fnac.com/search-products

### Is there a fnac.com API to search Fnac products?

You do not need one. "Search Fnac products" drives the real fnac.com pages in a browser, so it works whether or not fnac.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: page, sort, filters.

### What does it return?

It returns url, page, items, query, filters, total_pages, has_next_page, total_results, applied_filters.

### Do I need to be logged in to fnac.com?

No. It only uses pages of fnac.com that are reachable without signing in.

### Does it change anything on fnac.com, or only read data?

It only reads. It looks things up on fnac.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/fnac.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/fnac.com/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/fnac.com/search-products
