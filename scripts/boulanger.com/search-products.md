# Search Boulanger products

Automatically search Boulanger products on boulanger.com. Search Boulanger.com by free-text query, with Boulanger's own sort order, a price range and the filters of its left column (brand, seller, condition, customer rating, product type and the product's attributes). Returns one page of up to 40 results: the total result count, has_next_page, the filters that apply, the items (id, offer_id, title, url, price, list_price, rating, review_count, image_url, brand, seller, condition, available, badges such as Black Friday) and the filters the page offers for this search, each value with the id to pass back in filters and its result count. Prices are in euros. Advertising cards between the results are left out. A search with no match, and a page past the last one, give an empty items list. Pass an id to Get Boulanger product.

- Site: boulanger.com
- Address: `reduck/boulanger.com/search-products`
- Updated: 2026-11-24 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/boulanger.com/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/boulanger.com/search-products
```

## Input

- `query` (string, required): Free-text search query.
- `page` (integer, optional): Result page, up to 40 results a page. has_next_page says when to stop.
- `sort` (string, optional): Sort order: relevance (the default), price_asc (lowest price first), price_desc (highest price first), rating (best rating first).
- `filters` (array, optional): Filter ids from the filters of an earlier result for the same query, for example brand~jbl or brand~sony. Values of one filter are alternatives; different filters all apply.
- `price_max` (number, optional): Highest price in euros.
- `price_min` (number, optional): Lowest price in euros.

## Output

- `url` (string, required)
- `page` (integer, required)
- `items` (array, required): The results in page order, without the advertising cards.
- `query` (string, required)
- `filters` (array, required): Filters the page offers for this search, in page order.
- `has_next_page` (boolean, required)
- `total_results` (integer | null, required): Number of products that match, as Boulanger states it. 0 when nothing matches.
- `applied_filters` (array, required)

## FAQ

### What does "Search Boulanger products" do?

Search Boulanger.com by free-text query, with Boulanger's own sort order, a price range and the filters of its left column (brand, seller, condition, customer rating, product type and the product's attributes). Returns one page of up to 40 results: the total result count, has_next_page, the filters that apply, the items (id, offer_id, title, url, price, list_price, rating, review_count, image_url, brand, seller, condition, available, badges such as Black Friday) and the filters the page offers for this search, each value with the id to pass back in filters and its result count. Prices are in euros. Advertising cards between the results are left out. A search with no match, and a page past the last one, give an empty items list. Pass an id to Get Boulanger product.

### How do I automatically search Boulanger products on boulanger.com?

Ask an AI agent connected to Reduck to run reduck/boulanger.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/boulanger.com/search-products

### Is there a boulanger.com API to search Boulanger products?

You do not need one. "Search Boulanger products" drives the real boulanger.com pages in a browser, so it works whether or not boulanger.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: page, sort, filters, price_max, price_min.

### What does it return?

It returns url, page, items, query, filters, has_next_page, total_results, applied_filters.

### Do I need to be logged in to boulanger.com?

No. It only uses pages of boulanger.com that are reachable without signing in.

### Does it change anything on boulanger.com, or only read data?

It only reads. It looks things up on boulanger.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/boulanger.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/boulanger.com/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/boulanger.com/search-products
