# Get TikTok hashtag info

Automatically get TikTok hashtag info on tiktok.com. Get a TikTok hashtag/challenge's stats (exact video & view counts), id, title and description by name (with or without a leading #). TikTok removed the web hashtag video feed, so only the hashtag's metadata is available — to list videos, use search_videos by keyword.

- Site: tiktok.com
- Address: `reduck/tiktok.com/get_hashtag_info`
- Updated: 2026-09-03 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/tiktok.com/get_hashtag_info`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/tiktok.com/get_hashtag_info
```

## Input

- `hashtag` (string, required): Hashtag/challenge name, with or without a leading # (e.g. "booktok" or "#BookTok"). Case-insensitive; TikTok normalises it.

## Output

- `id` (string, required): The challenge's numeric id.
- `title` (string, required): Normalised hashtag name (lowercase, no #).
- `viewCount` (number, required): Exact cumulative view count (from statsV2).
- `isCommerce` (boolean, required)
- `videoCount` (number, required): Exact number of videos under the hashtag (from statsV2).
- `desc` (string | null, optional): Curated hashtag description, when TikTok set one.
- `cover` (string | null, optional): Cover image URL, when set. Signed and expires within hours.

## FAQ

### What does "Get TikTok hashtag info" do?

Get a TikTok hashtag/challenge's stats (exact video & view counts), id, title and description by name (with or without a leading #). TikTok removed the web hashtag video feed, so only the hashtag's metadata is available — to list videos, use search_videos by keyword.

### How do I automatically get TikTok hashtag info on tiktok.com?

Ask an AI agent connected to Reduck to run reduck/tiktok.com/get_hashtag_info, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tiktok.com/get_hashtag_info

### Is there a tiktok.com API to get TikTok hashtag info?

You do not need one. "Get TikTok hashtag info" drives the real tiktok.com pages in a browser, so it works whether or not tiktok.com offers an API for this.

### What information do I need to provide?

Required: hashtag.

### What does it return?

It returns id, desc, cover, title, viewCount, isCommerce, videoCount.

### Do I need to be logged in to tiktok.com?

No. It only uses pages of tiktok.com that are reachable without signing in.

### Does it change anything on tiktok.com, or only read data?

Unknown: its author has not declared whether it changes anything on tiktok.com, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/tiktok.com/get_hashtag_info, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tiktok.com/get_hashtag_info

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/tiktok.com/get_hashtag_info
