# Search Amazon.se products

Automatically search Amazon.se products on amazon.se. Search Amazon.se by free-text query, with Amazon's own filters: department, sort order, price range and refinements. Returns one page of results (asin, title, url, price, list_price, rating, review_count, image_url, sponsored, deal, badges, formats) with has_next_page. deal is the deal the card shows: its id, its label as Amazon writes it, and the end of its countdown when it shows one. badges are the other badges of the card. Prices are in Swedish kronor, pinned to a Swedish postcode.

- Site: amazon.se
- Address: `reduck/amazon.se/search-products`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/amazon.se/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/amazon.se/search-products
```

## Input

- `query` (string, required): Free-text search query.
- `page` (integer, optional): Result page. has_next_page says when to stop.
- `sort` (string, optional): Sort order.
- `zipCode` (string, optional): Swedish postcode used to pin the store location (prices, availability).
- `price_max` (number, optional): Maximum price in Swedish kronor.
- `price_min` (number, optional): Minimum price in Swedish kronor.
- `department` (string, optional): Department search alias, as in Amazon's i= URL parameter.
- `refinements` (array, optional): Filters as group:value, as in Amazon's rh= URL parameter.

## Output

- `url` (string, required)
- `zip` (string, required)
- `page` (integer, required)
- `items` (array, required)
- `query` (string, required)
- `has_next_page` (boolean, required)

## FAQ

### What does "Search Amazon.se products" do?

Search Amazon.se by free-text query, with Amazon's own filters: department, sort order, price range and refinements. Returns one page of results (asin, title, url, price, list_price, rating, review_count, image_url, sponsored, deal, badges, formats) with has_next_page. deal is the deal the card shows: its id, its label as Amazon writes it, and the end of its countdown when it shows one. badges are the other badges of the card. Prices are in Swedish kronor, pinned to a Swedish postcode.

### How do I automatically search Amazon.se products on amazon.se?

Ask an AI agent connected to Reduck to run reduck/amazon.se/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.se/search-products

### Is there a amazon.se API to search Amazon.se products?

You do not need one. "Search Amazon.se products" drives the real amazon.se pages in a browser, so it works whether or not amazon.se offers an API for this.

### What information do I need to provide?

Required: query. Optional: page, sort, zipCode, price_max, price_min, department, refinements.

### What does it return?

It returns url, zip, page, items, query, has_next_page.

### Do I need to be logged in to amazon.se?

No. It only uses pages of amazon.se that are reachable without signing in.

### Does it change anything on amazon.se, or only read data?

It only reads. It looks things up on amazon.se and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/amazon.se/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.se/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/amazon.se/search-products
