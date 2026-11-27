# Search Hepsiburada products

Automatically search Hepsiburada products on hepsiburada.com. Search Hepsiburada (hepsiburada.com) by free-text query, with Hepsiburada's sort order, a price range in Turkish lira and a brand filter. Returns one page of up to 36 results: query, page, total_results, last_page, has_next_page and items (product_id, title, brand, url, price, list_price, currency, rating, review_count, image_url, availability, seller, sponsored). Prices are in Turkish lira; price is what the card asks, list_price the struck-through price. Sponsored results are included and marked. Hepsiburada can narrow a search to the category the query matches best, as its own page does. A page past the last one returns no items. Other Hepsiburada filters (category, seller, rating, delivery speed, category-specific attributes) are not offered.

- Site: hepsiburada.com
- Address: `reduck/hepsiburada.com/search-products`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/hepsiburada.com/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/hepsiburada.com/search-products
```

## Input

- `query` (string, required): Free-text search query, in Turkish or English.
- `page` (integer, optional): Result page, 36 results a page. last_page says how far Hepsiburada goes.
- `sort` (string, optional): Sort order: recommended (Hepsiburada's default), price_asc, price_desc, best_selling, most_reviewed, top_rated, discount (highest discount first), newest.
- `brands` (array, optional): Hepsiburada brand codes, as in the brand_code of Get Hepsiburada product (for example apple, philips). Several brands are alternatives.
- `price_max` (number, optional): Maximum price in Turkish lira. Give it with price_min.
- `price_min` (number, optional): Minimum price in Turkish lira. Give it with price_max.

## Output

- `url` (string, required)
- `page` (integer, required)
- `items` (array, required)
- `query` (string, required)
- `last_page` (integer | null, required)
- `has_next_page` (boolean, required)
- `total_results` (integer | null, required): Number of matching products Hepsiburada reports. It caps the count at 10000.

## FAQ

### What does "Search Hepsiburada products" do?

Search Hepsiburada (hepsiburada.com) by free-text query, with Hepsiburada's sort order, a price range in Turkish lira and a brand filter. Returns one page of up to 36 results: query, page, total_results, last_page, has_next_page and items (product_id, title, brand, url, price, list_price, currency, rating, review_count, image_url, availability, seller, sponsored). Prices are in Turkish lira; price is what the card asks, list_price the struck-through price. Sponsored results are included and marked. Hepsiburada can narrow a search to the category the query matches best, as its own page does. A page past the last one returns no items. Other Hepsiburada filters (category, seller, rating, delivery speed, category-specific attributes) are not offered.

### How do I automatically search Hepsiburada products on hepsiburada.com?

Ask an AI agent connected to Reduck to run reduck/hepsiburada.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/hepsiburada.com/search-products

### Is there a hepsiburada.com API to search Hepsiburada products?

You do not need one. "Search Hepsiburada products" drives the real hepsiburada.com pages in a browser, so it works whether or not hepsiburada.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: page, sort, brands, price_max, price_min.

### What does it return?

It returns url, page, items, query, last_page, has_next_page, total_results.

### Do I need to be logged in to hepsiburada.com?

No. It only uses pages of hepsiburada.com that are reachable without signing in.

### Does it change anything on hepsiburada.com, or only read data?

It only reads. It looks things up on hepsiburada.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/hepsiburada.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/hepsiburada.com/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/hepsiburada.com/search-products
