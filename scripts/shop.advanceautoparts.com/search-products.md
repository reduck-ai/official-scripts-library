# Search Advance Auto Parts products

Automatically search Advance Auto Parts products on shop.advanceautoparts.com. Search Advance Auto Parts (shop.advanceautoparts.com) by keyword or part number. Returns one page of 18 results in the order the site shows them: total_results, total_pages, has_next_page, the store whose prices and stock apply, the filters the site shows with their counts, and items (product_id, name, brand, part_number, category, url, image_url, rating, review_count, price, regular_price, list_price, on_sale, sale_percent, store_status, store_quantity, core_charge). Prices are in US dollars, for the store the site picks for a new visitor. When the query is a general term, the site shows a category instead, and category says which. When the query is a part number, the site lists interchangeable parts, marked interchangeable. Filters and sort orders are not offered. A page past the last one is refused with an error.

- Site: shop.advanceautoparts.com
- Address: `reduck/shop.advanceautoparts.com/search-products`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/shop.advanceautoparts.com/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/shop.advanceautoparts.com/search-products
```

## Input

- `query` (string, required): Keyword or part number, for example "brake pads" or "PH7317".
- `page` (integer, optional): Result page, 18 results each. total_pages in the result says how far the site goes.

## Output

- `url` (string, required)
- `page` (integer, required)
- `items` (array, required)
- `query` (string, required)
- `facets` (array, required)
- `total_results` (integer, required): Number of matching products, not counting interchangeable parts.
- `category` (object | null, optional): The category the site shows for this query, or null when it shows search results.
- `store_id` (string | null, optional): The Advance Auto Parts store whose prices and stock apply.
- `total_pages` (integer | null, optional)
- `has_next_page` (boolean, optional)
- `searched_phrase` (string | null, optional): The phrase the site searched for.

## FAQ

### What does "Search Advance Auto Parts products" do?

Search Advance Auto Parts (shop.advanceautoparts.com) by keyword or part number. Returns one page of 18 results in the order the site shows them: total_results, total_pages, has_next_page, the store whose prices and stock apply, the filters the site shows with their counts, and items (product_id, name, brand, part_number, category, url, image_url, rating, review_count, price, regular_price, list_price, on_sale, sale_percent, store_status, store_quantity, core_charge). Prices are in US dollars, for the store the site picks for a new visitor. When the query is a general term, the site shows a category instead, and category says which. When the query is a part number, the site lists interchangeable parts, marked interchangeable. Filters and sort orders are not offered. A page past the last one is refused with an error.

### How do I automatically search Advance Auto Parts products on shop.advanceautoparts.com?

Ask an AI agent connected to Reduck to run reduck/shop.advanceautoparts.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/shop.advanceautoparts.com/search-products

### Is there a shop.advanceautoparts.com API to search Advance Auto Parts products?

You do not need one. "Search Advance Auto Parts products" drives the real shop.advanceautoparts.com pages in a browser, so it works whether or not shop.advanceautoparts.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: page.

### What does it return?

It returns url, page, items, query, facets, category, store_id, total_pages, has_next_page, total_results, searched_phrase.

### Do I need to be logged in to shop.advanceautoparts.com?

No. It only uses pages of shop.advanceautoparts.com that are reachable without signing in.

### Does it change anything on shop.advanceautoparts.com, or only read data?

It only reads. It looks things up on shop.advanceautoparts.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/shop.advanceautoparts.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/shop.advanceautoparts.com/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/shop.advanceautoparts.com/search-products
