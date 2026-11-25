# Search Amazon.com.br products

Automatically search Amazon.com.br products on amazon.com.br. Search Amazon.com.br by free-text query, with Amazon's own filters: department, sort order, price range and refinements. Returns one page of results (asin, title, url, price, list_price, rating, review_count, image_url, sponsored, deal, badges, formats) with has_next_page. deal is the deal the card shows: its id, its label as Amazon writes it, and the end of its countdown when it shows one. badges are the other badges of the card, for example Amazon's Choice. Prices are in reais, pinned to a Brazilian postcode.

- Site: amazon.com.br
- Address: `reduck/amazon.com.br/search-products`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/amazon.com.br/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/amazon.com.br/search-products
```

## Input

- `query` (string, required): Free-text search query.
- `page` (integer, optional): Result page. has_next_page says when to stop.
- `sort` (string, optional): Sort order.
- `zipCode` (string, optional): Brazilian postcode used to pin the store location (prices, availability).
- `price_max` (number, optional): Maximum price in reais.
- `price_min` (number, optional): Minimum price in reais.
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

### What does "Search Amazon.com.br products" do?

Search Amazon.com.br by free-text query, with Amazon's own filters: department, sort order, price range and refinements. Returns one page of results (asin, title, url, price, list_price, rating, review_count, image_url, sponsored, deal, badges, formats) with has_next_page. deal is the deal the card shows: its id, its label as Amazon writes it, and the end of its countdown when it shows one. badges are the other badges of the card, for example Amazon's Choice. Prices are in reais, pinned to a Brazilian postcode.

### How do I automatically search Amazon.com.br products on amazon.com.br?

Ask an AI agent connected to Reduck to run reduck/amazon.com.br/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.com.br/search-products

### Is there a amazon.com.br API to search Amazon.com.br products?

You do not need one. "Search Amazon.com.br products" drives the real amazon.com.br pages in a browser, so it works whether or not amazon.com.br offers an API for this.

### What information do I need to provide?

Required: query. Optional: page, sort, zipCode, price_max, price_min, department, refinements.

### What does it return?

It returns url, zip, page, items, query, has_next_page.

### Do I need to be logged in to amazon.com.br?

No. It only uses pages of amazon.com.br that are reachable without signing in.

### Does it change anything on amazon.com.br, or only read data?

It only reads. It looks things up on amazon.com.br and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/amazon.com.br/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.com.br/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/amazon.com.br/search-products
