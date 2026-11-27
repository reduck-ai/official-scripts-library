# Search John Lewis products

Automatically search John Lewis products on johnlewis.com. Search the John Lewis UK store (johnlewis.com) by free-text query and return one page of products (72 per page) in the site's relevance order. Returns the query, page, total count, page count (stated on page 1 only), has_next_page, the searches John Lewis suggests, and items: product number, link, title, brand, lowest and highest price in pounds sterling, earlier price when reduced, image, rating, review count, availability, default sku id, colours with their sku ids, and offer labels. A query with no match returns an empty list; John Lewis can also answer a query it cannot match with a list of popular products, which the script returns as the site shows it. A page past the last one returns an empty list.

- Site: johnlewis.com
- Address: `reduck/johnlewis.com/search-products`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/johnlewis.com/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/johnlewis.com/search-products
```

## Input

- `query` (string, required): Free-text search, for example "kettle".
- `page` (integer, optional): Results page, 72 products per page. Stop when has_next_page is false.

## Output

- `url` (string, required)
- `page` (integer, required)
- `items` (array, required)
- `query` (string, required)
- `currency` (string, required): GBP
- `page_count` (integer | null, required): Number of pages John Lewis states; it states it on page 1 only.
- `suggestions` (array, required): Other searches John Lewis suggests for this query.
- `total_count` (integer | null, required): Number of products John Lewis states for the search; null on a page past the end.
- `has_next_page` (boolean, required)

## FAQ

### What does "Search John Lewis products" do?

Search the John Lewis UK store (johnlewis.com) by free-text query and return one page of products (72 per page) in the site's relevance order. Returns the query, page, total count, page count (stated on page 1 only), has_next_page, the searches John Lewis suggests, and items: product number, link, title, brand, lowest and highest price in pounds sterling, earlier price when reduced, image, rating, review count, availability, default sku id, colours with their sku ids, and offer labels. A query with no match returns an empty list; John Lewis can also answer a query it cannot match with a list of popular products, which the script returns as the site shows it. A page past the last one returns an empty list.

### How do I automatically search John Lewis products on johnlewis.com?

Ask an AI agent connected to Reduck to run reduck/johnlewis.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/johnlewis.com/search-products

### Is there a johnlewis.com API to search John Lewis products?

You do not need one. "Search John Lewis products" drives the real johnlewis.com pages in a browser, so it works whether or not johnlewis.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: page.

### What does it return?

It returns url, page, items, query, currency, page_count, suggestions, total_count, has_next_page.

### Do I need to be logged in to johnlewis.com?

No. It only uses pages of johnlewis.com that are reachable without signing in.

### Does it change anything on johnlewis.com, or only read data?

It only reads. It looks things up on johnlewis.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/johnlewis.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/johnlewis.com/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/johnlewis.com/search-products
