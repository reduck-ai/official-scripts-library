# Get Amazon.com.tr product reviews

Automatically get Amazon.com.tr product reviews on amazon.com.tr. Fetch Amazon.com.tr customer reviews for a product by ASIN. With a signed-in Amazon session it returns 10 reviews at a time, with sort, star, media, verified-purchase and keyword filters, plus a cursor for the next 10. Without a session it returns the top reviews shown on the product page (one page only, no filters, reviews from other Amazon countries included), says so in the result, and fails with a clear error instead of ignoring a filter or cursor it cannot serve. Returns the product's rating summary and each review's rating, title, text, date line as shown, reviewer, country, variation, helpful votes, verified badge, Vine badge, images and videos.

- Site: amazon.com.tr
- Address: `reduck/amazon.com.tr/get-product-reviews`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/amazon.com.tr/get-product-reviews`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/amazon.com.tr/get-product-reviews
```

## Input

- `asin` (string, required): 10-character Amazon ASIN.
- `cursor` (string, optional): nextCursor from a previous call with the same ASIN, sortBy and filters. Needs a session.
- `sortBy` (string, optional): recent = most recent; helpful = top reviews. Honoured only with a session.
- `zipCode` (string, optional): Turkish postcode used to pin the store.
- `mediaType` (string, optional): Needs a session.
- `filterByStar` (string, optional): Needs a session.
- `reviewerType` (string, optional): Needs a session.
- `filterByKeyword` (string, optional): Needs a session.

## Output

- `source` (string, required)
- `product` (object, required)
- `reviews` (array, required)
- `nextCursor` (string | null, required)
- `authenticated` (boolean, required)
- `reviewAccess` (string | null, optional)

## FAQ

### What does "Get Amazon.com.tr product reviews" do?

Fetch Amazon.com.tr customer reviews for a product by ASIN. With a signed-in Amazon session it returns 10 reviews at a time, with sort, star, media, verified-purchase and keyword filters, plus a cursor for the next 10. Without a session it returns the top reviews shown on the product page (one page only, no filters, reviews from other Amazon countries included), says so in the result, and fails with a clear error instead of ignoring a filter or cursor it cannot serve. Returns the product's rating summary and each review's rating, title, text, date line as shown, reviewer, country, variation, helpful votes, verified badge, Vine badge, images and videos.

### How do I automatically get Amazon.com.tr product reviews on amazon.com.tr?

Ask an AI agent connected to Reduck to run reduck/amazon.com.tr/get-product-reviews, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.com.tr/get-product-reviews

### Is there a amazon.com.tr API to get Amazon.com.tr product reviews?

You do not need one. "Get Amazon.com.tr product reviews" drives the real amazon.com.tr pages in a browser, so it works whether or not amazon.com.tr offers an API for this.

### What information do I need to provide?

Required: asin. Optional: cursor, sortBy, zipCode, mediaType, filterByStar, reviewerType, filterByKeyword.

### What does it return?

It returns source, product, reviews, nextCursor, reviewAccess, authenticated.

### Do I need to be logged in to amazon.com.tr?

No. It only uses pages of amazon.com.tr that are reachable without signing in.

### Does it change anything on amazon.com.tr, or only read data?

It only reads. It looks things up on amazon.com.tr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/amazon.com.tr/get-product-reviews, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.com.tr/get-product-reviews

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/amazon.com.tr/get-product-reviews
