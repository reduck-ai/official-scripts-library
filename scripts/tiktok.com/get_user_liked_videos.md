# Get TikTok user liked videos

Automatically get TikTok user liked videos on tiktok.com. List the videos a TikTok user has liked (their Liked tab), by @username. Returns [] unless the account has set Liked videos to public (private by default).

- Site: tiktok.com
- Address: `reduck/tiktok.com/get_user_liked_videos`
- Updated: 2026-09-03 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/tiktok.com/get_user_liked_videos`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/tiktok.com/get_user_liked_videos
```

## Input

- `username` (string, required): TikTok handle, with or without leading @.
- `count` (integer, optional): Target number of liked videos to collect; pages until this many are gathered or the list ends.

## Output

- `videos` (array, required): Liked videos (each authored by its ORIGINAL creator). Empty when the account keeps its Liked list private, which is the default — an empty array is not an error.
- `hasMore` (boolean, required)
- `username` (string, required)

## FAQ

### What does "Get TikTok user liked videos" do?

List the videos a TikTok user has liked (their Liked tab), by @username. Returns [] unless the account has set Liked videos to public (private by default).

### How do I automatically get TikTok user liked videos on tiktok.com?

Ask an AI agent connected to Reduck to run reduck/tiktok.com/get_user_liked_videos, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tiktok.com/get_user_liked_videos

### Is there a tiktok.com API to get TikTok user liked videos?

You do not need one. "Get TikTok user liked videos" drives the real tiktok.com pages in a browser, so it works whether or not tiktok.com offers an API for this.

### What information do I need to provide?

Required: username. Optional: count.

### What does it return?

It returns videos, hasMore, username.

### Do I need to be logged in to tiktok.com?

Yes. It acts as you on tiktok.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the tiktok.com cookies saved by the Reduck extension.

### Does it change anything on tiktok.com, or only read data?

Unknown: its author has not declared whether it changes anything on tiktok.com, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/tiktok.com/get_user_liked_videos, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tiktok.com/get_user_liked_videos

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/tiktok.com/get_user_liked_videos
