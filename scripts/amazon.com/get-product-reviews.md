# Get Amazon product reviews

Automatically get Amazon product reviews on amazon.com. Fetch Amazon customer reviews for an ASIN. Works signed in or anonymously, and says which surface it used. With a session it reads the full /product-reviews/ list: one page of 10, with sort, star, media, reviewer and keyword filters, up to Amazon's 10-page cap. Without one it reads the product page's reviews medley instead (page 1 of top reviews, no filters, other-country reviews included), returns authenticated:false and source:product_page_medley, and throws rather than quietly ignoring a filter or page it cannot serve. Returns product (asin, title, overallRating, totalRatings, reviewCount, starBreakdown) and reviews (id, rating, title, text, date, reviewer, country, variation, helpfulVotes, verifiedPurchase, vine, images, videos). With sortBy=recent a given page is not stable across calls as new reviews arrive, so prefer sortBy=helpful for replay.

- Site: amazon.com
- Address: `reduck/amazon.com/get-product-reviews`
- Updated: 2026-09-09 (v8)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/amazon.com/get-product-reviews`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/amazon.com/get-product-reviews
```

## Input

- `asin` (string, required): 10-char Amazon ASIN.
- `page` (integer, optional): Review page to fetch (10 reviews/page; Amazon hard-caps reviews pagination at 10). One page per call — the caller loops for more. Ordering is server-controlled; with sortBy=recent the set can shift between calls as new reviews arrive, so page N is not guaranteed stable under replay (sortBy=helpful is far more stable). Pagination needs a session: an anonymous run can only read the product-page medley, which is page 1 only, and page>1 throws there.
- `sortBy` (string, optional): recent = Most recent; helpful = Top reviews. Honoured only when the run has a session; the anonymous medley serves Amazon's own top-reviews ordering regardless (check `source` in the result).
- `zipCode` (string, optional): US ZIP used to pin the store to the US.
- `mediaType` (string, optional): media_reviews_only restricts to reviews with an image or video. Needs a session, and throws on an anonymous run.
- `filterByStar` (string, optional): Star filter. positive/critical group multiple ratings. Needs a session, and throws on an anonymous run.
- `reviewerType` (string, optional): verified_reviews restricts to verified purchases (maps to Amazon's avp_only_reviews). Needs a session, and throws on an anonymous run.
- `filterByKeyword` (string, optional): Only reviews containing this keyword. This filter returns only ratings that include a written review. Needs a session, and throws on an anonymous run.

## Output

- `page` (integer, required): Review page this result covers. Always 1 when source=product_page_medley.
- `source` (string, required): Which Amazon surface produced this result. reviews_page = the full /product-reviews/ list (needs a session; supports sort, filters and pagination; US store only). product_page_medley = the top-reviews block on the product page, all an anonymous browser can read: page 1 only, no filters, Amazon's own ordering, and it mixes in reviews from other Amazon stores (read `country` per review) where reviews_page returns US only. Sort/filter/pagination arguments throw on this surface rather than being silently dropped.
- `product` (object, required)
- `reviews` (array, required)
- `authenticated` (boolean, required): Whether the run had a usable Amazon session. False means the result came from the anonymous medley and is thinner BY DESIGN, not by failure: page 1 of top reviews only.

## FAQ

### What does "Get Amazon product reviews" do?

Fetch Amazon customer reviews for an ASIN. Works signed in or anonymously, and says which surface it used. With a session it reads the full /product-reviews/ list: one page of 10, with sort, star, media, reviewer and keyword filters, up to Amazon's 10-page cap. Without one it reads the product page's reviews medley instead (page 1 of top reviews, no filters, other-country reviews included), returns authenticated:false and source:product_page_medley, and throws rather than quietly ignoring a filter or page it cannot serve. Returns product (asin, title, overallRating, totalRatings, reviewCount, starBreakdown) and reviews (id, rating, title, text, date, reviewer, country, variation, helpfulVotes, verifiedPurchase, vine, images, videos). With sortBy=recent a given page is not stable across calls as new reviews arrive, so prefer sortBy=helpful for replay.

### How do I automatically get Amazon product reviews on amazon.com?

Ask an AI agent connected to Reduck to run reduck/amazon.com/get-product-reviews, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.com/get-product-reviews

### Is there a amazon.com API to get Amazon product reviews?

You do not need one. "Get Amazon product reviews" drives the real amazon.com pages in a browser, so it works whether or not amazon.com offers an API for this.

### What information do I need to provide?

Required: asin. Optional: page, sortBy, zipCode, mediaType, filterByStar, reviewerType, filterByKeyword.

### What does it return?

It returns page, source, product, reviews, authenticated.

### Do I need to be logged in to amazon.com?

No. It only uses pages of amazon.com that are reachable without signing in.

### Does it change anything on amazon.com, or only read data?

It only reads. It looks things up on amazon.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/amazon.com/get-product-reviews, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.com/get-product-reviews

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/amazon.com/get-product-reviews
