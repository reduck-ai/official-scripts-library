# Search eBay products

Automatically search eBay products on ebay.com. Search eBay (ebay.com) by keyword, one page of 60 listings at a time. Returns eBay's result count, whether a next page exists, and for each listing its item id (the productId other eBay scripts take), title, link, price, currency, shipping cost, image and the card's attribute lines (buying format, location, returns, seller feedback) verbatim. Listings eBay pads a short result with are returned apart in related. A query with no match returns an empty list with eBay's notice when it gives one. A page past the last one returns an empty list. Sold items need a signed-in browser and are not offered.

- Site: ebay.com
- Address: `reduck/ebay.com/search-products`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/ebay.com/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/ebay.com/search-products
```

## Input

- `query` (string, required): Search keywords, e.g. "lego star wars".
- `page` (integer, optional): Result page, 60 listings each. has_next_page says when to stop.
- `sort` (string, optional): eBay's sort options.

## Output

- `page` (integer, required)
- `items` (array, required): Listings that match the query.
- `query` (string, required)
- `related` (array, required): Listings eBay adds below the matches when they run out. They are not matches for the query.
- `has_next_page` (boolean, required)
- `total` (integer | null, optional): The number in that heading (a lower bound when it ends with +).
- `total_text` (string | null, optional): eBay's count heading, verbatim ("260,000+ results for lego star wars").
- `empty_reason` (string | null, optional): eBay's notice when it shows no result and says why; null otherwise.

## FAQ

### What does "Search eBay products" do?

Search eBay (ebay.com) by keyword, one page of 60 listings at a time. Returns eBay's result count, whether a next page exists, and for each listing its item id (the productId other eBay scripts take), title, link, price, currency, shipping cost, image and the card's attribute lines (buying format, location, returns, seller feedback) verbatim. Listings eBay pads a short result with are returned apart in related. A query with no match returns an empty list with eBay's notice when it gives one. A page past the last one returns an empty list. Sold items need a signed-in browser and are not offered.

### How do I automatically search eBay products on ebay.com?

Ask an AI agent connected to Reduck to run reduck/ebay.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/ebay.com/search-products

### Is there a ebay.com API to search eBay products?

You do not need one. "Search eBay products" drives the real ebay.com pages in a browser, so it works whether or not ebay.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: page, sort.

### What does it return?

It returns page, items, query, total, related, total_text, empty_reason, has_next_page.

### Do I need to be logged in to ebay.com?

No. It only uses pages of ebay.com that are reachable without signing in.

### Does it change anything on ebay.com, or only read data?

It only reads. It looks things up on ebay.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/ebay.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/ebay.com/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/ebay.com/search-products
