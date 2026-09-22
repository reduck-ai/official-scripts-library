# Get Instagram user reels

Automatically get Instagram user reels on instagram.com. Fetch an Instagram user's reels by their username; count=0 returns all. Returns pk, code, url, taken_at, caption, thumbnail, video_url, like_count, play_count, comment_count, and video_duration. Results follow the profile feed order, not strictly newest-first.

- Site: instagram.com
- Address: `reduck/instagram.com/get_user_reels`
- Updated: 2026-09-10 (v5)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/instagram.com/get_user_reels`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/instagram.com/get_user_reels
```

## Input

- `username` (string, required): Instagram username without the @, e.g. "nasa"
- `count` (integer, optional): Maximum number of reels to return. 0 returns all reels found by paginating the profile feed.

## FAQ

### What does "Get Instagram user reels" do?

Fetch an Instagram user's reels by their username; count=0 returns all. Returns pk, code, url, taken_at, caption, thumbnail, video_url, like_count, play_count, comment_count, and video_duration. Results follow the profile feed order, not strictly newest-first.

### How do I automatically get Instagram user reels on instagram.com?

Ask an AI agent connected to Reduck to run reduck/instagram.com/get_user_reels, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/get_user_reels

### Is there a instagram.com API to get Instagram user reels?

You do not need one. "Get Instagram user reels" drives the real instagram.com pages in a browser, so it works whether or not instagram.com offers an API for this.

### What information do I need to provide?

Required: username. Optional: count.

### Do I need to be logged in to instagram.com?

Yes. It acts as you on instagram.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the instagram.com cookies saved by the Reduck extension.

### Does it change anything on instagram.com, or only read data?

It only reads. It looks things up on instagram.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/instagram.com/get_user_reels, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/get_user_reels

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/instagram.com/get_user_reels
