# Search Office Depot products

Automatically search Office Depot products on officedepot.com. Search OfficeDepot.com by free-text query and return one page of results (24 per page), sorted by relevance, newest, rating or price. Returns the total count, the page count, has_next_page and, for each product, its item number, link, title, brand, selling, regular and list price in US dollars, unit, image, rating, review count, whether it is sponsored, availability as Office Depot states it, delivery days and category. A query that is an item number returns that one product. Office Depot answers a query it does not understand with loosely related products, not with an empty list. A page past the last one returns an empty list. Stock and delivery estimates follow the store and ZIP code Office Depot assigns to a new guest browser (store_id and delivery_zip).

- Site: officedepot.com
- Address: `reduck/officedepot.com/search-products`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/officedepot.com/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/officedepot.com/search-products
```

## Input

- `query` (string, required): Free-text search, e.g. "stapler".
- `page` (integer, optional): Results page, 24 items per page. Stop when has_next_page is false.
- `sort` (string, optional): Sort order: relevance (the site's default), newest, rating, price_low or price_high.

## Output

- `page` (integer, required)
- `sort` (string, required)
- `items` (array, required)
- `query` (string, required)
- `page_count` (integer | null, required)
- `total_count` (integer | null, required): Number of results Office Depot gives for the query.
- `has_next_page` (boolean, required)
- `store_id` (string | null, optional): Office Depot store whose pickup stock is shown.
- `delivery_zip` (string | null, optional): ZIP code Office Depot uses for delivery estimates.

## FAQ

### What does "Search Office Depot products" do?

Search OfficeDepot.com by free-text query and return one page of results (24 per page), sorted by relevance, newest, rating or price. Returns the total count, the page count, has_next_page and, for each product, its item number, link, title, brand, selling, regular and list price in US dollars, unit, image, rating, review count, whether it is sponsored, availability as Office Depot states it, delivery days and category. A query that is an item number returns that one product. Office Depot answers a query it does not understand with loosely related products, not with an empty list. A page past the last one returns an empty list. Stock and delivery estimates follow the store and ZIP code Office Depot assigns to a new guest browser (store_id and delivery_zip).

### How do I automatically search Office Depot products on officedepot.com?

Ask an AI agent connected to Reduck to run reduck/officedepot.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/officedepot.com/search-products

### Is there a officedepot.com API to search Office Depot products?

You do not need one. "Search Office Depot products" drives the real officedepot.com pages in a browser, so it works whether or not officedepot.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: page, sort.

### What does it return?

It returns page, sort, items, query, store_id, page_count, total_count, delivery_zip, has_next_page.

### Do I need to be logged in to officedepot.com?

No. It only uses pages of officedepot.com that are reachable without signing in.

### Does it change anything on officedepot.com, or only read data?

It only reads. It looks things up on officedepot.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/officedepot.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/officedepot.com/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/officedepot.com/search-products
