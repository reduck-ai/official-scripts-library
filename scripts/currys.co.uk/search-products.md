# Search Currys products

Automatically search Currys products on currys.co.uk. Search Currys (currys.co.uk) by free-text query, with the site's sort orders, page size, a price range and the filters it offers for the list (brand, price ranges, delivery or collection and the product's own attributes). Returns one page of products: product number, title, link, brand, barcode number, price and price before the reduction in pounds sterling, rating, review count, image, delivery and store collection availability, stock status, category path and a flag for paid placements, plus the total count, has_next_page and the filter values the site offers, each with the filter string to pass back. Currys sends some queries (a category word) to a category page: then redirect_url gives that page, and the results are the products it lists with the same page, sort and filters. A query with no exact match can return a few products the site finds close to it; a search with no result at all returns an empty list.

- Site: currys.co.uk
- Address: `reduck/currys.co.uk/search-products`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/currys.co.uk/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/currys.co.uk/search-products
```

## Input

- `query` (string, required): Free-text search query.
- `page` (integer, optional): Result page. has_next_page says when to stop.
- `sort` (string, optional): Sort order: relevance (best match, the default), price_asc, price_desc, rating (customer rating), newest (newest arrivals).
- `filters` (array, optional): Filters, each as field:value exactly as the filter of a value in facets gives it, for example "brand:SONY" or "price:0.0-200.0". Values of one field are alternatives; different fields all apply.
- `page_size` (integer, optional): Products a page, as the site offers: 20, 30 or 50.
- `price_max` (number, optional): Maximum price in pounds.
- `price_min` (number, optional): Minimum price in pounds.

## Output

- `url` (string, required): The page that gave the results.
- `page` (integer, required)
- `items` (array, required): Products of this page in the site's order, paid placements included and marked. Empty when nothing matches.
- `query` (string, required)
- `facets` (array, required): The filter values the site offers for this list (category, brand, price ranges, delivery or collection, customer rating, stock and the product's own attributes), grouped by filter, with the filter string to pass back in filters.
- `page_count` (integer, required)
- `redirect_url` (string | null, required): Set when Currys opened one of its category pages for this query instead of the search results. Null for a normal search.
- `has_next_page` (boolean, required)
- `total_results` (integer, required)

## FAQ

### What does "Search Currys products" do?

Search Currys (currys.co.uk) by free-text query, with the site's sort orders, page size, a price range and the filters it offers for the list (brand, price ranges, delivery or collection and the product's own attributes). Returns one page of products: product number, title, link, brand, barcode number, price and price before the reduction in pounds sterling, rating, review count, image, delivery and store collection availability, stock status, category path and a flag for paid placements, plus the total count, has_next_page and the filter values the site offers, each with the filter string to pass back. Currys sends some queries (a category word) to a category page: then redirect_url gives that page, and the results are the products it lists with the same page, sort and filters. A query with no exact match can return a few products the site finds close to it; a search with no result at all returns an empty list.

### How do I automatically search Currys products on currys.co.uk?

Ask an AI agent connected to Reduck to run reduck/currys.co.uk/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/currys.co.uk/search-products

### Is there a currys.co.uk API to search Currys products?

You do not need one. "Search Currys products" drives the real currys.co.uk pages in a browser, so it works whether or not currys.co.uk offers an API for this.

### What information do I need to provide?

Required: query. Optional: page, sort, filters, page_size, price_max, price_min.

### What does it return?

It returns url, page, items, query, facets, page_count, redirect_url, has_next_page, total_results.

### Do I need to be logged in to currys.co.uk?

No. It only uses pages of currys.co.uk that are reachable without signing in.

### Does it change anything on currys.co.uk, or only read data?

It only reads. It looks things up on currys.co.uk and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/currys.co.uk/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/currys.co.uk/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/currys.co.uk/search-products
