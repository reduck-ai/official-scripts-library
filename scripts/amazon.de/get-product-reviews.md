# Get Amazon.de product reviews

Automatically get Amazon.de product reviews on amazon.de. Fetch Amazon.de customer reviews for a product by ASIN. With a signed-in Amazon session it returns 10 reviews at a time, with sort, star, media, verified-purchase and keyword filters, plus a cursor for the next 10; pass it back with the same filters to continue, until no cursor comes back (Amazon stops after about 10 pages). Without a session it returns the top reviews shown on the product page (one page only, no filters, reviews from other Amazon countries included), says so in the result, and fails with a clear error instead of ignoring a filter or cursor it cannot serve, or when Amazon hides the reviews from the visitor. Returns the product's rating summary and each review's rating, title, text, date, reviewer, country, variation, helpful votes, verified badge, Vine badge, images and videos. With sortBy=recent the pages can shift between calls as new reviews arrive; sortBy=helpful is more stable.

- Site: amazon.de
- Address: `reduck/amazon.de/get-product-reviews`
- Updated: 2026-11-23 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/amazon.de/get-product-reviews`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/amazon.de/get-product-reviews
```

## Input

- `asin` (string, required): 10-char Amazon ASIN.
- `cursor` (string, optional): nextCursor from a previous call with the same ASIN, sort and filters; returns the next 10 reviews. Omit for the first page. Amazon stops offering a next page after about 10 pages. Paging needs a session: an anonymous run can only read the top reviews on the product page, and a cursor throws there.
- `sortBy` (string, optional): recent = Most recent; helpful = Top reviews. Honoured only when the run has a session; an anonymous run returns the product page's top reviews in Amazon's own order regardless (check `source` in the result).
- `zipCode` (string, optional): German postcode used to pin the store to Germany.
- `mediaType` (string, optional): media_reviews_only restricts to reviews with an image or video. Needs a session, and throws on an anonymous run.
- `filterByStar` (string, optional): Star filter. positive/critical group multiple ratings. Needs a session, and throws on an anonymous run.
- `reviewerType` (string, optional): verified_reviews restricts to verified purchases. Needs a session, and throws on an anonymous run.
- `filterByKeyword` (string, optional): Only reviews containing this keyword. This filter returns only ratings that include a written review. Needs a session, and throws on an anonymous run.

## Output

- `source` (string, required): Which Amazon surface produced this result. reviews_page = the full reviews list (needs a session; supports sort, filters and paging). product_page_medley = the top-reviews block on the product page, all an anonymous browser can read: one page only, no filters, Amazon's own ordering, and it mixes in reviews from other Amazon stores (read `country` per review) where reviews_page returns Germany only. Sort, filter and cursor arguments throw on this surface rather than being silently dropped. Amazon sometimes serves an anonymous browser the product page without its reviews (rating and star histogram shown, a sign-in prompt in place of the review list); the run then fails with an error saying so instead of returning an empty list, so reviews: [] on this surface means the product really has no written reviews.
- `product` (object, required)
- `reviews` (array, required)
- `nextCursor` (string | null, required): Pass as cursor to get the next 10 reviews. Null when Amazon offers no next page, and always null when source=product_page_medley.
- `authenticated` (boolean, required): Whether the run had a usable Amazon session. False means the result came from the anonymous medley and is thinner by design, not by failure: the top reviews only.
- `reviewAccess` (string | null, optional): Review access as the reviews page shows it. full: the whole list, with sort, filters and paging. limited: Amazon limits this account after unusual activity, so the page shows only its top reviews, with no filters and no paging; the reviews page offers a request to restore access. limited_request_sent: limited, and a request is pending until Amazon answers by email. Null on the signed-out product page.

## FAQ

### What does "Get Amazon.de product reviews" do?

Fetch Amazon.de customer reviews for a product by ASIN. With a signed-in Amazon session it returns 10 reviews at a time, with sort, star, media, verified-purchase and keyword filters, plus a cursor for the next 10; pass it back with the same filters to continue, until no cursor comes back (Amazon stops after about 10 pages). Without a session it returns the top reviews shown on the product page (one page only, no filters, reviews from other Amazon countries included), says so in the result, and fails with a clear error instead of ignoring a filter or cursor it cannot serve, or when Amazon hides the reviews from the visitor. Returns the product's rating summary and each review's rating, title, text, date, reviewer, country, variation, helpful votes, verified badge, Vine badge, images and videos. With sortBy=recent the pages can shift between calls as new reviews arrive; sortBy=helpful is more stable.

### How do I automatically get Amazon.de product reviews on amazon.de?

Ask an AI agent connected to Reduck to run reduck/amazon.de/get-product-reviews, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.de/get-product-reviews

### Is there a amazon.de API to get Amazon.de product reviews?

You do not need one. "Get Amazon.de product reviews" drives the real amazon.de pages in a browser, so it works whether or not amazon.de offers an API for this.

### What information do I need to provide?

Required: asin. Optional: cursor, sortBy, zipCode, mediaType, filterByStar, reviewerType, filterByKeyword.

### What does it return?

It returns source, product, reviews, nextCursor, reviewAccess, authenticated.

### Do I need to be logged in to amazon.de?

No. It only uses pages of amazon.de that are reachable without signing in.

### Does it change anything on amazon.de, or only read data?

It only reads. It looks things up on amazon.de and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/amazon.de/get-product-reviews, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.de/get-product-reviews

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/amazon.de/get-product-reviews
