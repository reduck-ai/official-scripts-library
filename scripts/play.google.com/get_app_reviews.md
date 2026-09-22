# Get Google Play app reviews

Automatically get Google Play app reviews on play.google.com. Fetch reviews for an Android app from its Google Play Store listing: reviewer name, star rating, date, and review text. No login required.

- Site: play.google.com
- Address: `reduck/play.google.com/get_app_reviews`
- Updated: 2026-09-08 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/play.google.com/get_app_reviews`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/play.google.com/get_app_reviews
```

## Input

- `package_id` (string, required): Android app package id, e.g. "com.Slack" (from play.google.com/store/apps/details?id=<package_id>)

## Output

- `reviews` (array, required)
- `package_id` (string, required)

## FAQ

### What does "Get Google Play app reviews" do?

Fetch reviews for an Android app from its Google Play Store listing: reviewer name, star rating, date, and review text. No login required.

### How do I automatically get Google Play app reviews on play.google.com?

Ask an AI agent connected to Reduck to run reduck/play.google.com/get_app_reviews, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/play.google.com/get_app_reviews

### Is there a play.google.com API to get Google Play app reviews?

You do not need one. "Get Google Play app reviews" drives the real play.google.com pages in a browser, so it works whether or not play.google.com offers an API for this.

### What information do I need to provide?

Required: package_id.

### What does it return?

It returns reviews, package_id.

### Do I need to be logged in to play.google.com?

No. It only uses pages of play.google.com that are reachable without signing in.

### Does it change anything on play.google.com, or only read data?

It only reads. It looks things up on play.google.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/play.google.com/get_app_reviews, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/play.google.com/get_app_reviews

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/play.google.com/get_app_reviews
