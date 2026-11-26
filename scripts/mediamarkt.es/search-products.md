# Search MediaMarkt Spain products

Automatically search MediaMarkt Spain products on mediamarkt.es. Search MediaMarkt Spain (mediamarkt.es) by free-text query, with the site's sort orders, a price range and the filters of its filter column (brand, category, rating, color and the product's own attributes). Returns one page of 12 products: product id, title, link, brand, barcode number, price and struck-through price in euros, discount, rating, review count, image, delivery status and dates, shipping cost and seller (MediaMarkt or a Marketplace seller), plus the total count, has_next_page and the filter values the site offers, each with the filter string to pass back. MediaMarkt sends some queries (a category word or a brand) to a category, brand or theme page: then redirect_url gives that page, and the results are the products it lists with the same page, sort and filters, or no items when it is a theme page without a list. A query with no exact match can still return products the site finds close to it. Paging stops at page 30. Texts are in Spanish.

- Site: mediamarkt.es
- Address: `reduck/mediamarkt.es/search-products`
- Updated: 2026-11-24 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/mediamarkt.es/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/mediamarkt.es/search-products
```

## Input

- `query` (string, required): Free-text search query, in Spanish or any word the shop knows.
- `page` (integer, optional): Result page, 12 products a page. MediaMarkt stops at page 30. has_next_page says when to stop.
- `sort` (string, optional): Sort order: relevance (the default), price_asc, price_desc, rating (customer rating), bestseller, newest, availability.
- `filters` (array, optional): Filters from the site's filter column, each as field:value exactly as the filter of a value in facets gives it, for example "brand:SONY" or "category:CAT_ES_MM_398". Values of one field are alternatives; different fields all apply.
- `price_max` (number, optional): Maximum price in euros.
- `price_min` (number, optional): Minimum price in euros.

## Output

- `url` (string, required): The page that gave the results.
- `page` (integer, required)
- `items` (array, required): Products of this page in the site's order.
- `query` (string, required)
- `facets` (array, required): The filter values the site offers for this search, with the filter string to pass back in filters. Price is the price_min and price_max arguments.
- `page_count` (integer | null, required)
- `redirect_url` (string | null, required): Set when MediaMarkt opened one of its category, brand or theme pages for this query instead of the search results. Null for a normal search.
- `has_next_page` (boolean, required)
- `total_results` (integer | null, required): Number of products that match. Null when the query opened a theme page that lists no products.

## FAQ

### What does "Search MediaMarkt Spain products" do?

Search MediaMarkt Spain (mediamarkt.es) by free-text query, with the site's sort orders, a price range and the filters of its filter column (brand, category, rating, color and the product's own attributes). Returns one page of 12 products: product id, title, link, brand, barcode number, price and struck-through price in euros, discount, rating, review count, image, delivery status and dates, shipping cost and seller (MediaMarkt or a Marketplace seller), plus the total count, has_next_page and the filter values the site offers, each with the filter string to pass back. MediaMarkt sends some queries (a category word or a brand) to a category, brand or theme page: then redirect_url gives that page, and the results are the products it lists with the same page, sort and filters, or no items when it is a theme page without a list. A query with no exact match can still return products the site finds close to it. Paging stops at page 30. Texts are in Spanish.

### How do I automatically search MediaMarkt Spain products on mediamarkt.es?

Ask an AI agent connected to Reduck to run reduck/mediamarkt.es/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/mediamarkt.es/search-products

### Is there a mediamarkt.es API to search MediaMarkt Spain products?

You do not need one. "Search MediaMarkt Spain products" drives the real mediamarkt.es pages in a browser, so it works whether or not mediamarkt.es offers an API for this.

### What information do I need to provide?

Required: query. Optional: page, sort, filters, price_max, price_min.

### What does it return?

It returns url, page, items, query, facets, page_count, redirect_url, has_next_page, total_results.

### Do I need to be logged in to mediamarkt.es?

No. It only uses pages of mediamarkt.es that are reachable without signing in.

### Does it change anything on mediamarkt.es, or only read data?

It only reads. It looks things up on mediamarkt.es and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/mediamarkt.es/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/mediamarkt.es/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/mediamarkt.es/search-products
