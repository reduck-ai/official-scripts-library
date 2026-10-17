# Search YouTube videos

Automatically search YouTube videos on youtube.com. Search YouTube videos by query, or list a channel's or playlist's videos from its URL. Returns a list of videos with id, title, url, duration, channelName, channelUrl, viewCount, date, thumbnailUrl, and description.

- Site: youtube.com
- Address: `reduck/youtube.com/search_videos`
- Updated: 2026-10-16 (v8)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/youtube.com/search_videos`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/youtube.com/search_videos
```

## Input

- `query` (string, optional): Free-text search query. Provide this OR channelUrl OR playlistUrl.
- `channelUrl` (string, optional): A channel URL — lists that channel's videos (its /videos tab), newest first. Query params you include are preserved (e.g. ?hl=fr&persist_hl=1 to force the UI locale), and a URL already pointing at /videos is used as-is.
- `maxResults` (integer, optional): Max videos to return. Further pages are loaded until this many videos or the end of the list. Default 20.
- `playlistUrl` (string, optional): A playlist URL — lists that playlist's videos, in playlist order.

## FAQ

### What does "Search YouTube videos" do?

Search YouTube videos by query, or list a channel's or playlist's videos from its URL. Returns a list of videos with id, title, url, duration, channelName, channelUrl, viewCount, date, thumbnailUrl, and description.

### How do I automatically search YouTube videos on youtube.com?

Ask an AI agent connected to Reduck to run reduck/youtube.com/search_videos, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/youtube.com/search_videos

### Is there a youtube.com API to search YouTube videos?

You do not need one. "Search YouTube videos" drives the real youtube.com pages in a browser, so it works whether or not youtube.com offers an API for this.

### What information do I need to provide?

Optional: query, channelUrl, maxResults, playlistUrl.

### Do I need to be logged in to youtube.com?

No. It only uses pages of youtube.com that are reachable without signing in.

### Does it change anything on youtube.com, or only read data?

It only reads. It looks things up on youtube.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/youtube.com/search_videos, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/youtube.com/search_videos

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/youtube.com/search_videos
