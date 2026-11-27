# Search Rakuten products

Automatically search Rakuten products on rakuten.co.jp. Search Rakuten Ichiba (rakuten.co.jp) by free-text query, with Rakuten's own filters: sort order, price range in yen, genre, minimum review score, shipping speed or free shipping, Super Deal items only, sold-out items included, words to exclude, any-word matching and title-only matching. Returns one page of 45 results plus the shop ads Rakuten adds at the end: query, page, total_results, has_next_page and items (product_id, title, url, price, price_max, currency, rating, review_count, image_url, shop, condition, availability, free_shipping, points, genre_ids, sponsored). Prices are in Japanese yen, tax included. product_id is the id Get Rakuten product and Get Rakuten product reviews take. Rakuten shows at most 150 pages; has_next_page is false on the last page and when nothing matches, and then items is empty. Gift-wrapping and subscription filters are not offered.

- Site: rakuten.co.jp
- Address: `reduck/rakuten.co.jp/search-products`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/rakuten.co.jp/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/rakuten.co.jp/search-products
```

## Input

- `query` (string, required): Free-text search query, in Japanese or English.
- `page` (integer, optional): Result page, 45 results a page. Rakuten stops at page 150.
- `sort` (string, optional): Sort order: standard (Rakuten's default), price_asc, price_desc, price_with_shipping_asc, price_with_shipping_desc, newest, review_count (most reviews), review_score (best average).
- `genre_id` (string, optional): Rakuten genre (category) id, as in the genre_ids of a result or the number in a rakuten.co.jp/category/<id>/ link.
- `shipping` (string, optional): free: free shipping only. free_or_threshold: free shipping, or free above the shop's order threshold. next_day: delivery the next day. within_two_days: delivery within two days. Rakuten takes one of these at a time.
- `price_max` (integer, optional): Maximum price in yen.
- `price_min` (integer, optional): Minimum price in yen.
- `title_only` (boolean, optional): Match the query against item titles only.
- `exclude_words` (string, optional): Words that results must not contain, separated by spaces.
- `match_any_word` (boolean, optional): Match items that contain any of the query words, not all of them.
- `super_deal_only` (boolean, optional): Only Super Deal items (extra points back).
- `include_sold_out` (boolean, optional): Also show sold-out items.
- `min_review_score` (string, optional): Only items with at least this average review score.

## Output

- `url` (string, required): The search page that was read.
- `page` (integer, required)
- `items` (array, required)
- `query` (string, required)
- `has_next_page` (boolean, required)
- `total_results` (integer | null, required): Number of matching items Rakuten reports.

## FAQ

### What does "Search Rakuten products" do?

Search Rakuten Ichiba (rakuten.co.jp) by free-text query, with Rakuten's own filters: sort order, price range in yen, genre, minimum review score, shipping speed or free shipping, Super Deal items only, sold-out items included, words to exclude, any-word matching and title-only matching. Returns one page of 45 results plus the shop ads Rakuten adds at the end: query, page, total_results, has_next_page and items (product_id, title, url, price, price_max, currency, rating, review_count, image_url, shop, condition, availability, free_shipping, points, genre_ids, sponsored). Prices are in Japanese yen, tax included. product_id is the id Get Rakuten product and Get Rakuten product reviews take. Rakuten shows at most 150 pages; has_next_page is false on the last page and when nothing matches, and then items is empty. Gift-wrapping and subscription filters are not offered.

### How do I automatically search Rakuten products on rakuten.co.jp?

Ask an AI agent connected to Reduck to run reduck/rakuten.co.jp/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/rakuten.co.jp/search-products

### Is there a rakuten.co.jp API to search Rakuten products?

You do not need one. "Search Rakuten products" drives the real rakuten.co.jp pages in a browser, so it works whether or not rakuten.co.jp offers an API for this.

### What information do I need to provide?

Required: query. Optional: page, sort, genre_id, shipping, price_max, price_min, title_only, exclude_words, match_any_word, super_deal_only, include_sold_out, min_review_score.

### What does it return?

It returns url, page, items, query, has_next_page, total_results.

### Do I need to be logged in to rakuten.co.jp?

No. It only uses pages of rakuten.co.jp that are reachable without signing in.

### Does it change anything on rakuten.co.jp, or only read data?

It only reads. It looks things up on rakuten.co.jp and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/rakuten.co.jp/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/rakuten.co.jp/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/rakuten.co.jp/search-products
