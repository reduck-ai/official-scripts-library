# Get Google Maps place reviews

Automatically get Google Maps place reviews on google.com. Get the reviews of a Google Maps place, given its place id or its Maps link. Returns how many reviews came back and, for each, the author, their reviewer byline and photo count, the star rating, when it was posted, the full text, the owner's reply, and a stable review id. Reviews come in Google's "most relevant" order, not by date. Places with few reviews return fewer than asked, and a place with none returns an empty list. A browser not signed in to Google (such as a Reduck cloud browser) only gets Google's limited view, which stops after the first 10 to 30 reviews: the answer then says limitedView is true. A place Google cannot find fails with a clear error.

- Site: google.com
- Address: `reduck/google.com/get_place_reviews`
- Updated: 2026-10-12 (v18)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/google.com/get_place_reviews`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/google.com/get_place_reviews
```

## Input

- `count` (number, optional): How many reviews to return at most. Places with few reviews return fewer.
- `placeId` (string, optional): The Google place id, as google.com/search_places returns it. A place id Google does not know fails with a clear error.
- `placeUrl` (string, optional): The place's Google Maps link, as google.com/get_place returns it in resolvedUrl. The most reliable input; used instead of placeId when both are given.

## Output

- `n` (number, optional): Number of reviews returned. 0 when the place has no reviews at all.
- `reviews` (array, optional)
- `limitedView` (boolean, optional): True when fewer reviews than asked came back because Google showed this browser its limited view, which stops the list after the first reviews until the browser is signed in to Google. False when the count was reached or the place has no more reviews.

## FAQ

### What does "Get Google Maps place reviews" do?

Get the reviews of a Google Maps place, given its place id or its Maps link. Returns how many reviews came back and, for each, the author, their reviewer byline and photo count, the star rating, when it was posted, the full text, the owner's reply, and a stable review id. Reviews come in Google's "most relevant" order, not by date. Places with few reviews return fewer than asked, and a place with none returns an empty list. A browser not signed in to Google (such as a Reduck cloud browser) only gets Google's limited view, which stops after the first 10 to 30 reviews: the answer then says limitedView is true. A place Google cannot find fails with a clear error.

### How do I automatically get Google Maps place reviews on google.com?

Ask an AI agent connected to Reduck to run reduck/google.com/get_place_reviews, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/google.com/get_place_reviews

### Is there a google.com API to get Google Maps place reviews?

You do not need one. "Get Google Maps place reviews" drives the real google.com pages in a browser, so it works whether or not google.com offers an API for this.

### What information do I need to provide?

Optional: count, placeId, placeUrl.

### What does it return?

It returns n, reviews, limitedView.

### Do I need to be logged in to google.com?

No. It only uses pages of google.com that are reachable without signing in.

### Does it change anything on google.com, or only read data?

It only reads. It looks things up on google.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/google.com/get_place_reviews, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/google.com/get_place_reviews

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/google.com/get_place_reviews
