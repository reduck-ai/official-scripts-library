# Trending Now searches

Google Trends "Trending Now": every trending search for a country over the last 4h/24h/48h/7d — title, search volume, growth %, start/end time, active flag, breakdown terms.

- Site: trends.google.com
- Address: `reduck/trends.google.com/trending_now`
- Updated: 2026-07-13 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/trends.google.com/trending_now`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/trends.google.com/trending_now
```

## Input

- `geo` (string, optional): ISO country code (e.g. "US", "FR", "DE"). Trending Now is per-country; no worldwide view.
- `hours` (integer, optional): Lookback window: 4, 24, 48 hours or 168 (7 days) — the same options as the site's time picker.
- `category` (integer, optional): Optional Trending Now category id (site's category picker). Omit for all categories.

## Output

- `geo` (string, required)
- `hours` (integer, required)
- `trends` (array, required): Every trend in the window (the full dataset behind the page, not just the first rendered page of rows).

## FAQ

### What does "Trending Now searches" do?

Google Trends "Trending Now": every trending search for a country over the last 4h/24h/48h/7d — title, search volume, growth %, start/end time, active flag, breakdown terms.

### What information do I need to provide?

Optional: geo, hours, category.

### What does it return?

It returns geo, hours, trends.

### Do I need to be logged in to trends.google.com?

No. It only uses pages of trends.google.com that are reachable without signing in.

### Does it change anything on trends.google.com, or only read data?

Unknown: its author has not declared whether it changes anything on trends.google.com, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/trends.google.com/trending_now, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/trends.google.com/trending_now

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/trends.google.com/trending_now
