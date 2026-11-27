# Search Lowe's products

Automatically search Lowe's products on lowes.com. Search Lowes.com by free-text query and return one page of results (24 per page). Returns query, page, sort, total_count, page_count, has_next_page and items (item_id, title, brand, model, url, price, was_price, currency, image_url, rating, review_count, sponsored, marketplace, availability by fulfillment method). Sort by featured, best_sellers, price_low, price_high, highest_rated, brand or newest. A query with no match returns an empty list; Lowe's can also answer a query it does not understand with loosely related items. A page past page_count returns an empty list. Prices and availability follow the store Lowe's assigns to the browser's location. Lowe's serves US visitors and can refuse other networks.

- Site: lowes.com
- Address: `reduck/lowes.com/search-products`
- Updated: 2026-11-26 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/lowes.com/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/lowes.com/search-products
```

## Input

- `query` (string, required): Free-text search, e.g. "claw hammer".
- `page` (integer, optional): Results page, 24 items per page. Stop when has_next_page is false.
- `sort` (string, optional): Sort order. Omit for Lowe's default relevance.

## Output

- `page` (integer, required)
- `items` (array, required)
- `query` (string, required)
- `has_next_page` (boolean, required)
- `url` (string, optional)
- `sort` (string | null, optional)
- `store` (string | null, optional): Lowe's store whose prices and stock are shown.
- `page_count` (integer | null, optional)
- `total_count` (integer | null, optional)

## FAQ

### What does "Search Lowe's products" do?

Search Lowes.com by free-text query and return one page of results (24 per page). Returns query, page, sort, total_count, page_count, has_next_page and items (item_id, title, brand, model, url, price, was_price, currency, image_url, rating, review_count, sponsored, marketplace, availability by fulfillment method). Sort by featured, best_sellers, price_low, price_high, highest_rated, brand or newest. A query with no match returns an empty list; Lowe's can also answer a query it does not understand with loosely related items. A page past page_count returns an empty list. Prices and availability follow the store Lowe's assigns to the browser's location. Lowe's serves US visitors and can refuse other networks.

### How do I automatically search Lowe's products on lowes.com?

Ask an AI agent connected to Reduck to run reduck/lowes.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/lowes.com/search-products

### Is there a lowes.com API to search Lowe's products?

You do not need one. "Search Lowe's products" drives the real lowes.com pages in a browser, so it works whether or not lowes.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: page, sort.

### What does it return?

It returns url, page, sort, items, query, store, page_count, total_count, has_next_page.

### Do I need to be logged in to lowes.com?

No. It only uses pages of lowes.com that are reachable without signing in.

### Does it change anything on lowes.com, or only read data?

It only reads. It looks things up on lowes.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/lowes.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/lowes.com/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/lowes.com/search-products
