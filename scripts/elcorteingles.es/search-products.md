# Search El Corte Inglés products

Automatically search El Corte Inglés products on elcorteingles.es. Search El Corte Inglés Spain (elcorteingles.es) by free-text query, with the site's sort orders, a price range and the filters of its filter panel (brand, colour, discount, fast delivery, rating, product type, category). Returns one page of results: product id, title, link, brand, barcode number, price and struck-through price in euros, discount, image, status, seller (El Corte Inglés or a marketplace seller), plus the total count, has_next_page and the filter values the site offers, each with the filter string to pass back. A page holds up to 12 slots; the slots the site keeps for sponsored products are not returned, so a page can return fewer than 12 products. El Corte Inglés sends some queries (a brand name) to a brand page: then redirect_url gives that page, the results are the products it lists with the same page and sort, and no filter values are returned, because that page takes no filters; filters or a price range on such a query give an error. A query with no match returns an empty list. Texts are in Spanish. Ratings are not returned: the site does not give them with the results.

- Site: elcorteingles.es
- Address: `reduck/elcorteingles.es/search-products`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/elcorteingles.es/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/elcorteingles.es/search-products
```

## Input

- `query` (string, required): Free-text search query, in Spanish or any word the shop knows.
- `page` (integer, optional): Result page. has_next_page says when to stop.
- `sort` (string, optional): Sort order: relevance (the default), price_asc, price_desc, rating (best rated), bestseller, newest, availability, discount (largest first), name_asc, name_desc.
- `filters` (array, optional): Filters from the site's filter panel, each exactly as the filter of a value in facets gives it, for example "brand::De'Longhi", "colors::Negro", "discount::0.2->0.3" or "category::electrodomesticos". Values of one field are alternatives; different fields all apply. At most one category.
- `price_max` (number, optional): Maximum price in euros.
- `price_min` (number, optional): Minimum price in euros.

## Output

- `url` (string, required): The page that gave the results.
- `page` (integer, required)
- `items` (array, required): Products of this page in the site's order.
- `query` (string, required)
- `facets` (array, required): The filter values the site offers for this search, with the filter string to pass back in filters. Price is the price_min and price_max arguments.
- `page_count` (integer | null, required)
- `redirect_url` (string | null, required): Set when El Corte Inglés opened one of its brand pages for this query instead of the search results. Null for a normal search.
- `has_next_page` (boolean, required)
- `total_results` (integer | null, required): Number of products that match.

## FAQ

### What does "Search El Corte Inglés products" do?

Search El Corte Inglés Spain (elcorteingles.es) by free-text query, with the site's sort orders, a price range and the filters of its filter panel (brand, colour, discount, fast delivery, rating, product type, category). Returns one page of results: product id, title, link, brand, barcode number, price and struck-through price in euros, discount, image, status, seller (El Corte Inglés or a marketplace seller), plus the total count, has_next_page and the filter values the site offers, each with the filter string to pass back. A page holds up to 12 slots; the slots the site keeps for sponsored products are not returned, so a page can return fewer than 12 products. El Corte Inglés sends some queries (a brand name) to a brand page: then redirect_url gives that page, the results are the products it lists with the same page and sort, and no filter values are returned, because that page takes no filters; filters or a price range on such a query give an error. A query with no match returns an empty list. Texts are in Spanish. Ratings are not returned: the site does not give them with the results.

### How do I automatically search El Corte Inglés products on elcorteingles.es?

Ask an AI agent connected to Reduck to run reduck/elcorteingles.es/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/elcorteingles.es/search-products

### Is there a elcorteingles.es API to search El Corte Inglés products?

You do not need one. "Search El Corte Inglés products" drives the real elcorteingles.es pages in a browser, so it works whether or not elcorteingles.es offers an API for this.

### What information do I need to provide?

Required: query. Optional: page, sort, filters, price_max, price_min.

### What does it return?

It returns url, page, items, query, facets, page_count, redirect_url, has_next_page, total_results.

### Do I need to be logged in to elcorteingles.es?

No. It only uses pages of elcorteingles.es that are reachable without signing in.

### Does it change anything on elcorteingles.es, or only read data?

It only reads. It looks things up on elcorteingles.es and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/elcorteingles.es/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/elcorteingles.es/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/elcorteingles.es/search-products
