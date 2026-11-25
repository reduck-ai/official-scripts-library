# Get Coolblue product reviews

Automatically get Coolblue product reviews on coolblue.nl. Get the customer reviews of a product of Coolblue Netherlands (coolblue.nl) by its product number or product link, 10 reviews a page, sorted by helpfulness or by score, with a star filter and the site's review language filter. Each review gives its score out of 10 as Coolblue gives it, title, text, pros, cons, author, date, images, helpful and not helpful votes, whether it is Coolblue's own expert review, and the variant it was written for. The result also gives the product's review score out of 10, the review counts (all languages, and in the chosen language), the count for each number of stars and the score for each aspect. Pass page to read the next reviews until has_next_page is false. A product with no review returns an empty list; an unknown product number fails with an error that says so.

- Site: coolblue.nl
- Address: `reduck/coolblue.nl/get-product-reviews`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/coolblue.nl/get-product-reviews`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/coolblue.nl/get-product-reviews
```

## Input

- `product` (string, required): Coolblue product number (the product_id of Search Coolblue products) or a product link.
- `page` (integer, optional): Review page, 10 reviews a page. has_next_page says when to stop.
- `sort` (string, optional): Sort order: helpful (most helpful first, the default), rating_desc (highest score first), rating_asc (lowest score first).
- `stars` (integer, optional): Only the reviews with this number of stars (1 to 5).
- `language` (string, optional): Only the reviews written in this language: nl (Dutch, the default) or en (English).
- `include_translations` (boolean, optional): Also include the reviews written in another language, translated by the site.

## Output

- `page` (integer, required)
- `reviews` (array, required)
- `product_id` (string, required)
- `has_next_page` (boolean, required)
- `url` (string | null, optional)
- `rating` (number | null, optional): The product's average review score out of 10, as Coolblue gives it.
- `review_count` (integer | null, optional): Reviews in all languages.
- `aspect_ratings` (array, optional): Average score out of 10 for each aspect the reviewers rate, in Dutch.
- `rating_distribution` (array, optional): Number of reviews for each number of stars (1 to 5), all languages.
- `review_count_in_language` (integer | null, optional): Reviews written in the chosen language.

## FAQ

### What does "Get Coolblue product reviews" do?

Get the customer reviews of a product of Coolblue Netherlands (coolblue.nl) by its product number or product link, 10 reviews a page, sorted by helpfulness or by score, with a star filter and the site's review language filter. Each review gives its score out of 10 as Coolblue gives it, title, text, pros, cons, author, date, images, helpful and not helpful votes, whether it is Coolblue's own expert review, and the variant it was written for. The result also gives the product's review score out of 10, the review counts (all languages, and in the chosen language), the count for each number of stars and the score for each aspect. Pass page to read the next reviews until has_next_page is false. A product with no review returns an empty list; an unknown product number fails with an error that says so.

### How do I automatically get Coolblue product reviews on coolblue.nl?

Ask an AI agent connected to Reduck to run reduck/coolblue.nl/get-product-reviews, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/coolblue.nl/get-product-reviews

### Is there a coolblue.nl API to get Coolblue product reviews?

You do not need one. "Get Coolblue product reviews" drives the real coolblue.nl pages in a browser, so it works whether or not coolblue.nl offers an API for this.

### What information do I need to provide?

Required: product. Optional: page, sort, stars, language, include_translations.

### What does it return?

It returns url, page, rating, reviews, product_id, review_count, has_next_page, aspect_ratings, rating_distribution, review_count_in_language.

### Do I need to be logged in to coolblue.nl?

No. It only uses pages of coolblue.nl that are reachable without signing in.

### Does it change anything on coolblue.nl, or only read data?

It only reads. It looks things up on coolblue.nl and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/coolblue.nl/get-product-reviews, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/coolblue.nl/get-product-reviews

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/coolblue.nl/get-product-reviews
