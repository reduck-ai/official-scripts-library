# Search dm products

Automatically search dm products on dm.de. Search dm Germany (dm.de, the German store) by free-text query, with the site's sort orders, a price range and the filters of its filter bar (category, brand, popular filters, product features and others). Returns one page of 30 products: product id, barcode number, title, brand, link, price in euros, unit price text, rating, review count and image, plus the total count, the page count, has_next_page and the filter values the site offers, each with the filter string to pass back. The online pharmacy products that dm shows in its own tab for the same query come in pharmacy_items. Prices are the online shop prices dm shows a new guest with no dm store chosen. A query with no exact match can still return products the site finds close to it. A page past the last one returns no items. Texts are in German.

- Site: dm.de
- Address: `reduck/dm.de/search-products`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/dm.de/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/dm.de/search-products
```

## Input

- `query` (string, required): Free-text search query, in German or any word the shop knows.
- `page` (integer, optional): Result page, 30 products a page. has_next_page says when to stop.
- `sort` (string, optional): Sort order: relevance (popularity, the default), price_asc, price_desc, new, rating.
- `filters` (array, optional): Filters from the site's filter bar, each as key:value exactly as the filter of a value in facets gives it, for example "brandName:Balea". Values of one key are alternatives; different keys all apply.
- `price_max` (number, optional): Maximum price in euros.
- `price_min` (number, optional): Minimum price in euros.

## Output

- `url` (string, required): The dm page that gave the results.
- `page` (integer, required)
- `items` (array, required): dm products of this page in the site's order.
- `query` (string, required)
- `facets` (array, required): The filter values the site offers for this search, with the filter string to pass back in filters. The price range is the price_min and price_max arguments.
- `page_count` (integer | null, required)
- `has_next_page` (boolean, required)
- `total_results` (integer | null, required): Number of dm products that match.
- `pharmacy_items` (array, required): Online pharmacy products dm shows in its pharmacy tab for this query. Empty when there are none.

## FAQ

### What does "Search dm products" do?

Search dm Germany (dm.de, the German store) by free-text query, with the site's sort orders, a price range and the filters of its filter bar (category, brand, popular filters, product features and others). Returns one page of 30 products: product id, barcode number, title, brand, link, price in euros, unit price text, rating, review count and image, plus the total count, the page count, has_next_page and the filter values the site offers, each with the filter string to pass back. The online pharmacy products that dm shows in its own tab for the same query come in pharmacy_items. Prices are the online shop prices dm shows a new guest with no dm store chosen. A query with no exact match can still return products the site finds close to it. A page past the last one returns no items. Texts are in German.

### How do I automatically search dm products on dm.de?

Ask an AI agent connected to Reduck to run reduck/dm.de/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/dm.de/search-products

### Is there a dm.de API to search dm products?

You do not need one. "Search dm products" drives the real dm.de pages in a browser, so it works whether or not dm.de offers an API for this.

### What information do I need to provide?

Required: query. Optional: page, sort, filters, price_max, price_min.

### What does it return?

It returns url, page, items, query, facets, page_count, has_next_page, total_results, pharmacy_items.

### Do I need to be logged in to dm.de?

No. It only uses pages of dm.de that are reachable without signing in.

### Does it change anything on dm.de, or only read data?

It only reads. It looks things up on dm.de and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/dm.de/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/dm.de/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/dm.de/search-products
