# Get Amazon product reviews

Automatically get Amazon product reviews on amazon.com. You get each review's text, stars, date and variation, about ten per call, with filters when signed in.

- Site: amazon.com
- Address: `reduck/amazon.com/get-product-reviews`
- Updated: 2026-10-05 (v9)
- Author: Reduck AI (reduck)

## About

Amazon's affiliate API will not give you what reviewers wrote. The Creators API, which is replacing the Product Advertising API, covers titles, images, offers and browse nodes, and no reviews. Give this an ASIN and you get the reviews, about 10 at a time, with the variation each buyer reviewed and a verified or Vine flag. Say you sell insulated bottles and a rival's 32 oz model has slid from 4.5 to 4.1 stars in a month. Run it with filterByStar=critical, filterByKeyword=leak and sortBy=recent, page through, and the complaints pile up on one lid variation: the point your own listing should answer first. The catch is the session. With one you read the full US reviews page, every filter, 10 pages deep. Without one you get only the product page's top reviews, a few from other countries mixed in, no filters, and in tests on 2 October about half of fresh cloud browsers got a sign-in prompt instead.

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/amazon.com/get-product-reviews`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/amazon.com/get-product-reviews
```

## Input

- `asin` (string, required): 10-char Amazon ASIN.
- `page` (integer, optional): Review page to fetch (10 reviews/page; Amazon hard-caps reviews pagination at 10). One page per call; the caller loops for more. Ordering is server-controlled; with sortBy=recent the set can shift between calls as new reviews arrive, so page N is not guaranteed stable under replay (sortBy=helpful is far more stable). Pagination needs a session: an anonymous run can only read the top reviews shown on the product page, which is page 1 only, and page>1 throws there.
- `sortBy` (string, optional): recent = Most recent; helpful = Top reviews. Honoured only when the run has a session; an anonymous run returns the product page's top reviews in Amazon's own order regardless (check `source` in the result).
- `zipCode` (string, optional): US ZIP used to pin the store to the US.
- `mediaType` (string, optional): media_reviews_only restricts to reviews with an image or video. Needs a session, and throws on an anonymous run.
- `filterByStar` (string, optional): Star filter. positive/critical group multiple ratings. Needs a session, and throws on an anonymous run.
- `reviewerType` (string, optional): verified_reviews restricts to verified purchases. Needs a session, and throws on an anonymous run.
- `filterByKeyword` (string, optional): Only reviews containing this keyword. This filter returns only ratings that include a written review. Needs a session, and throws on an anonymous run.

## Output

- `page` (integer, required): Review page this result covers. Always 1 when source=product_page_medley.
- `source` (string, required): Which Amazon surface produced this result. reviews_page = the full /product-reviews/ list (needs a session; supports sort, filters and pagination; US store only). product_page_medley = the top-reviews block on the product page, all an anonymous browser can read: page 1 only, no filters, Amazon's own ordering, and it mixes in reviews from other Amazon stores (read `country` per review) where reviews_page returns US only. Sort/filter/pagination arguments throw on this surface rather than being silently dropped. Amazon sometimes serves an anonymous browser the product page without its reviews (rating and star histogram shown, a sign-in prompt in place of the review list); the run then fails with an error saying so instead of returning an empty list, so reviews: [] on this surface means the product really has no written reviews.
- `product` (object, required)
- `reviews` (array, required)
- `authenticated` (boolean, required): Whether the run had a usable Amazon session. False means the result came from the anonymous medley and is thinner BY DESIGN, not by failure: page 1 of top reviews only.

## Example output

Shape only: placeholder values generated from the output schema, not a real run.

```json
{
  "page": 1,
  "source": "reviews_page",
  "product": {
    "asin": "…",
    "title": "Example",
    "reviewCount": 3,
    "totalRatings": 3,
    "overallRating": 3.5,
    "starBreakdown": {
      "one_star": 3,
      "two_star": 3,
      "five_star": 3,
      "four_star": 3,
      "three_star": 3
    }
  },
  "reviews": [
    {
      "id": "abc123",
      "date": "2026-01-15T09:30:00Z",
      "text": "…",
      "vine": true,
      "title": "Example",
      "images": [
        "…"
      ],
      "rating": 3.5,
      "videos": [
        "…"
      ],
      "country": 3,
      "dateText": "…",
      "reviewer": "…",
      "variation": "…",
      "helpfulVotes": 3,
      "verifiedPurchase": true
    }
  ],
  "authenticated": true
}
```

## FAQ

### What does "Get Amazon product reviews" do?

Fetch Amazon customer reviews for a product by ASIN. With a signed-in Amazon session it returns one page of 10 reviews, with sort, star, media, verified-purchase and keyword filters, up to Amazon's 10-page limit. Without a session it returns the top reviews shown on the product page (page 1 only, no filters, reviews from other Amazon countries included), says so in the result, and fails with a clear error instead of ignoring a filter or page it cannot serve, or when Amazon hides the reviews from the visitor. Returns the product's rating summary and each review's rating, title, text, date, reviewer, country, variation, helpful votes, verified badge, Vine badge, images and videos. With sortBy=recent a page can change between calls as new reviews arrive; sortBy=helpful is more stable.

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

### How many Amazon reviews can I pull for one product?

Signed in to Amazon, you get 10 reviews per call and Amazon stops at page 10, so one sort and filter combination tops out around 100 reviews. Each star filter from five_star to one_star has its own 10 pages and they never overlap, which means running all five gets you up to about 500 on a heavily reviewed product. Signed out, you get only the top reviews block on the product page, one page and no filters.

### Does it work for amazon.co.uk, amazon.de or other Amazon stores?

No, only amazon.com: the run pins the US store with a ZIP code, and an ASIN with no US product page fails with a clear error instead of returning an empty list. A signed-out run does show a few reviews written on other Amazon stores, because Amazon mixes them into the product page's top reviews, and the country field usually names the store each came from. Country and date are parsed from Amazon's English "Reviewed in" line, so on an account whose amazon.com language is set to Spanish they can come back null, with only dateText filled.

### Why does Amazon show the star rating but no reviews when I'm not signed in?

Amazon hides review text from some signed-out visitors, keeping the rating, star histogram and AI summary on the product page but putting a sign-in prompt where the review list belongs. In tests on 2 October about half of fresh cloud browsers got that version, and the run fails with an error naming it rather than handing back an empty list. A retry can land the normal page, and a Chrome signed in to Amazon reads the full reviews page instead.

### How do I track new reviews on a product over time?

Schedule page 1 with sortBy=recent from a browser signed in to Amazon and store every review id you see, since an id stays the same from run to run. If more than 10 reviews can land between two runs, keep requesting the next page until one contains an id you already have. Check authenticated in each result: a signed-out run ignores sortBy without any error and returns Amazon's top reviews instead, so new ones can slip past unnoticed.

Source: https://reduck.ai/explore/scripts/reduck/amazon.com/get-product-reviews
