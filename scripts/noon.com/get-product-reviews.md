# Get noon product reviews

Automatically get noon product reviews on noon.com. Fetch the customer reviews of one noon (noon.com) product, 15 at a time, by its id (the product_id of Search noon products) or its noon.com product link, in the UAE, Saudi Arabia or Egypt store. Takes noon's sort orders (top, newest, highest rating, lowest rating) and a star filter. Returns the product's rating summary (average, rating count, review count, count per star), page, total_pages, has_next_page and reviews (id, rating, title, text, author, date, verified_purchase, helpful_count, language, variant, product_id, images). noon pools the reviews of all variants of a product, so variant and product_id say which one the reviewer bought. Reviews are returned in the language they were written in. When nothing matches the star filter, reviews is empty.

- Site: noon.com
- Address: `reduck/noon.com/get-product-reviews`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/noon.com/get-product-reviews`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/noon.com/get-product-reviews
```

## Input

- `product` (string, required): The noon product id (the product_id of Search noon products) or a noon.com product link.
- `page` (integer, optional): Review page, 15 reviews a page. has_next_page says when to stop.
- `sort` (string, optional): top (noon's default), newest, rating_desc (highest rating first), rating_asc (lowest rating first).
- `rating` (integer, optional): Only reviews with this many stars.
- `country` (string, optional): The noon store: uae, saudi or egypt.

## Output

- `page` (integer, required)
- `product` (object, required)
- `reviews` (array, required)
- `total_pages` (integer, required)
- `has_next_page` (boolean, required)

## FAQ

### What does "Get noon product reviews" do?

Fetch the customer reviews of one noon (noon.com) product, 15 at a time, by its id (the product_id of Search noon products) or its noon.com product link, in the UAE, Saudi Arabia or Egypt store. Takes noon's sort orders (top, newest, highest rating, lowest rating) and a star filter. Returns the product's rating summary (average, rating count, review count, count per star), page, total_pages, has_next_page and reviews (id, rating, title, text, author, date, verified_purchase, helpful_count, language, variant, product_id, images). noon pools the reviews of all variants of a product, so variant and product_id say which one the reviewer bought. Reviews are returned in the language they were written in. When nothing matches the star filter, reviews is empty.

### How do I automatically get noon product reviews on noon.com?

Ask an AI agent connected to Reduck to run reduck/noon.com/get-product-reviews, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/noon.com/get-product-reviews

### Is there a noon.com API to get noon product reviews?

You do not need one. "Get noon product reviews" drives the real noon.com pages in a browser, so it works whether or not noon.com offers an API for this.

### What information do I need to provide?

Required: product. Optional: page, sort, rating, country.

### What does it return?

It returns page, product, reviews, total_pages, has_next_page.

### Do I need to be logged in to noon.com?

No. It only uses pages of noon.com that are reachable without signing in.

### Does it change anything on noon.com, or only read data?

It only reads. It looks things up on noon.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/noon.com/get-product-reviews, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/noon.com/get-product-reviews

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/noon.com/get-product-reviews
