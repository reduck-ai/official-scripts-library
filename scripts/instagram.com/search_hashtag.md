# Search Instagram hashtags

Automatically search Instagram hashtags on instagram.com. Search Instagram hashtags by keyword. Returns matching hashtags with name, media_count (posts using the tag), and formatted_media_count. Pass the term without the leading #.

- Site: instagram.com
- Address: `reduck/instagram.com/search_hashtag`
- Updated: 2026-10-22 (v6)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/instagram.com/search_hashtag`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/instagram.com/search_hashtag
```

## Input

- `query` (string, required): Hashtag term without the leading #, e.g. "space".
- `count` (integer, optional): Upper bound on hashtags returned. Instagram may suggest fewer than this.

## FAQ

### What does "Search Instagram hashtags" do?

Search Instagram hashtags by keyword. Returns matching hashtags with name, media_count (posts using the tag), and formatted_media_count. Pass the term without the leading #.

### How do I automatically search Instagram hashtags on instagram.com?

Ask an AI agent connected to Reduck to run reduck/instagram.com/search_hashtag, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/search_hashtag

### Is there a instagram.com API to search Instagram hashtags?

You do not need one. "Search Instagram hashtags" drives the real instagram.com pages in a browser, so it works whether or not instagram.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: count.

### Do I need to be logged in to instagram.com?

No. It only uses pages of instagram.com that are reachable without signing in.

### Does it change anything on instagram.com, or only read data?

It only reads. It looks things up on instagram.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/instagram.com/search_hashtag, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/search_hashtag

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/instagram.com/search_hashtag
