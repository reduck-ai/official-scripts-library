# Get TikTok profile

Automatically get TikTok profile on tiktok.com. Get a TikTok user's profile (bio, stats, verified, secUid) by @username.

- Site: tiktok.com
- Address: `reduck/tiktok.com/get_profile`
- Updated: 2026-09-08 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/tiktok.com/get_profile`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/tiktok.com/get_profile
```

## Input

- `username` (string, required): TikTok handle, with or without leading @ (e.g. "tiktok" or "@tiktok").

## Output

- `id` (string, required)
- `stats` (object, required): Exact counts from statsV2 (numbers).
- `secUid` (string, required): Stable opaque id; join key for video/feed APIs.
- `nickname` (string, required)
- `uniqueId` (string, required)
- `verified` (boolean, required)
- `privateAccount` (boolean, required)
- `avatar` (string | null, optional): Largest avatar URL; signed, expires within hours.
- `region` (string | null, optional)
- `bioLink` (string | null, optional)
- `category` (string | null, optional): Commerce/account category, null if not a commerce account.
- `signature` (string | null, optional): Bio text.
- `createTime` (integer | null, optional): Account creation, unix seconds.

## FAQ

### What does "Get TikTok profile" do?

Get a TikTok user's profile (bio, stats, verified, secUid) by @username.

### How do I automatically get TikTok profile on tiktok.com?

Ask an AI agent connected to Reduck to run reduck/tiktok.com/get_profile, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tiktok.com/get_profile

### Is there a tiktok.com API to get TikTok profile?

You do not need one. "Get TikTok profile" drives the real tiktok.com pages in a browser, so it works whether or not tiktok.com offers an API for this.

### What information do I need to provide?

Required: username.

### What does it return?

It returns id, stats, avatar, region, secUid, bioLink, category, nickname, uniqueId, verified, signature, createTime, privateAccount.

### Do I need to be logged in to tiktok.com?

No. It only uses pages of tiktok.com that are reachable without signing in.

### Does it change anything on tiktok.com, or only read data?

It only reads. It looks things up on tiktok.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/tiktok.com/get_profile, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tiktok.com/get_profile

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/tiktok.com/get_profile
