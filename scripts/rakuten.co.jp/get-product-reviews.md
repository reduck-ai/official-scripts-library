# Get Rakuten product reviews

Automatically get Rakuten product reviews on rakuten.co.jp. Fetch the customer reviews of one Rakuten Ichiba (rakuten.co.jp) product, 30 at a time, by its id (shop-code/item-code, as Search Rakuten products returns it) or its item.rakuten.co.jp link. Takes Rakuten's own sort order and filters: star rating, reviews with images or video only, reviewer age range and gender. Returns the product's rating summary (average, count, count per star), page, total_pages, has_next_page and reviews (id, rating, title, text, author, date, order_date, variation, helpful_count, age_range, gender, images). Review text is in Japanese, as written. When nothing matches the filters, reviews is empty. Shop reviews are not included.

- Site: rakuten.co.jp
- Address: `reduck/rakuten.co.jp/get-product-reviews`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/rakuten.co.jp/get-product-reviews`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/rakuten.co.jp/get-product-reviews
```

## Input

- `product` (string, required): The product id as shop-code/item-code (the product_id of Search Rakuten products), or an item.rakuten.co.jp product link.
- `page` (integer, optional): Review page, 30 reviews a page. has_next_page says when to stop.
- `sort` (string, optional): standard (Rakuten's default order), most_helpful, highest_rating, newest.
- `gender` (string, optional): Only reviews from reviewers of this gender.
- `rating` (integer, optional): Only reviews with this many stars.
- `age_range` (string, optional): Only reviews from reviewers in this age range.
- `with_media_only` (boolean, optional): Only reviews that include an image or a video.

## Output

- `page` (integer, required)
- `product` (object, required)
- `reviews` (array, required)
- `total_pages` (integer, required)
- `has_next_page` (boolean, required)
- `matching_reviews` (integer | null, optional): Number of reviews that match the filters.

## FAQ

### What does "Get Rakuten product reviews" do?

Fetch the customer reviews of one Rakuten Ichiba (rakuten.co.jp) product, 30 at a time, by its id (shop-code/item-code, as Search Rakuten products returns it) or its item.rakuten.co.jp link. Takes Rakuten's own sort order and filters: star rating, reviews with images or video only, reviewer age range and gender. Returns the product's rating summary (average, count, count per star), page, total_pages, has_next_page and reviews (id, rating, title, text, author, date, order_date, variation, helpful_count, age_range, gender, images). Review text is in Japanese, as written. When nothing matches the filters, reviews is empty. Shop reviews are not included.

### How do I automatically get Rakuten product reviews on rakuten.co.jp?

Ask an AI agent connected to Reduck to run reduck/rakuten.co.jp/get-product-reviews, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/rakuten.co.jp/get-product-reviews

### Is there a rakuten.co.jp API to get Rakuten product reviews?

You do not need one. "Get Rakuten product reviews" drives the real rakuten.co.jp pages in a browser, so it works whether or not rakuten.co.jp offers an API for this.

### What information do I need to provide?

Required: product. Optional: page, sort, gender, rating, age_range, with_media_only.

### What does it return?

It returns page, product, reviews, total_pages, has_next_page, matching_reviews.

### Do I need to be logged in to rakuten.co.jp?

No. It only uses pages of rakuten.co.jp that are reachable without signing in.

### Does it change anything on rakuten.co.jp, or only read data?

It only reads. It looks things up on rakuten.co.jp and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/rakuten.co.jp/get-product-reviews, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/rakuten.co.jp/get-product-reviews

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/rakuten.co.jp/get-product-reviews
