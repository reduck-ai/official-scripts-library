# Search Alibaba.com products

Automatically search Alibaba.com products on alibaba.com. Search Alibaba.com products by free-text query, with the site's own filters: verified supplier, Trade Assurance, instant order, a highest minimum order quantity, a price range, a lowest supplier rating, supplier countries, a category, and every other filter the result lists in filters. Returns one page of about 60 products: per product its id, title, link, price text and price range, minimum order quantity, supplier name, company id, country, years on Alibaba.com, verified mark, supplier rating, review count, sold text, image and whether it is a sponsored slot. Also returns the display currency and ship-to country of this browser, the total of results, the page count and has_next_page. Prices are in the display currency that Alibaba.com sets for the browser. Alibaba.com has no sort control on this search. Its search finds related products for nearly any query, so a query with no exact match can still return a full page; a page with no product returns an empty list. Alibaba.com can show a slider check after many searches close together: the run then fails and names it.

- Site: alibaba.com
- Address: `reduck/alibaba.com/search-products`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/alibaba.com/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/alibaba.com/search-products
```

## Input

- `query` (string, required): Free-text search query.
- `page` (integer, optional): Result page, about 60 products a page. has_next_page says when to stop.
- `price_max` (number, optional): Highest price, in the display currency of the result.
- `price_min` (number, optional): Lowest price, in the display currency of the result.
- `category_id` (string, optional): Only this category, by the id the categoryList filter of a result gives.
- `refinements` (array, optional): Other filters, each as the refinement string of an option in the filters of a result, for example "productAuthTag=CE". Values of one filter are alternatives; different filters all apply.
- `instant_order` (boolean, optional): Only products that you can order at once, with no price talk with the supplier.
- `trade_assurance` (boolean, optional): Only products covered by Trade Assurance.
- `max_minimum_order` (integer, optional): Only products whose minimum order quantity is at most this number.
- `verified_supplier` (boolean, optional): Only products of verified suppliers.
- `supplier_countries` (array, optional): Only suppliers from these countries or regions, as two-letter codes, for example CN or US.
- `min_supplier_rating` (number, optional): Only suppliers whose store rating is at least this value, out of 5.

## Output

- `url` (string, required): The Alibaba.com search page. It does not hold the filters.
- `page` (integer, required)
- `items` (array, required): The products in page order, sponsored slots included. Empty when the page shows no product.
- `query` (string, required)
- `filters` (array, required): The filters Alibaba.com offers for this search, with the options it gives and which ones apply.
- `currency` (string | null, required): Three-letter code of the display currency the prices are in, for example EUR.
- `total_pages` (integer | null, required)
- `has_next_page` (boolean, required)
- `total_results` (integer | null, required): Number of results Alibaba.com gives for the search.
- `ship_to_country` (string | null, required): Two-letter code of the country the browser delivers to, as the header shows it.

## FAQ

### What does "Search Alibaba.com products" do?

Search Alibaba.com products by free-text query, with the site's own filters: verified supplier, Trade Assurance, instant order, a highest minimum order quantity, a price range, a lowest supplier rating, supplier countries, a category, and every other filter the result lists in filters. Returns one page of about 60 products: per product its id, title, link, price text and price range, minimum order quantity, supplier name, company id, country, years on Alibaba.com, verified mark, supplier rating, review count, sold text, image and whether it is a sponsored slot. Also returns the display currency and ship-to country of this browser, the total of results, the page count and has_next_page. Prices are in the display currency that Alibaba.com sets for the browser. Alibaba.com has no sort control on this search. Its search finds related products for nearly any query, so a query with no exact match can still return a full page; a page with no product returns an empty list. Alibaba.com can show a slider check after many searches close together: the run then fails and names it.

### How do I automatically search Alibaba.com products on alibaba.com?

Ask an AI agent connected to Reduck to run reduck/alibaba.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/alibaba.com/search-products

### Is there a alibaba.com API to search Alibaba.com products?

You do not need one. "Search Alibaba.com products" drives the real alibaba.com pages in a browser, so it works whether or not alibaba.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: page, price_max, price_min, category_id, refinements, instant_order, trade_assurance, max_minimum_order, verified_supplier, supplier_countries, min_supplier_rating.

### What does it return?

It returns url, page, items, query, filters, currency, total_pages, has_next_page, total_results, ship_to_country.

### Do I need to be logged in to alibaba.com?

No. It only uses pages of alibaba.com that are reachable without signing in.

### Does it change anything on alibaba.com, or only read data?

It only reads. It looks things up on alibaba.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/alibaba.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/alibaba.com/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/alibaba.com/search-products
