# Search Cdiscount products

Automatically search Cdiscount products on cdiscount.com. Search Cdiscount.com by free-text query, with Cdiscount's own sort order and filters (category, brand, price band, seller, delivery, customer rating, condition and the product's attributes). Returns one page of results: the total result and page counts, has_next_page, the filters that apply, the items (sku, offer_id, title, url, price, list_price, rating, review_count, image_url, sponsored, seller, condition, free_shipping and deals such as Black Friday operations with their end time), and the filters the page offers for this search, each value with the id to pass back in filters and its result count. Prices are in euros. A page has about 45 to 65 items, sponsored ones included. Stop paging when has_next_page is false: Cdiscount refuses a page far past the last one, and the run then fails. When few products match, Cdiscount shows loosely related products; a filter id that matches nothing gives an empty items list with total_results 0. Pass a sku to Get Cdiscount product or Get Cdiscount product reviews.

- Site: cdiscount.com
- Address: `reduck/cdiscount.com/search-products`
- Updated: 2026-11-24 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/cdiscount.com/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/cdiscount.com/search-products
```

## Input

- `query` (string, required): Free-text search query.
- `page` (integer, optional): Result page. has_next_page and total_pages say when to stop.
- `sort` (string, optional): Sort order: relevance (the default), best_sellers, price_asc (lowest price first), price_desc (highest price first), rating (customer reviews).
- `filters` (array, optional): Filter ids from the filters of an earlier result for the same query, for example Marque/"jbl" (a brand), Prix/"20 à 50€" (a price band) or Vendeur/[*;0] (sold by Cdiscount). Values of one filter are alternatives; different filters all apply.

## Output

- `url` (string, required)
- `page` (integer, required)
- `items` (array, required): The results in page order, sponsored ones included.
- `query` (string, required)
- `filters` (array, required): Filters the page offers for this search, in page order.
- `total_pages` (integer | null, required)
- `has_next_page` (boolean, required): True when Cdiscount has a page after this one.
- `total_results` (integer | null, required): Number of products that match, as Cdiscount states it.
- `applied_filters` (array, required): Filter ids that apply to this page. Cdiscount can add a category on its own.
- `sort` (string | null, optional): Sort that Cdiscount applied, as field and direction, for example "price asc".

## FAQ

### What does "Search Cdiscount products" do?

Search Cdiscount.com by free-text query, with Cdiscount's own sort order and filters (category, brand, price band, seller, delivery, customer rating, condition and the product's attributes). Returns one page of results: the total result and page counts, has_next_page, the filters that apply, the items (sku, offer_id, title, url, price, list_price, rating, review_count, image_url, sponsored, seller, condition, free_shipping and deals such as Black Friday operations with their end time), and the filters the page offers for this search, each value with the id to pass back in filters and its result count. Prices are in euros. A page has about 45 to 65 items, sponsored ones included. Stop paging when has_next_page is false: Cdiscount refuses a page far past the last one, and the run then fails. When few products match, Cdiscount shows loosely related products; a filter id that matches nothing gives an empty items list with total_results 0. Pass a sku to Get Cdiscount product or Get Cdiscount product reviews.

### How do I automatically search Cdiscount products on cdiscount.com?

Ask an AI agent connected to Reduck to run reduck/cdiscount.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/cdiscount.com/search-products

### Is there a cdiscount.com API to search Cdiscount products?

You do not need one. "Search Cdiscount products" drives the real cdiscount.com pages in a browser, so it works whether or not cdiscount.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: page, sort, filters.

### What does it return?

It returns url, page, sort, items, query, filters, total_pages, has_next_page, total_results, applied_filters.

### Do I need to be logged in to cdiscount.com?

No. It only uses pages of cdiscount.com that are reachable without signing in.

### Does it change anything on cdiscount.com, or only read data?

It only reads. It looks things up on cdiscount.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/cdiscount.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/cdiscount.com/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/cdiscount.com/search-products
