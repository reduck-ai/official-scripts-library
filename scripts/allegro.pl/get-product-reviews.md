# Get Allegro product reviews

Automatically get Allegro product reviews on allegro.pl. Fetch the product reviews of an Allegro (allegro.pl) offer, 20 at a time, by its offer number (the product_id of Search Allegro products) or its allegro.pl link. Allegro collects reviews per catalog product, so the reviews cover every offer of the same product. Takes Allegro's sort order (most helpful or newest) and a star filter. Returns the product's rating summary (average, rating count, review count, count per star), page, total_pages, has_next_page and reviews (id, rating, text, pros, cons, author, date, seller, helpful votes, images, translated). Review text is in the language the reviewer used, mostly Polish; author names are masked by Allegro. An offer that is not linked to a catalog product has no product reviews: then reviews is empty and reason says why.

- Site: allegro.pl
- Address: `reduck/allegro.pl/get-product-reviews`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/allegro.pl/get-product-reviews`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/allegro.pl/get-product-reviews
```

## Input

- `product` (string, required): The Allegro offer number (the product_id of Search Allegro products), or an allegro.pl offer link, or a product link that carries offerId.
- `page` (integer, optional): Review page, 20 reviews a page. has_next_page says when to stop.
- `sort` (string, optional): most_helpful (Allegro's default) or newest.
- `rating` (integer, optional): Only reviews with this many stars.

## Output

- `page` (integer, required)
- `reason` (string | null, required): Why there are no reviews to list, when the offer has no catalog product. Null otherwise.
- `product` (object, required)
- `reviews` (array, required)
- `total_pages` (integer, required)
- `has_next_page` (boolean, required)
- `matching_reviews` (integer | null, optional): Number of written reviews that match the star filter.

## FAQ

### What does "Get Allegro product reviews" do?

Fetch the product reviews of an Allegro (allegro.pl) offer, 20 at a time, by its offer number (the product_id of Search Allegro products) or its allegro.pl link. Allegro collects reviews per catalog product, so the reviews cover every offer of the same product. Takes Allegro's sort order (most helpful or newest) and a star filter. Returns the product's rating summary (average, rating count, review count, count per star), page, total_pages, has_next_page and reviews (id, rating, text, pros, cons, author, date, seller, helpful votes, images, translated). Review text is in the language the reviewer used, mostly Polish; author names are masked by Allegro. An offer that is not linked to a catalog product has no product reviews: then reviews is empty and reason says why.

### How do I automatically get Allegro product reviews on allegro.pl?

Ask an AI agent connected to Reduck to run reduck/allegro.pl/get-product-reviews, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/allegro.pl/get-product-reviews

### Is there a allegro.pl API to get Allegro product reviews?

You do not need one. "Get Allegro product reviews" drives the real allegro.pl pages in a browser, so it works whether or not allegro.pl offers an API for this.

### What information do I need to provide?

Required: product. Optional: page, sort, rating.

### What does it return?

It returns page, reason, product, reviews, total_pages, has_next_page, matching_reviews.

### Do I need to be logged in to allegro.pl?

No. It only uses pages of allegro.pl that are reachable without signing in.

### Does it change anything on allegro.pl, or only read data?

It only reads. It looks things up on allegro.pl and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/allegro.pl/get-product-reviews, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/allegro.pl/get-product-reviews

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/allegro.pl/get-product-reviews
