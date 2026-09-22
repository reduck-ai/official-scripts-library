# Get Google Maps place reviews

Automatically get Google Maps place reviews on google.com. Get a Google Maps place's reviews by placeId. Returns n and reviews with author, authorMeta byline, rating, time, text, and reviewId. Returned in Google's default "most relevant" order, not by date; fewer than requested come back for places with few reviews.

- Site: google.com
- Address: `reduck/google.com/get_place_reviews`
- Updated: 2026-09-17 (v9)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/google.com/get_place_reviews`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/google.com/get_place_reviews
```

## Input

- `count` (number, optional): Max reviews to return. Scrolls the feed until this many load or the feed is exhausted (fewer for places with few reviews).
- `placeId` (string, optional): Canonical ChIJ… place ID. Reached via Google's ?q=place_id: redirect. Prefer placeUrl when you have get_place's resolvedUrl — the free-text path of get_place yields no ChIJ. An id Google cannot resolve is reported as an unresolved place rather than timing out.
- `placeUrl` (string, optional): A canonical Google Maps place URL containing '/data=…!16s…' — for example get_place's resolvedUrl. Navigated directly with no redirect, and the most reliable join key from get_place. Wins over placeId when both are given.

## Output

- `n` (number, optional): Number of reviews returned. 0 when the place has no reviews at all.
- `reviews` (array, optional)

## FAQ

### What does "Get Google Maps place reviews" do?

Get a Google Maps place's reviews by placeId. Returns n and reviews with author, authorMeta byline, rating, time, text, and reviewId. Returned in Google's default "most relevant" order, not by date; fewer than requested come back for places with few reviews.

### How do I automatically get Google Maps place reviews on google.com?

Ask an AI agent connected to Reduck to run reduck/google.com/get_place_reviews, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/google.com/get_place_reviews

### Is there a google.com API to get Google Maps place reviews?

You do not need one. "Get Google Maps place reviews" drives the real google.com pages in a browser, so it works whether or not google.com offers an API for this.

### What information do I need to provide?

Optional: count, placeId, placeUrl.

### What does it return?

It returns n, reviews.

### Do I need to be logged in to google.com?

No. It only uses pages of google.com that are reachable without signing in.

### Does it change anything on google.com, or only read data?

It only reads. It looks things up on google.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/google.com/get_place_reviews, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/google.com/get_place_reviews

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/google.com/get_place_reviews
