# Search Coolblue products

Automatically search Coolblue products on coolblue.nl. Search Coolblue Netherlands (coolblue.nl) by free-text query, with the site's sort orders, a price range and the filters of its filter column (category, brand, review score and the product's own attributes). Returns one page of products: product number, title, link, brand, price and the reference price before the reduction in euros, review score, review count, image, availability, Coolblue's choice, promotion label and a flag for sponsored products, plus the total count, page count, has_next_page, the filter values the site offers (each with the filter string to pass back and its count) and the price range of the list. Coolblue rates products out of 10, and rating is returned as the site gives it. Coolblue sends some queries (a category word or a brand) to a category or brand page: then redirect_url gives that page, and the results are the products it lists with the same page, sort and filters, or no items when it is a landing page without a list. A search with no result returns an empty list.

- Site: coolblue.nl
- Address: `reduck/coolblue.nl/search-products`
- Updated: 2026-11-24 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/coolblue.nl/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/coolblue.nl/search-products
```

## Input

- `query` (string, required): Free-text search query, in Dutch or any word the shop knows.
- `page` (integer, optional): Result page. has_next_page says when to stop.
- `sort` (string, optional): Sort order: relevance (the default), rating (best review score), price_asc, price_desc, bestseller (most popular).
- `filters` (array, optional): Filters from the site's filter column, each as field:value exactly as the filter of a value in facets gives it, for example "merk:logitech", "producttype:muizen" or "minimum-review-sterren:4". Values of one field are alternatives; different fields all apply.
- `price_max` (number, optional): Maximum price in euros.
- `price_min` (number, optional): Minimum price in euros.

## Output

- `url` (string, required): The page that gave the results.
- `page` (integer, required)
- `items` (array, required): Products of this page in the site's order.
- `query` (string, required)
- `facets` (array, required): The filter values the site offers for this list, with the filter string to pass back in filters. Price is the price_min and price_max arguments.
- `page_count` (integer | null, required)
- `price_range` (object | null, required): Lowest and highest price in the list, and the price range applied.
- `redirect_url` (string | null, required): Set when Coolblue opened one of its category, brand or landing pages for this query instead of the search results. Null for a normal search.
- `has_next_page` (boolean, required)
- `total_results` (integer | null, required): Number of products that match. Null when the query opened a landing page that lists no products.

## FAQ

### What does "Search Coolblue products" do?

Search Coolblue Netherlands (coolblue.nl) by free-text query, with the site's sort orders, a price range and the filters of its filter column (category, brand, review score and the product's own attributes). Returns one page of products: product number, title, link, brand, price and the reference price before the reduction in euros, review score, review count, image, availability, Coolblue's choice, promotion label and a flag for sponsored products, plus the total count, page count, has_next_page, the filter values the site offers (each with the filter string to pass back and its count) and the price range of the list. Coolblue rates products out of 10, and rating is returned as the site gives it. Coolblue sends some queries (a category word or a brand) to a category or brand page: then redirect_url gives that page, and the results are the products it lists with the same page, sort and filters, or no items when it is a landing page without a list. A search with no result returns an empty list.

### How do I automatically search Coolblue products on coolblue.nl?

Ask an AI agent connected to Reduck to run reduck/coolblue.nl/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/coolblue.nl/search-products

### Is there a coolblue.nl API to search Coolblue products?

You do not need one. "Search Coolblue products" drives the real coolblue.nl pages in a browser, so it works whether or not coolblue.nl offers an API for this.

### What information do I need to provide?

Required: query. Optional: page, sort, filters, price_max, price_min.

### What does it return?

It returns url, page, items, query, facets, page_count, price_range, redirect_url, has_next_page, total_results.

### Do I need to be logged in to coolblue.nl?

No. It only uses pages of coolblue.nl that are reachable without signing in.

### Does it change anything on coolblue.nl, or only read data?

It only reads. It looks things up on coolblue.nl and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/coolblue.nl/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/coolblue.nl/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/coolblue.nl/search-products
