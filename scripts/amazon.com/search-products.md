# Search Amazon products

Automatically search Amazon products on amazon.com. Search Amazon by free-text query, with Amazon's own filters: department, sort order, price range, and the refinements of its left column (Prime, delivery speed, brand, customer reviews, condition, seller and the product's attributes), whose values List Amazon search filters gives. Returns one page of results: query, page, zip, url, has_next_page and items (asin, title, url, price, list_price, rating, review_count, image_url, sponsored, formats). formats lists each edition a result links to (for example Hardcover, Kindle and Audiobook for a book), with its own ASIN, URL and price when shown. has_next_page is false on the last page, on a page past the last one (Amazon stops near page 20) and when nothing matches; then Amazon can still show a few unrelated sponsored products. Organic results are stable per page but sponsored slots rotate between fetches.

- Site: amazon.com
- Address: `reduck/amazon.com/search-products`
- Updated: 2026-10-22 (v17)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/amazon.com/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/amazon.com/search-products
```

## Input

- `query` (string, required): Free-text search query.
- `page` (integer, optional): Result page (about 16 to 22 organic results a page; Amazon stops near page 20). has_next_page says when to stop.
- `sort` (string, optional): Sort order: relevanceblender (featured, the default), price-asc-rank, price-desc-rank, review-rank (average customer review), date-desc-rank (newest arrivals), exact-aware-popularity-rank (best sellers).
- `zipCode` (string, optional): US ZIP used to pin the store location (prices, availability).
- `price_max` (number, optional): Maximum price in US dollars.
- `price_min` (number, optional): Minimum price in US dollars.
- `department` (string, optional): Department to search in, as its search alias, e.g. "stripbooks" (Books) or "electronics" (values from list_search_filters, key department). Default: all departments.
- `refinements` (array, optional): Filters from Amazon's left column, each as group:value, e.g. "p_85:2470955011" (Prime) or "p_123:3271" (a brand). Get them from list_search_filters for the same query. Values of one group are alternatives; different groups all apply.

## Output

- `url` (string, required)
- `zip` (string, required)
- `page` (integer, required)
- `items` (array, required): The results in page order, sponsored ones included. When nothing matches the query, Amazon can still show a few sponsored products that are not about it.
- `query` (string, required)
- `has_next_page` (boolean, required): True when Amazon offers a next page of results for this search. False on the last page, on a page past the last one, and when nothing matches the query.

## FAQ

### What does "Search Amazon products" do?

Search Amazon by free-text query, with Amazon's own filters: department, sort order, price range, and the refinements of its left column (Prime, delivery speed, brand, customer reviews, condition, seller and the product's attributes), whose values List Amazon search filters gives. Returns one page of results: query, page, zip, url, has_next_page and items (asin, title, url, price, list_price, rating, review_count, image_url, sponsored, formats). formats lists each edition a result links to (for example Hardcover, Kindle and Audiobook for a book), with its own ASIN, URL and price when shown. has_next_page is false on the last page, on a page past the last one (Amazon stops near page 20) and when nothing matches; then Amazon can still show a few unrelated sponsored products. Organic results are stable per page but sponsored slots rotate between fetches.

### How do I automatically search Amazon products on amazon.com?

Ask an AI agent connected to Reduck to run reduck/amazon.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.com/search-products

### Is there a amazon.com API to search Amazon products?

You do not need one. "Search Amazon products" drives the real amazon.com pages in a browser, so it works whether or not amazon.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: page, sort, zipCode, price_max, price_min, department, refinements.

### What does it return?

It returns url, zip, page, items, query, has_next_page.

### Do I need to be logged in to amazon.com?

No. It only uses pages of amazon.com that are reachable without signing in.

### Does it change anything on amazon.com, or only read data?

It only reads. It looks things up on amazon.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/amazon.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.com/search-products

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/amazon.com/search-products
