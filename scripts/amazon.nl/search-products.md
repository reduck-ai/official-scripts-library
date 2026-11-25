# Search Amazon.nl products

Automatically search Amazon.nl products on amazon.nl. Search Amazon.nl by free-text query, with Amazon's own filters: department, sort order, price range and refinements. Returns one page of results (asin, title, url, price, list_price, rating, review_count, image_url, sponsored, deal, badges, formats) with has_next_page. deal is the deal the card shows: its id, its label as Amazon writes it, and the end of its countdown when it shows one. badges are the other badges of the card, for example Amazon's Choice. Prices are in euros. Amazon.nl takes no postcode from a signed-out visitor (only a country), so the delivery location is the one the browser already has and zip is empty.

- Site: amazon.nl
- Address: `reduck/amazon.nl/search-products`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/amazon.nl/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/amazon.nl/search-products
```

## Input

- `query` (string, required): Free-text search query.
- `page` (integer, optional): Result page. has_next_page says when to stop.
- `sort` (string, optional): Sort order.
- `price_max` (number, optional): Maximum price in euros.
- `price_min` (number, optional): Minimum price in euros.
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

### What does "Search Amazon.nl products" do?

Search Amazon.nl by free-text query, with Amazon's own filters: department, sort order, price range and refinements. Returns one page of results (asin, title, url, price, list_price, rating, review_count, image_url, sponsored, deal, badges, formats) with has_next_page. deal is the deal the card shows: its id, its label as Amazon writes it, and the end of its countdown when it shows one. badges are the other badges of the card, for example Amazon's Choice. Prices are in euros. Amazon.nl takes no postcode from a signed-out visitor (only a country), so the delivery location is the one the browser already has and zip is empty.

### How do I automatically search Amazon.nl products on amazon.nl?

Ask an AI agent connected to Reduck to run reduck/amazon.nl/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.nl/search-products

### Is there a amazon.nl API to search Amazon.nl products?

You do not need one. "Search Amazon.nl products" drives the real amazon.nl pages in a browser, so it works whether or not amazon.nl offers an API for this.

### What information do I need to provide?

Required: query. Optional: page, sort, price_max, price_min, department, refinements.

### What does it return?

It returns url, zip, page, items, query, has_next_page.

### Do I need to be logged in to amazon.nl?

No. It only uses pages of amazon.nl that are reachable without signing in.

### Does it change anything on amazon.nl, or only read data?

It only reads. It looks things up on amazon.nl and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/amazon.nl/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.nl/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/amazon.nl/search-products
