# Restaurant TheFork + TripAdvisor ratings

Open a TheFork restaurant page (by slug + legacyId) and read both ratings it carries: TheFork (/10) and TripAdvisor (/5), each with its review count. Works on a fresh or managed browser, and since TheFork is a TripAdvisor company the TripAdvisor rating is included, so no separate TripAdvisor lookup is needed.

- Site: thefork.com
- Address: `reduck/thefork.com/get_ratings`
- Updated: 2026-08-26 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/thefork.com/get_ratings`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/thefork.com/get_ratings
```

## Input

- `slug` (string, required): Restaurant slug, e.g. 'l-atelier-entrecote-volaille-reaumur'.
- `legacyId` (integer, required): Restaurant legacy id, e.g. 817127.

## Output

- `url` (string, optional)
- `name` (string | null, optional)
- `theforkRating` (number | null, optional)
- `theforkReviews` (integer | null, optional)
- `tripadvisorRating` (number | null, optional)
- `tripadvisorReviews` (integer | null, optional)

## FAQ

### What does "Restaurant TheFork + TripAdvisor ratings" do?

Open a TheFork restaurant page (by slug + legacyId) and read both ratings it carries: TheFork (/10) and TripAdvisor (/5), each with its review count. Works on a fresh or managed browser, and since TheFork is a TripAdvisor company the TripAdvisor rating is included, so no separate TripAdvisor lookup is needed.

### What information do I need to provide?

Required: slug, legacyId.

### What does it return?

It returns url, name, theforkRating, theforkReviews, tripadvisorRating, tripadvisorReviews.

### Do I need to be logged in to thefork.com?

No. It only uses pages of thefork.com that are reachable without signing in.

### Does it change anything on thefork.com, or only read data?

It only reads. It looks things up on thefork.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/thefork.com/get_ratings, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/thefork.com/get_ratings

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/thefork.com/get_ratings
