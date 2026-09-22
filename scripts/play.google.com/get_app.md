# Get Google Play app details

Automatically get Google Play app details on play.google.com. Fetch an Android app's store listing details: name, description, developer, category, rating, review count, price, and icon. No login required.

- Site: play.google.com
- Address: `reduck/play.google.com/get_app`
- Updated: 2026-09-02 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/play.google.com/get_app`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/play.google.com/get_app
```

## Input

- `package_id` (string, required): Android app package id, e.g. "com.Slack" (from play.google.com/store/apps/details?id=<package_id>)

## Output

- `available` (boolean, required)
- `package_id` (string, required)
- `free` (boolean | null, optional)
- `name` (string | null, optional)
- `price` (number | null, optional)
- `iconUrl` (string | null, optional)
- `category` (string | null, optional)
- `currency` (string | null, optional)
- `developer` (string | null, optional)
- `description` (string | null, optional)
- `ratingCount` (integer | null, optional)
- `ratingValue` (number | null, optional)
- `contentRating` (string | null, optional)

## FAQ

### What does "Get Google Play app details" do?

Fetch an Android app's store listing details: name, description, developer, category, rating, review count, price, and icon. No login required.

### How do I automatically get Google Play app details on play.google.com?

Ask an AI agent connected to Reduck to run reduck/play.google.com/get_app, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/play.google.com/get_app

### Is there a play.google.com API to get Google Play app details?

You do not need one. "Get Google Play app details" drives the real play.google.com pages in a browser, so it works whether or not play.google.com offers an API for this.

### What information do I need to provide?

Required: package_id.

### What does it return?

It returns free, name, price, iconUrl, category, currency, available, developer, package_id, description, ratingCount, ratingValue, contentRating.

### Do I need to be logged in to play.google.com?

No. It only uses pages of play.google.com that are reachable without signing in.

### Does it change anything on play.google.com, or only read data?

It only reads. It looks things up on play.google.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/play.google.com/get_app, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/play.google.com/get_app

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/play.google.com/get_app
