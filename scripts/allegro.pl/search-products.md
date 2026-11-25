# Search Allegro products

Automatically search Allegro products on allegro.pl. Search Allegro (allegro.pl) offers by free-text query, with Allegro's own filters: category, sort order, price range in zloty, condition, offer type (buy now or auction), free delivery and Super Seller only. Returns one page of results: query, page, total_results, last_page, has_next_page and items (product_id, catalog_product_id, title, url, price, list_price, currency, rating, review_count, image_url, seller, delivery_price, price_with_delivery, free_delivery, promoted, sponsored). Prices are in Polish zloty (PLN). product_id is the offer number that Get Allegro product and Get Allegro product reviews take. Results include promoted and sponsored offers, marked as such. Allegro also answers a query that matches nothing exactly with loosely related offers; has_next_page is false on the last page. Brand, color and other category-specific filters are not offered.

- Site: allegro.pl
- Address: `reduck/allegro.pl/search-products`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/allegro.pl/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/allegro.pl/search-products
```

## Input

- `query` (string, required): Free-text search query, in Polish or English.
- `page` (integer, optional): Result page. last_page in the result says how far Allegro goes.
- `sort` (string, optional): Sort order: relevance (Allegro's default), price_asc, price_desc, price_with_delivery_asc, price_with_delivery_desc, popularity, ending_soon (auctions ending first), newest, product_rating.
- `condition` (string, optional): Item condition.
- `price_max` (number, optional): Maximum price in zloty.
- `price_min` (number, optional): Minimum price in zloty.
- `offer_type` (string, optional): buy_now: fixed-price offers only. auction: auctions only.
- `category_id` (string, optional): Allegro category id, as in the category_path ids of Get Allegro product or the number at the end of an allegro.pl/kategoria/ link.
- `free_delivery` (boolean, optional): Only offers with free delivery.
- `super_seller_only` (boolean, optional): Only offers from Super Sellers.

## Output

- `url` (string, required)
- `page` (integer, required)
- `items` (array, required)
- `query` (string, required)
- `last_page` (integer | null, required): Last result page Allegro serves.
- `has_next_page` (boolean, required)
- `total_results` (integer | null, required): Number of matching offers Allegro reports.

## FAQ

### What does "Search Allegro products" do?

Search Allegro (allegro.pl) offers by free-text query, with Allegro's own filters: category, sort order, price range in zloty, condition, offer type (buy now or auction), free delivery and Super Seller only. Returns one page of results: query, page, total_results, last_page, has_next_page and items (product_id, catalog_product_id, title, url, price, list_price, currency, rating, review_count, image_url, seller, delivery_price, price_with_delivery, free_delivery, promoted, sponsored). Prices are in Polish zloty (PLN). product_id is the offer number that Get Allegro product and Get Allegro product reviews take. Results include promoted and sponsored offers, marked as such. Allegro also answers a query that matches nothing exactly with loosely related offers; has_next_page is false on the last page. Brand, color and other category-specific filters are not offered.

### How do I automatically search Allegro products on allegro.pl?

Ask an AI agent connected to Reduck to run reduck/allegro.pl/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/allegro.pl/search-products

### Is there a allegro.pl API to search Allegro products?

You do not need one. "Search Allegro products" drives the real allegro.pl pages in a browser, so it works whether or not allegro.pl offers an API for this.

### What information do I need to provide?

Required: query. Optional: page, sort, condition, price_max, price_min, offer_type, category_id, free_delivery, super_seller_only.

### What does it return?

It returns url, page, items, query, last_page, has_next_page, total_results.

### Do I need to be logged in to allegro.pl?

No. It only uses pages of allegro.pl that are reachable without signing in.

### Does it change anything on allegro.pl, or only read data?

It only reads. It looks things up on allegro.pl and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/allegro.pl/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/allegro.pl/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/allegro.pl/search-products
