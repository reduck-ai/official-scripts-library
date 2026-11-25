# Search Amazon.co.uk products

Automatically search Amazon.co.uk products on amazon.co.uk. Search Amazon.co.uk by free-text query, with Amazon's own filters: department, sort order, price range and refinements. Returns one page of results (asin, title, url, price, list_price, rating, review_count, image_url, sponsored, deal, badges, formats) with has_next_page. deal is the deal the card shows: its id, its label as Amazon writes it (for example "Early Black Friday"), and the end of its countdown when it shows one. badges are the other badges of the card, for example Amazon's Choice or a sustainability label. Prices are in pounds sterling, pinned to a UK postcode.

- Site: amazon.co.uk
- Address: `reduck/amazon.co.uk/search-products`
- Updated: 2026-11-24 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/amazon.co.uk/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/amazon.co.uk/search-products
```

## Input

- `query` (string, required): Free-text search query.
- `page` (integer, optional): Result page. has_next_page says when to stop.
- `sort` (string, optional): Sort order.
- `zipCode` (string, optional): UK postcode used to pin the store location (prices, availability).
- `price_max` (number, optional): Maximum price in pounds sterling.
- `price_min` (number, optional): Minimum price in pounds sterling.
- `department` (string, optional): Department search alias, from list_search_filters.
- `refinements` (array, optional): Filters as group:value, from list_search_filters for the same query.

## Output

- `url` (string, required)
- `zip` (string, required)
- `page` (integer, required)
- `items` (array, required)
- `query` (string, required)
- `has_next_page` (boolean, required)

## FAQ

### What does "Search Amazon.co.uk products" do?

Search Amazon.co.uk by free-text query, with Amazon's own filters: department, sort order, price range and refinements. Returns one page of results (asin, title, url, price, list_price, rating, review_count, image_url, sponsored, deal, badges, formats) with has_next_page. deal is the deal the card shows: its id, its label as Amazon writes it (for example "Early Black Friday"), and the end of its countdown when it shows one. badges are the other badges of the card, for example Amazon's Choice or a sustainability label. Prices are in pounds sterling, pinned to a UK postcode.

### How do I automatically search Amazon.co.uk products on amazon.co.uk?

Ask an AI agent connected to Reduck to run reduck/amazon.co.uk/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.co.uk/search-products

### Is there a amazon.co.uk API to search Amazon.co.uk products?

You do not need one. "Search Amazon.co.uk products" drives the real amazon.co.uk pages in a browser, so it works whether or not amazon.co.uk offers an API for this.

### What information do I need to provide?

Required: query. Optional: page, sort, zipCode, price_max, price_min, department, refinements.

### What does it return?

It returns url, zip, page, items, query, has_next_page.

### Do I need to be logged in to amazon.co.uk?

No. It only uses pages of amazon.co.uk that are reachable without signing in.

### Does it change anything on amazon.co.uk, or only read data?

It only reads. It looks things up on amazon.co.uk and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/amazon.co.uk/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.co.uk/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/amazon.co.uk/search-products
