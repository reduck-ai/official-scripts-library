# Search Argos products

Automatically search Argos products on argos.co.uk. Search Argos (argos.co.uk) by free-text query, with the site's sort orders and the filters it offers for the search (category, brand, price range, customer rating and the product's own attributes). Returns one page of up to 60 products: product number, title, link, brand, price and earlier price in pounds sterling, offer text, rating, review count, image, delivery cost, delivery and store reservation flags, clearance and variant flags, plus the total count, has_next_page and the filter values the site offers, each with the filter string to pass back. Argos sends some queries to a curated list page: then redirect_url gives that page, and the results are the products it lists with the same page, sort and filters. Argos can also apply a category to a search by itself. When nothing matches, items is empty.

- Site: argos.co.uk
- Address: `reduck/argos.co.uk/search-products`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/argos.co.uk/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/argos.co.uk/search-products
```

## Input

- `query` (string, required): Free-text search query.
- `page` (integer, optional): Result page, 60 products a page. has_next_page says when to stop.
- `sort` (string, optional): Sort order: relevance (the default), price_asc, price_desc, rating (customer rating), newest (new in).
- `filters` (array, optional): Filters, each as field:value exactly as the filter of a value in facets gives it, for example "brands:sony", "category:820665", "price:£25 - £50" or "customer rating:4 or more". Values of one field are alternatives; different fields all apply. Price is one of the ranges the site offers.

## Output

- `url` (string, required): The page that gave the results.
- `page` (integer, required)
- `items` (array, required): Products of this page in the site's order. Empty when nothing matches.
- `query` (string, required)
- `facets` (array, required): The filters the site offers for this search (category, brand, price ranges, customer rating and the product's own attributes), with the filter string to pass back in filters. Argos can apply a category by itself: it then shows in facets.
- `page_count` (integer, required)
- `redirect_url` (string | null, required): Set when Argos opened one of its curated list pages for this query instead of the search results. Null for a normal search.
- `has_next_page` (boolean, required)
- `total_results` (integer, required)

## FAQ

### What does "Search Argos products" do?

Search Argos (argos.co.uk) by free-text query, with the site's sort orders and the filters it offers for the search (category, brand, price range, customer rating and the product's own attributes). Returns one page of up to 60 products: product number, title, link, brand, price and earlier price in pounds sterling, offer text, rating, review count, image, delivery cost, delivery and store reservation flags, clearance and variant flags, plus the total count, has_next_page and the filter values the site offers, each with the filter string to pass back. Argos sends some queries to a curated list page: then redirect_url gives that page, and the results are the products it lists with the same page, sort and filters. Argos can also apply a category to a search by itself. When nothing matches, items is empty.

### How do I automatically search Argos products on argos.co.uk?

Ask an AI agent connected to Reduck to run reduck/argos.co.uk/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/argos.co.uk/search-products

### Is there a argos.co.uk API to search Argos products?

You do not need one. "Search Argos products" drives the real argos.co.uk pages in a browser, so it works whether or not argos.co.uk offers an API for this.

### What information do I need to provide?

Required: query. Optional: page, sort, filters.

### What does it return?

It returns url, page, items, query, facets, page_count, redirect_url, has_next_page, total_results.

### Do I need to be logged in to argos.co.uk?

No. It only uses pages of argos.co.uk that are reachable without signing in.

### Does it change anything on argos.co.uk, or only read data?

It only reads. It looks things up on argos.co.uk and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/argos.co.uk/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/argos.co.uk/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/argos.co.uk/search-products
