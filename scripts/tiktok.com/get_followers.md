# Get TikTok followers

Automatically get TikTok followers on tiktok.com. List a TikTok user's followers by @username, paginated. A handle nobody owns is reported as no such account rather than a vague lookup failure, and an account that will not disclose its followers (private accounts show them only to approved followers) is reported with the reason instead of a bare API code. Note that an account hiding who it follows still discloses its followers normally. Returns total, hasMore, truncated, and users (id, uniqueId, secUid, nickname, signature, verified, privateAccount, followerCount).

- Site: tiktok.com
- Address: `reduck/tiktok.com/get_followers`
- Updated: 2026-09-08 (v6)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/tiktok.com/get_followers`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/tiktok.com/get_followers
```

## Input

- `username` (string, required): TikTok handle, with or without leading @.
- `count` (integer, optional): Target number of followers to collect.

## Output

- `total` (integer, required): Total follower count reported by TikTok.
- `users` (array, required)
- `hasMore` (boolean, required)
- `username` (string, required)
- `truncated` (boolean, optional): True if TikTok flagged the list as truncated (visibility-limited).

## FAQ

### What does "Get TikTok followers" do?

List a TikTok user's followers by @username, paginated. A handle nobody owns is reported as no such account rather than a vague lookup failure, and an account that will not disclose its followers (private accounts show them only to approved followers) is reported with the reason instead of a bare API code. Note that an account hiding who it follows still discloses its followers normally. Returns total, hasMore, truncated, and users (id, uniqueId, secUid, nickname, signature, verified, privateAccount, followerCount).

### How do I automatically get TikTok followers on tiktok.com?

Ask an AI agent connected to Reduck to run reduck/tiktok.com/get_followers, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tiktok.com/get_followers

### Is there a tiktok.com API to get TikTok followers?

You do not need one. "Get TikTok followers" drives the real tiktok.com pages in a browser, so it works whether or not tiktok.com offers an API for this.

### What information do I need to provide?

Required: username. Optional: count.

### What does it return?

It returns total, users, hasMore, username, truncated.

### Do I need to be logged in to tiktok.com?

No. It only uses pages of tiktok.com that are reachable without signing in.

### Does it change anything on tiktok.com, or only read data?

It only reads. It looks things up on tiktok.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/tiktok.com/get_followers, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tiktok.com/get_followers

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/tiktok.com/get_followers
