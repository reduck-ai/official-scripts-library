# Search Amazon.fr products

Automatically search Amazon.fr products on amazon.fr. Search Amazon.fr by free-text query, with Amazon's own filters: department, sort order, price range, and the refinements of its left column (Prime, delivery speed, brand, customer reviews, condition, seller and the product's attributes), whose values List Amazon search filters gives. Returns one page of results: query, page, zip, url, has_next_page and items (asin, title, url, price, list_price, rating, review_count, image_url, sponsored, deal, badges, formats). deal is the deal the card shows: its id, its label as Amazon writes it, and the end of its countdown when it shows one. badges are the other badges of the card, for example Choix d'Amazon or a sustainability label. formats lists each edition a result links to (for example Hardcover, Kindle and Audiobook for a book), with its own ASIN, URL and price when shown. has_next_page is false on the last page, on a page past the last one (Amazon stops near page 20) and when nothing matches; then Amazon can still show a few unrelated sponsored products. Organic results are stable per page but sponsored slots rotate between fetches.

- Site: amazon.fr
- Address: `reduck/amazon.fr/search-products`
- Updated: 2026-11-18 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/amazon.fr/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/amazon.fr/search-products
```

## Input

- `query` (string, required): Free-text search query.
- `page` (integer, optional): Result page (about 16 to 22 organic results a page; Amazon stops near page 20). has_next_page says when to stop.
- `sort` (string, optional): Sort order: relevanceblender (featured, the default), price-asc-rank, price-desc-rank, review-rank (average customer review), date-desc-rank (newest arrivals), exact-aware-popularity-rank (best sellers).
- `zipCode` (string, optional): French postcode used to pin the store location (prices, availability).
- `price_max` (number, optional): Maximum price in euros.
- `price_min` (number, optional): Minimum price in euros.
- `department` (string, optional): Department to search in, as its search alias, e.g. "stripbooks" (Books) or "electronics" (values from list_search_filters, key department). Default: all departments.
- `refinements` (array, optional): Filters from Amazon's left column, each as group:value, e.g. "p_123:<id>" for a brand. Get them from List Amazon.fr search filters for the same query: the ids are this store's own. Values of one group are alternatives; different groups all apply.

## Output

- `url` (string, required)
- `zip` (string, required)
- `page` (integer, required)
- `items` (array, required): The results in page order, sponsored ones included. When nothing matches the query, Amazon can still show a few sponsored products that are not about it.
- `query` (string, required)
- `has_next_page` (boolean, required): True when Amazon offers a next page of results for this search. False on the last page, on a page past the last one, and when nothing matches the query.

## FAQ

### What does "Search Amazon.fr products" do?

Search Amazon.fr by free-text query, with Amazon's own filters: department, sort order, price range, and the refinements of its left column (Prime, delivery speed, brand, customer reviews, condition, seller and the product's attributes), whose values List Amazon search filters gives. Returns one page of results: query, page, zip, url, has_next_page and items (asin, title, url, price, list_price, rating, review_count, image_url, sponsored, deal, badges, formats). deal is the deal the card shows: its id, its label as Amazon writes it, and the end of its countdown when it shows one. badges are the other badges of the card, for example Choix d'Amazon or a sustainability label. formats lists each edition a result links to (for example Hardcover, Kindle and Audiobook for a book), with its own ASIN, URL and price when shown. has_next_page is false on the last page, on a page past the last one (Amazon stops near page 20) and when nothing matches; then Amazon can still show a few unrelated sponsored products. Organic results are stable per page but sponsored slots rotate between fetches.

### How do I automatically search Amazon.fr products on amazon.fr?

Ask an AI agent connected to Reduck to run reduck/amazon.fr/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.fr/search-products

### Is there a amazon.fr API to search Amazon.fr products?

You do not need one. "Search Amazon.fr products" drives the real amazon.fr pages in a browser, so it works whether or not amazon.fr offers an API for this.

### What information do I need to provide?

Required: query. Optional: page, sort, zipCode, price_max, price_min, department, refinements.

### What does it return?

It returns url, zip, page, items, query, has_next_page.

### Do I need to be logged in to amazon.fr?

No. It only uses pages of amazon.fr that are reachable without signing in.

### Does it change anything on amazon.fr, or only read data?

It only reads. It looks things up on amazon.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/amazon.fr/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.fr/search-products

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/amazon.fr/search-products
