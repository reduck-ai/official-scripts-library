# Search noon products

Automatically search noon products on noon.com. Search noon (noon.com) by free-text query in the UAE, Saudi Arabia or Egypt store, with noon's sort order, a price range and a brand filter. Returns one page of results: query, country, currency, page, total_results, total_pages, has_next_page and items (product_id, title, brand, brand_code, url, price, list_price, currency, rating, review_count, image_url, availability, seller, express, bestseller, sponsored). A page has 50 results plus the sponsored products noon places among them, marked as sponsored. Prices are in the currency of the store: UAE dirham for the UAE, Saudi riyal for Saudi Arabia, Egyptian pound for Egypt. price is the price the card asks, list_price the struck-through price. Titles are in English, except for products noon lists only in Arabic. noon answers a query that matches nothing with loosely related products. Other noon filters (category, delivery speed, deals, category-specific attributes) are not offered.

- Site: noon.com
- Address: `reduck/noon.com/search-products`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/noon.com/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/noon.com/search-products
```

## Input

- `query` (string, required): Free-text search query.
- `page` (integer, optional): Result page, 50 results a page. total_pages says how far noon goes.
- `sort` (string, optional): Sort order: recommended (noon's default), price_asc, price_desc, newest, rating (highest rated first).
- `brands` (array, optional): noon brand codes, as in the brand_code of a Search noon products result (for example apple, samsung). Several brands are alternatives.
- `country` (string, optional): The noon store: uae (prices in UAE dirham), saudi (Saudi riyal) or egypt (Egyptian pound).
- `price_max` (number, optional): Maximum price, in the currency of the store.
- `price_min` (number, optional): Minimum price, in the currency of the store.

## Output

- `url` (string, required)
- `page` (integer, required)
- `items` (array, required)
- `query` (string, required)
- `country` (string, required)
- `total_pages` (integer | null, required)
- `has_next_page` (boolean, required)
- `total_results` (integer | null, required): Number of matching products noon reports.
- `currency` (string, optional)

## FAQ

### What does "Search noon products" do?

Search noon (noon.com) by free-text query in the UAE, Saudi Arabia or Egypt store, with noon's sort order, a price range and a brand filter. Returns one page of results: query, country, currency, page, total_results, total_pages, has_next_page and items (product_id, title, brand, brand_code, url, price, list_price, currency, rating, review_count, image_url, availability, seller, express, bestseller, sponsored). A page has 50 results plus the sponsored products noon places among them, marked as sponsored. Prices are in the currency of the store: UAE dirham for the UAE, Saudi riyal for Saudi Arabia, Egyptian pound for Egypt. price is the price the card asks, list_price the struck-through price. Titles are in English, except for products noon lists only in Arabic. noon answers a query that matches nothing with loosely related products. Other noon filters (category, delivery speed, deals, category-specific attributes) are not offered.

### How do I automatically search noon products on noon.com?

Ask an AI agent connected to Reduck to run reduck/noon.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/noon.com/search-products

### Is there a noon.com API to search noon products?

You do not need one. "Search noon products" drives the real noon.com pages in a browser, so it works whether or not noon.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: page, sort, brands, country, price_max, price_min.

### What does it return?

It returns url, page, items, query, country, currency, total_pages, has_next_page, total_results.

### Do I need to be logged in to noon.com?

No. It only uses pages of noon.com that are reachable without signing in.

### Does it change anything on noon.com, or only read data?

It only reads. It looks things up on noon.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/noon.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/noon.com/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/noon.com/search-products
