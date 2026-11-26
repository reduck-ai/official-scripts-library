# Search Amazon.es products

Automatically search Amazon.es products on amazon.es. Search Amazon.es by free-text query, with Amazon's own filters: department, sort order, price range and refinements. Returns one page of results (asin, title, url, price, list_price, rating, review_count, image_url, sponsored, deal, badges, formats) with currency and has_next_page. deal is the deal the card shows: its id, its label as Amazon writes it, and the end of its countdown when it shows one. badges are the other badges of the card, for example Amazon's Choice or a sustainability label. Prices are in the currency the store displays, returned as currency: euros unless the browser prefers another. Pinned to a Spanish postcode.

- Site: amazon.es
- Address: `reduck/amazon.es/search-products`
- Updated: 2026-11-25 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/amazon.es/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/amazon.es/search-products
```

## Input

- `query` (string, required): Free-text search query.
- `page` (integer, optional): Result page. has_next_page says when to stop.
- `sort` (string, optional): Sort order.
- `zipCode` (string, optional): Spanish postcode used to pin the store location (prices, availability).
- `price_max` (number, optional): Maximum price, in euros: the store's own currency, even when the page displays another.
- `price_min` (number, optional): Minimum price, in euros: the store's own currency, even when the page displays another.
- `department` (string, optional): Department search alias, from list_search_filters.
- `refinements` (array, optional): Filters as group:value, from list_search_filters for the same query.

## Output

- `url` (string, required)
- `zip` (string, required)
- `page` (integer, required)
- `items` (array, required)
- `query` (string, required)
- `currency` (string, required): ISO 4217 code of the currency of every price in this result, as the store displays it: the store's own (euros (EUR)) unless the browser prefers another, which Amazon then shows instead.
- `has_next_page` (boolean, required)

## FAQ

### What does "Search Amazon.es products" do?

Search Amazon.es by free-text query, with Amazon's own filters: department, sort order, price range and refinements. Returns one page of results (asin, title, url, price, list_price, rating, review_count, image_url, sponsored, deal, badges, formats) with currency and has_next_page. deal is the deal the card shows: its id, its label as Amazon writes it, and the end of its countdown when it shows one. badges are the other badges of the card, for example Amazon's Choice or a sustainability label. Prices are in the currency the store displays, returned as currency: euros unless the browser prefers another. Pinned to a Spanish postcode.

### How do I automatically search Amazon.es products on amazon.es?

Ask an AI agent connected to Reduck to run reduck/amazon.es/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.es/search-products

### Is there a amazon.es API to search Amazon.es products?

You do not need one. "Search Amazon.es products" drives the real amazon.es pages in a browser, so it works whether or not amazon.es offers an API for this.

### What information do I need to provide?

Required: query. Optional: page, sort, zipCode, price_max, price_min, department, refinements.

### What does it return?

It returns url, zip, page, items, query, currency, has_next_page.

### Do I need to be logged in to amazon.es?

No. It only uses pages of amazon.es that are reachable without signing in.

### Does it change anything on amazon.es, or only read data?

It only reads. It looks things up on amazon.es and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/amazon.es/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.es/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/amazon.es/search-products
