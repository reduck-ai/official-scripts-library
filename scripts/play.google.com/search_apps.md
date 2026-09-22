# Search Google Play apps

Automatically search Google Play apps on play.google.com. Search the Google Play Store for apps by keyword: package id, name, developer, rating, and icon for each result. No login required.

- Site: play.google.com
- Address: `reduck/play.google.com/search_apps`
- Updated: 2026-09-02 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/play.google.com/search_apps`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/play.google.com/search_apps
```

## Input

- `query` (string, required): Search keywords, e.g. "notion"

## Output

- `query` (string, required)
- `results` (array, required)

## FAQ

### What does "Search Google Play apps" do?

Search the Google Play Store for apps by keyword: package id, name, developer, rating, and icon for each result. No login required.

### How do I automatically search Google Play apps on play.google.com?

Ask an AI agent connected to Reduck to run reduck/play.google.com/search_apps, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/play.google.com/search_apps

### Is there a play.google.com API to search Google Play apps?

You do not need one. "Search Google Play apps" drives the real play.google.com pages in a browser, so it works whether or not play.google.com offers an API for this.

### What information do I need to provide?

Required: query.

### What does it return?

It returns query, results.

### Do I need to be logged in to play.google.com?

No. It only uses pages of play.google.com that are reachable without signing in.

### Does it change anything on play.google.com, or only read data?

It only reads. It looks things up on play.google.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/play.google.com/search_apps, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/play.google.com/search_apps

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/play.google.com/search_apps
