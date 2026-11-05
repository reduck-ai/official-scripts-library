# Get TikTok search suggestions

Automatically get TikTok search suggestions on tiktok.com. Get the search suggestions TikTok shows as you type a query, in TikTok's order. Suggestions that start with # are hashtags (marked isHashtag). TikTok web has no hashtag results page, so this is the way to find hashtags from a keyword. An empty list means TikTok has no suggestion for the query.

- Site: tiktok.com
- Address: `reduck/tiktok.com/get_search_suggestions`
- Updated: 2026-11-04 (v6)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/tiktok.com/get_search_suggestions`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/tiktok.com/get_search_suggestions
```

## Input

- `query` (string, required): Free-text query, e.g. "puppy" or "#booktok". TikTok returns up to ~10 autocomplete suggestions.

## Output

- `query` (string, required)
- `suggestions` (array, required)

## FAQ

### What does "Get TikTok search suggestions" do?

Get the search suggestions TikTok shows as you type a query, in TikTok's order. Suggestions that start with # are hashtags (marked isHashtag). TikTok web has no hashtag results page, so this is the way to find hashtags from a keyword. An empty list means TikTok has no suggestion for the query.

### How do I automatically get TikTok search suggestions on tiktok.com?

Ask an AI agent connected to Reduck to run reduck/tiktok.com/get_search_suggestions, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tiktok.com/get_search_suggestions

### Is there a tiktok.com API to get TikTok search suggestions?

You do not need one. "Get TikTok search suggestions" drives the real tiktok.com pages in a browser, so it works whether or not tiktok.com offers an API for this.

### What information do I need to provide?

Required: query.

### What does it return?

It returns query, suggestions.

### Do I need to be logged in to tiktok.com?

No. It only uses pages of tiktok.com that are reachable without signing in.

### Does it change anything on tiktok.com, or only read data?

It only reads. It looks things up on tiktok.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/tiktok.com/get_search_suggestions, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tiktok.com/get_search_suggestions

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/tiktok.com/get_search_suggestions
