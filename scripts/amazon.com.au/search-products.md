# Search Amazon.com.au products

Automatically search Amazon.com.au products on amazon.com.au. Search Amazon.com.au by free-text query, with Amazon's own filters: department, sort order, price range and refinements. Returns one page of results (asin, title, url, price, list_price, rating, review_count, image_url, sponsored, deal, badges, formats) with currency and has_next_page. deal is the deal the card shows: its id, its label as Amazon writes it (for example "Black Friday Deal"), and the end of its countdown when it shows one. badges are the other badges of the card, for example Amazon's Choice or a sustainability label. Prices are in the currency the store displays, returned as currency: Australian dollars unless the browser prefers another. Pinned to an Australian postcode.

- Site: amazon.com.au
- Address: `reduck/amazon.com.au/search-products`
- Updated: 2026-11-25 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/amazon.com.au/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/amazon.com.au/search-products
```

## Input

- `query` (string, required): Free-text search query.
- `page` (integer, optional): Result page. has_next_page says when to stop.
- `sort` (string, optional): Sort order: relevanceblender (featured, the default), price-asc-rank, price-desc-rank, review-rank (average customer review), date-desc-rank (newest arrivals), exact-aware-popularity-rank (best sellers).
- `zipCode` (string, optional): Australian postcode used to pin the store location (prices, availability).
- `price_max` (number, optional): Maximum price, in Australian dollars: the store's own currency, even when the page displays another.
- `price_min` (number, optional): Minimum price, in Australian dollars: the store's own currency, even when the page displays another.
- `department` (string, optional): Department search alias, e.g. "electronics".
- `refinements` (array, optional): Filters from Amazon's left column, each as group:value (the store's own ids). Values of one group are alternatives; different groups all apply.

## Output

- `url` (string, required)
- `zip` (string, required)
- `page` (integer, required)
- `items` (array, required): The results in page order, sponsored ones included.
- `query` (string, required)
- `currency` (string, required): ISO 4217 code of the currency of every price in this result, as the store displays it: the store's own (Australian dollars (AUD)) unless the browser prefers another, which Amazon then shows instead.
- `has_next_page` (boolean, required): True when Amazon offers a next page. False on the last page and when nothing matches.

## FAQ

### What does "Search Amazon.com.au products" do?

Search Amazon.com.au by free-text query, with Amazon's own filters: department, sort order, price range and refinements. Returns one page of results (asin, title, url, price, list_price, rating, review_count, image_url, sponsored, deal, badges, formats) with currency and has_next_page. deal is the deal the card shows: its id, its label as Amazon writes it (for example "Black Friday Deal"), and the end of its countdown when it shows one. badges are the other badges of the card, for example Amazon's Choice or a sustainability label. Prices are in the currency the store displays, returned as currency: Australian dollars unless the browser prefers another. Pinned to an Australian postcode.

### How do I automatically search Amazon.com.au products on amazon.com.au?

Ask an AI agent connected to Reduck to run reduck/amazon.com.au/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.com.au/search-products

### Is there a amazon.com.au API to search Amazon.com.au products?

You do not need one. "Search Amazon.com.au products" drives the real amazon.com.au pages in a browser, so it works whether or not amazon.com.au offers an API for this.

### What information do I need to provide?

Required: query. Optional: page, sort, zipCode, price_max, price_min, department, refinements.

### What does it return?

It returns url, zip, page, items, query, currency, has_next_page.

### Do I need to be logged in to amazon.com.au?

No. It only uses pages of amazon.com.au that are reachable without signing in.

### Does it change anything on amazon.com.au, or only read data?

It only reads. It looks things up on amazon.com.au and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/amazon.com.au/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.com.au/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/amazon.com.au/search-products
