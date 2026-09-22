# Get App Store app reviews

Automatically get App Store app reviews on apps.apple.com. Read an App Store app's customer reviews and aggregate rating from its public "Ratings & Reviews" page, for any storefront country. Returns averageRating, the site's own ratings-count text, and the reviews the page renders (id, title, rating 1-5, author, ISO date, full body). Anonymous, read-only. Apple's web page serves a fixed first page of ~10 reviews and exposes no pagination, offset or sort control at all, so that is the ceiling — deeper history is not a web affordance.

- Site: apps.apple.com
- Address: `reduck/apps.apple.com/get_app_reviews`
- Updated: 2026-09-18 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/apps.apple.com/get_app_reviews`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/apps.apple.com/get_app_reviews
```

## Input

- `appId` (string | number, required): The numeric App Store app id, as it appears in the URL apps.apple.com/<country>/app/<slug>/id<appId> — e.g. 324684580 for Spotify. A leading "id" is accepted and stripped.
- `country` (string, optional): Two-letter App Store storefront code (us, fr, jp, gb, de...). Reviews, the app name and the ratings-count text are storefront-specific: the same app returns different reviews and a different average per country.

## Output

- `url` (string, required): The reviews page actually landed on, after Apple's slug redirect.
- `appId` (string, required): The app id as requested (echoed for joining).
- `appName` (string | null, required): App name as rendered in this storefront's locale.
- `country` (string, required)
- `reviews` (array, required): Empty array is a legitimate outcome for an app whose page renders no reviews.
- `reviewCount` (integer, required): Number of reviews returned — how many this page rendered, not the app's total review count.
- `averageRating` (number | null, required): Average star rating out of 5. Parsed from the site's own average-rating element; comma decimals (fr) are normalised to a dot.
- `ratingsCountText` (string | null, required): The ratings total exactly as the site renders it, verbatim and locale-specific ("42M Ratings", "4,7 M notes", "評価件数：51万"). Deliberately not parsed to a number: Apple abbreviates and localises this, so any parse would be lossy or wrong.

## FAQ

### What does "Get App Store app reviews" do?

Read an App Store app's customer reviews and aggregate rating from its public "Ratings & Reviews" page, for any storefront country. Returns averageRating, the site's own ratings-count text, and the reviews the page renders (id, title, rating 1-5, author, ISO date, full body). Anonymous, read-only. Apple's web page serves a fixed first page of ~10 reviews and exposes no pagination, offset or sort control at all, so that is the ceiling — deeper history is not a web affordance.

### How do I automatically get App Store app reviews on apps.apple.com?

Ask an AI agent connected to Reduck to run reduck/apps.apple.com/get_app_reviews, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/apps.apple.com/get_app_reviews

### Is there a apps.apple.com API to get App Store app reviews?

You do not need one. "Get App Store app reviews" drives the real apps.apple.com pages in a browser, so it works whether or not apps.apple.com offers an API for this.

### What information do I need to provide?

Required: appId. Optional: country.

### What does it return?

It returns url, appId, appName, country, reviews, reviewCount, averageRating, ratingsCountText.

### Do I need to be logged in to apps.apple.com?

No. It only uses pages of apps.apple.com that are reachable without signing in.

### Does it change anything on apps.apple.com, or only read data?

It only reads. It looks things up on apps.apple.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/apps.apple.com/get_app_reviews, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/apps.apple.com/get_app_reviews

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/apps.apple.com/get_app_reviews
