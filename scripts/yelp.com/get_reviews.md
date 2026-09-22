# Get Yelp business reviews

Automatically get Yelp business reviews on yelp.com. List a Yelp business's reviews by slug, paginated. Returns author, rating, date, review text, and reaction counts (helpful/thanks/love this/oh no) per review.

- Site: yelp.com
- Address: `reduck/yelp.com/get_reviews`
- Updated: 2026-08-27 (v8)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/yelp.com/get_reviews`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/yelp.com/get_reviews
```

## Input

- `slug` (string, required): Yelp business slug, e.g. 'l-industrie-pizzeria-new-york'
- `start` (integer, optional): Pagination offset (Yelp shows ~10 reviews per page): 0, 10, 20, ...

## Output

- `slug` (string, optional)
- `count` (integer, optional)
- `start` (integer, optional)
- `reviews` (array, optional)

## FAQ

### What does "Get Yelp business reviews" do?

List a Yelp business's reviews by slug, paginated. Returns author, rating, date, review text, and reaction counts (helpful/thanks/love this/oh no) per review.

### How do I automatically get Yelp business reviews on yelp.com?

Ask an AI agent connected to Reduck to run reduck/yelp.com/get_reviews, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/yelp.com/get_reviews

### Is there a yelp.com API to get Yelp business reviews?

You do not need one. "Get Yelp business reviews" drives the real yelp.com pages in a browser, so it works whether or not yelp.com offers an API for this.

### What information do I need to provide?

Required: slug. Optional: start.

### What does it return?

It returns slug, count, start, reviews.

### Do I need to be logged in to yelp.com?

No. It only uses pages of yelp.com that are reachable without signing in.

### Does it change anything on yelp.com, or only read data?

It only reads. It looks things up on yelp.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/yelp.com/get_reviews, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/yelp.com/get_reviews

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/yelp.com/get_reviews
