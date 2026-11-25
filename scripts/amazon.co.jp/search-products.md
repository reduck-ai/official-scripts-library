# Search Amazon.co.jp products

Automatically search Amazon.co.jp products on amazon.co.jp. Search Amazon.co.jp by free-text query, with Amazon's own filters: department, sort order, price range and refinements. Returns one page of results (asin, title, url, price, list_price, rating, review_count, image_url, sponsored, deal, badges, formats) with has_next_page. deal is the deal the card shows: its id, its label as Amazon writes it, and the end of its countdown when it shows one. badges are the other badges of the card, for example Amazon's Choice. Prices are in the currency the page shows (Japanese yen unless the browser asks Amazon for another), pinned to a Japanese postcode.

- Site: amazon.co.jp
- Address: `reduck/amazon.co.jp/search-products`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/amazon.co.jp/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/amazon.co.jp/search-products
```

## Input

- `query` (string, required): Free-text search query.
- `page` (integer, optional): Result page. has_next_page says when to stop.
- `sort` (string, optional): Sort order.
- `zipCode` (string, optional): Japanese postcode used to pin the store location (prices, availability).
- `price_max` (number, optional): Maximum price, in the currency the page shows.
- `price_min` (number, optional): Minimum price, in the currency the page shows.
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

### What does "Search Amazon.co.jp products" do?

Search Amazon.co.jp by free-text query, with Amazon's own filters: department, sort order, price range and refinements. Returns one page of results (asin, title, url, price, list_price, rating, review_count, image_url, sponsored, deal, badges, formats) with has_next_page. deal is the deal the card shows: its id, its label as Amazon writes it, and the end of its countdown when it shows one. badges are the other badges of the card, for example Amazon's Choice. Prices are in the currency the page shows (Japanese yen unless the browser asks Amazon for another), pinned to a Japanese postcode.

### How do I automatically search Amazon.co.jp products on amazon.co.jp?

Ask an AI agent connected to Reduck to run reduck/amazon.co.jp/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.co.jp/search-products

### Is there a amazon.co.jp API to search Amazon.co.jp products?

You do not need one. "Search Amazon.co.jp products" drives the real amazon.co.jp pages in a browser, so it works whether or not amazon.co.jp offers an API for this.

### What information do I need to provide?

Required: query. Optional: page, sort, zipCode, price_max, price_min, department, refinements.

### What does it return?

It returns url, zip, page, items, query, has_next_page.

### Do I need to be logged in to amazon.co.jp?

No. It only uses pages of amazon.co.jp that are reachable without signing in.

### Does it change anything on amazon.co.jp, or only read data?

It only reads. It looks things up on amazon.co.jp and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/amazon.co.jp/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.co.jp/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/amazon.co.jp/search-products
