# Get Flipkart product reviews

Automatically get Flipkart product reviews on flipkart.com. Fetch the customer reviews of one Flipkart India (flipkart.com) product, 10 at a time, by its id (the product_id of Search Flipkart products) or its flipkart.com product link. Takes Flipkart's sort orders (most helpful, newest, positive first, negative first) and a verified purchases filter. Returns the product's rating summary (average, rating count, review count, count per star), page, has_next_page and reviews (id, rating, title, text, author, location, date, verified_purchase, helpful_count, unhelpful_count, variant, images). Flipkart pools the reviews of all variants of a product (colors, sizes), so variant says which one the reviewer bought. date is the text Flipkart shows, either relative ("29 days ago") or a month and year ("Sep, 2024").

- Site: flipkart.com
- Address: `reduck/flipkart.com/get-product-reviews`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/flipkart.com/get-product-reviews`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/flipkart.com/get-product-reviews
```

## Input

- `product` (string, required): The Flipkart product id (the product_id of Search Flipkart products) or a flipkart.com product link that has pid= in it.
- `page` (integer, optional): Review page, 10 reviews a page. has_next_page says when to stop.
- `sort` (string, optional): most_helpful (Flipkart's default), newest, positive_first, negative_first.
- `verified_only` (boolean, optional): Only reviews from verified purchases.

## Output

- `page` (integer, required)
- `product` (object, required)
- `reviews` (array, required)
- `has_next_page` (boolean, required)

## FAQ

### What does "Get Flipkart product reviews" do?

Fetch the customer reviews of one Flipkart India (flipkart.com) product, 10 at a time, by its id (the product_id of Search Flipkart products) or its flipkart.com product link. Takes Flipkart's sort orders (most helpful, newest, positive first, negative first) and a verified purchases filter. Returns the product's rating summary (average, rating count, review count, count per star), page, has_next_page and reviews (id, rating, title, text, author, location, date, verified_purchase, helpful_count, unhelpful_count, variant, images). Flipkart pools the reviews of all variants of a product (colors, sizes), so variant says which one the reviewer bought. date is the text Flipkart shows, either relative ("29 days ago") or a month and year ("Sep, 2024").

### How do I automatically get Flipkart product reviews on flipkart.com?

Ask an AI agent connected to Reduck to run reduck/flipkart.com/get-product-reviews, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/flipkart.com/get-product-reviews

### Is there a flipkart.com API to get Flipkart product reviews?

You do not need one. "Get Flipkart product reviews" drives the real flipkart.com pages in a browser, so it works whether or not flipkart.com offers an API for this.

### What information do I need to provide?

Required: product. Optional: page, sort, verified_only.

### What does it return?

It returns page, product, reviews, has_next_page.

### Do I need to be logged in to flipkart.com?

No. It only uses pages of flipkart.com that are reachable without signing in.

### Does it change anything on flipkart.com, or only read data?

It only reads. It looks things up on flipkart.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/flipkart.com/get-product-reviews, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/flipkart.com/get-product-reviews

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/flipkart.com/get-product-reviews
