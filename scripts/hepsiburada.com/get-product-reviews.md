# Get Hepsiburada product reviews

Automatically get Hepsiburada product reviews on hepsiburada.com. Fetch the customer reviews of one Hepsiburada (hepsiburada.com) product, 10 at a time, by its id (the product_id of Search Hepsiburada products) or its hepsiburada.com product link. Takes Hepsiburada's sort orders and a star filter. Returns the product's rating summary (average, rating count, count per star), page, total_pages, has_next_page and reviews (id, rating, text, author, date, verified_purchase, likes, dislikes, seller, product_id, images). Hepsiburada pools the reviews of all variants of a product, so product_id says which variant the reviewer bought. Review text is in Turkish, as written; author names are masked by Hepsiburada. When nothing matches the star filter, reviews is empty.

- Site: hepsiburada.com
- Address: `reduck/hepsiburada.com/get-product-reviews`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/hepsiburada.com/get-product-reviews`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/hepsiburada.com/get-product-reviews
```

## Input

- `product` (string, required): The Hepsiburada product id (the product_id of Search Hepsiburada products) or a hepsiburada.com product link.
- `page` (integer, optional): Review page, 10 reviews a page. has_next_page says when to stop.
- `sort` (string, optional): recommended (Hepsiburada's default), newest, most_helpful, rating_desc (highest rating first), rating_asc (lowest rating first).
- `rating` (integer, optional): Only reviews with this many stars.

## Output

- `page` (integer, required)
- `product` (object, required)
- `reviews` (array, required)
- `total_pages` (integer, required)
- `has_next_page` (boolean, required)
- `matching_reviews` (integer | null, optional): Number of reviews that match the star filter, or all of them without one.

## FAQ

### What does "Get Hepsiburada product reviews" do?

Fetch the customer reviews of one Hepsiburada (hepsiburada.com) product, 10 at a time, by its id (the product_id of Search Hepsiburada products) or its hepsiburada.com product link. Takes Hepsiburada's sort orders and a star filter. Returns the product's rating summary (average, rating count, count per star), page, total_pages, has_next_page and reviews (id, rating, text, author, date, verified_purchase, likes, dislikes, seller, product_id, images). Hepsiburada pools the reviews of all variants of a product, so product_id says which variant the reviewer bought. Review text is in Turkish, as written; author names are masked by Hepsiburada. When nothing matches the star filter, reviews is empty.

### How do I automatically get Hepsiburada product reviews on hepsiburada.com?

Ask an AI agent connected to Reduck to run reduck/hepsiburada.com/get-product-reviews, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/hepsiburada.com/get-product-reviews

### Is there a hepsiburada.com API to get Hepsiburada product reviews?

You do not need one. "Get Hepsiburada product reviews" drives the real hepsiburada.com pages in a browser, so it works whether or not hepsiburada.com offers an API for this.

### What information do I need to provide?

Required: product. Optional: page, sort, rating.

### What does it return?

It returns page, product, reviews, total_pages, has_next_page, matching_reviews.

### Do I need to be logged in to hepsiburada.com?

No. It only uses pages of hepsiburada.com that are reachable without signing in.

### Does it change anything on hepsiburada.com, or only read data?

It only reads. It looks things up on hepsiburada.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/hepsiburada.com/get-product-reviews, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/hepsiburada.com/get-product-reviews

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/hepsiburada.com/get-product-reviews
