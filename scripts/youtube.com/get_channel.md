# Get YouTube channel stats

Automatically get YouTube channel stats on youtube.com. Get a YouTube channel's stats and profile from a @handle, channel id (UC...) or channel URL. Returns channel_id, handle, name, description, subscribers, video_count, view_count, joined, country, channel_url, avatar, rss_url, is_family_safe, keywords and links. Subscribers is the abbreviated public figure (e.g. 4.51m becomes 4510000, approximate), while video_count and view_count are exact; joined is a display string (e.g. "1 Feb 2015") and each link's url is the display host without scheme.

- Site: youtube.com
- Address: `reduck/youtube.com/get_channel`
- Updated: 2026-08-14 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/youtube.com/get_channel`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/youtube.com/get_channel
```

## Input

- `channel` (string, required): A @handle (e.g. @RickAstleyYT or RickAstleyYT), a channel id (UC…), or a full channel URL.

## Output

- `name` (string | null, required)
- `channel_id` (string, required)
- `links` (array, optional)
- `avatar` (string | null, optional)
- `handle` (string | null, optional)
- `joined` (string | null, optional)
- `country` (string | null, optional)
- `rss_url` (string | null, optional)
- `keywords` (string | null, optional)
- `view_count` (integer | null, optional)
- `channel_url` (string | null, optional)
- `description` (string | null, optional)
- `subscribers` (integer | null, optional): Approximate, parsed from YouTube's abbreviated public count.
- `video_count` (integer | null, optional)
- `is_family_safe` (boolean | null, optional)
- `subscribers_text` (string | null, optional)

## FAQ

### What does "Get YouTube channel stats" do?

Get a YouTube channel's stats and profile from a @handle, channel id (UC...) or channel URL. Returns channel_id, handle, name, description, subscribers, video_count, view_count, joined, country, channel_url, avatar, rss_url, is_family_safe, keywords and links. Subscribers is the abbreviated public figure (e.g. 4.51m becomes 4510000, approximate), while video_count and view_count are exact; joined is a display string (e.g. "1 Feb 2015") and each link's url is the display host without scheme.

### How do I automatically get YouTube channel stats on youtube.com?

Ask an AI agent connected to Reduck to run reduck/youtube.com/get_channel, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/youtube.com/get_channel

### Is there a youtube.com API to get YouTube channel stats?

You do not need one. "Get YouTube channel stats" drives the real youtube.com pages in a browser, so it works whether or not youtube.com offers an API for this.

### What information do I need to provide?

Required: channel.

### What does it return?

It returns name, links, avatar, handle, joined, country, rss_url, keywords, channel_id, view_count, channel_url, description, subscribers, video_count, is_family_safe, subscribers_text.

### Do I need to be logged in to youtube.com?

No. It only uses pages of youtube.com that are reachable without signing in.

### Does it change anything on youtube.com, or only read data?

It only reads. It looks things up on youtube.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/youtube.com/get_channel, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/youtube.com/get_channel

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/youtube.com/get_channel
