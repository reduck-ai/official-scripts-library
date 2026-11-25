# Search Flipkart products

Automatically search Flipkart products on flipkart.com. Search Flipkart India (flipkart.com) by free-text query, with Flipkart's sort order, a price range in rupees and a brand filter. Returns one page of results: query, searched_query, page, total_results, total_pages, has_next_page and items (product_id, title, brand, url, price, list_price, currency, rating, rating_count, review_count, image_url, availability, flipkart_assured, sponsored). Prices are in Indian rupees (INR); price is the selling price the card shows, list_price the struck-through maximum retail price. Sponsored results are included and marked. When Flipkart finds no match for the query, it searches for a corrected or shorter query instead: searched_query says which. Other Flipkart filters (category-specific attributes, rating, discount, Flipkart Assured) are not offered.

- Site: flipkart.com
- Address: `reduck/flipkart.com/search-products`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/flipkart.com/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/flipkart.com/search-products
```

## Input

- `query` (string, required): Free-text search query.
- `page` (integer, optional): Result page. total_pages in the result says how far Flipkart goes.
- `sort` (string, optional): Sort order: relevance (Flipkart's default), popularity, price_asc, price_desc, newest.
- `brands` (array, optional): Brand names as Flipkart writes them, for example the brand of a Search Flipkart products result ("Apple", "Samsung"). Several brands are alternatives.
- `price_max` (number, optional): Maximum price in rupees.
- `price_min` (number, optional): Minimum price in rupees.

## Output

- `url` (string, required)
- `page` (integer, required)
- `items` (array, required)
- `query` (string, required)
- `total_pages` (integer | null, required)
- `has_next_page` (boolean, required)
- `total_results` (integer | null, required): Number of matching products Flipkart reports.
- `searched_query` (string | null, optional): The query Flipkart searched for. It differs from query when Flipkart corrected the spelling or found no match and searched for a part of it.

## FAQ

### What does "Search Flipkart products" do?

Search Flipkart India (flipkart.com) by free-text query, with Flipkart's sort order, a price range in rupees and a brand filter. Returns one page of results: query, searched_query, page, total_results, total_pages, has_next_page and items (product_id, title, brand, url, price, list_price, currency, rating, rating_count, review_count, image_url, availability, flipkart_assured, sponsored). Prices are in Indian rupees (INR); price is the selling price the card shows, list_price the struck-through maximum retail price. Sponsored results are included and marked. When Flipkart finds no match for the query, it searches for a corrected or shorter query instead: searched_query says which. Other Flipkart filters (category-specific attributes, rating, discount, Flipkart Assured) are not offered.

### How do I automatically search Flipkart products on flipkart.com?

Ask an AI agent connected to Reduck to run reduck/flipkart.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/flipkart.com/search-products

### Is there a flipkart.com API to search Flipkart products?

You do not need one. "Search Flipkart products" drives the real flipkart.com pages in a browser, so it works whether or not flipkart.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: page, sort, brands, price_max, price_min.

### What does it return?

It returns url, page, items, query, total_pages, has_next_page, total_results, searched_query.

### Do I need to be logged in to flipkart.com?

No. It only uses pages of flipkart.com that are reachable without signing in.

### Does it change anything on flipkart.com, or only read data?

It only reads. It looks things up on flipkart.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/flipkart.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/flipkart.com/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/flipkart.com/search-products
