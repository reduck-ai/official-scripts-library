# Get Cdiscount product reviews

Automatically get Cdiscount product reviews on cdiscount.com. Fetch the customer reviews of one Cdiscount.com product by its sku (from Search Cdiscount products), 10 at a time, with Cdiscount's own sort orders and a star filter. Returns the product's rating summary (average, review count, number of ratings per star, recommendations, average per criterion such as value for money) and each review's id, rating, title, text, date, reviewer name, helpful and unhelpful votes, source, criterion scores and images. source tells where the review comes from: Native (written on Cdiscount), Syndicated (copied from the brand's site, named in source_name) or Family (written for another variant, named in source_name). Pass page to read further; has_next_page is false on the last page. A product with no reviews gives an empty list. An unknown sku fails with an error that says so.

- Site: cdiscount.com
- Address: `reduck/cdiscount.com/get-product-reviews`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/cdiscount.com/get-product-reviews`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/cdiscount.com/get-product-reviews
```

## Input

- `sku` (string, required): Cdiscount product id, as Search Cdiscount products returns it, for example jbl1200130029967.
- `page` (integer, optional): Page of 10 reviews. total_pages and has_next_page say when to stop.
- `sort` (string, optional): helpful (most helpful first, the order of the product page), recent (newest first), oldest, rating_desc (best rating first), rating_asc (worst rating first).
- `stars` (integer, optional): Only reviews with this rating. Omit for all ratings.

## Output

- `sku` (string, required)
- `page` (integer, required)
- `sort` (string, required)
- `stars` (integer | null, required)
- `product` (object, required)
- `reviews` (array, required)
- `total_pages` (integer, required)
- `has_next_page` (boolean, required)
- `matching_reviews` (integer, required): Reviews that match the star filter, all reviews without it.

## FAQ

### What does "Get Cdiscount product reviews" do?

Fetch the customer reviews of one Cdiscount.com product by its sku (from Search Cdiscount products), 10 at a time, with Cdiscount's own sort orders and a star filter. Returns the product's rating summary (average, review count, number of ratings per star, recommendations, average per criterion such as value for money) and each review's id, rating, title, text, date, reviewer name, helpful and unhelpful votes, source, criterion scores and images. source tells where the review comes from: Native (written on Cdiscount), Syndicated (copied from the brand's site, named in source_name) or Family (written for another variant, named in source_name). Pass page to read further; has_next_page is false on the last page. A product with no reviews gives an empty list. An unknown sku fails with an error that says so.

### How do I automatically get Cdiscount product reviews on cdiscount.com?

Ask an AI agent connected to Reduck to run reduck/cdiscount.com/get-product-reviews, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/cdiscount.com/get-product-reviews

### Is there a cdiscount.com API to get Cdiscount product reviews?

You do not need one. "Get Cdiscount product reviews" drives the real cdiscount.com pages in a browser, so it works whether or not cdiscount.com offers an API for this.

### What information do I need to provide?

Required: sku. Optional: page, sort, stars.

### What does it return?

It returns sku, page, sort, stars, product, reviews, total_pages, has_next_page, matching_reviews.

### Do I need to be logged in to cdiscount.com?

No. It only uses pages of cdiscount.com that are reachable without signing in.

### Does it change anything on cdiscount.com, or only read data?

It only reads. It looks things up on cdiscount.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/cdiscount.com/get-product-reviews, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/cdiscount.com/get-product-reviews

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/cdiscount.com/get-product-reviews
