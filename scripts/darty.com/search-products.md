# Search Darty products

Automatically search Darty products on darty.com. Search Darty.com by free-text query, with Darty's own sort order and filters (brand, category, seller, condition, customer rating, availability and the product's characteristics). Returns one page of up to 30 results: the total result count, has_next_page, the items (id, title, brand, url, price, list_price, rating, review_count, image_url, marketplace_seller) and the filters the page offers for this search, each value with the id to pass back in filters. Prices are in euros. A search with no match gives an empty items list with total_results 0. Pass an id to Get Darty product.

- Site: darty.com
- Address: `reduck/darty.com/search-products`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/darty.com/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/darty.com/search-products
```

## Input

- `query` (string, required): Free-text search query.
- `page` (integer, optional): Result page, 30 results a page. has_next_page says when to stop.
- `sort` (string, optional): Sort order: relevance (the default), price_asc (lowest price first), price_desc (highest price first), rating (best rating first), newest.
- `filters` (array, optional): Filter ids from the filters of an earlier result for the same query, for example m=JBL (a brand) or c=368296 (a characteristic). Values with the same key are alternatives; different keys all apply.

## Output

- `url` (string, required)
- `page` (integer, required)
- `items` (array, required)
- `query` (string, required)
- `filters` (array, required): Filter values the page offers for this search, in page order.
- `has_next_page` (boolean, required)
- `total_results` (integer | null, required): Number of products that match, as Darty states it. 0 when nothing matches.
- `applied_filters` (array, required)

## FAQ

### What does "Search Darty products" do?

Search Darty.com by free-text query, with Darty's own sort order and filters (brand, category, seller, condition, customer rating, availability and the product's characteristics). Returns one page of up to 30 results: the total result count, has_next_page, the items (id, title, brand, url, price, list_price, rating, review_count, image_url, marketplace_seller) and the filters the page offers for this search, each value with the id to pass back in filters. Prices are in euros. A search with no match gives an empty items list with total_results 0. Pass an id to Get Darty product.

### How do I automatically search Darty products on darty.com?

Ask an AI agent connected to Reduck to run reduck/darty.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/darty.com/search-products

### Is there a darty.com API to search Darty products?

You do not need one. "Search Darty products" drives the real darty.com pages in a browser, so it works whether or not darty.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: page, sort, filters.

### What does it return?

It returns url, page, items, query, filters, has_next_page, total_results, applied_filters.

### Do I need to be logged in to darty.com?

No. It only uses pages of darty.com that are reachable without signing in.

### Does it change anything on darty.com, or only read data?

It only reads. It looks things up on darty.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/darty.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/darty.com/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/darty.com/search-products
