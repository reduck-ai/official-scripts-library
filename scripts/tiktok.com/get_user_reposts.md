# Get TikTok user reposts

Automatically get TikTok user reposts on tiktok.com. List the videos a TikTok user has reposted (from their Reposts tab), by @username, up to `count`.

- Site: tiktok.com
- Address: `reduck/tiktok.com/get_user_reposts`
- Updated: 2026-09-03 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/tiktok.com/get_user_reposts`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/tiktok.com/get_user_reposts
```

## Input

- `username` (string, required): TikTok handle, with or without leading @.
- `count` (integer, optional): Target number of reposts to collect; pages until this many are gathered or the list ends.

## Output

- `videos` (array, required): Reposted videos, in repost order. Each video's author is the ORIGINAL creator, not the reposting user.
- `hasMore` (boolean, required)
- `username` (string, required)

## FAQ

### What does "Get TikTok user reposts" do?

List the videos a TikTok user has reposted (from their Reposts tab), by @username, up to `count`.

### How do I automatically get TikTok user reposts on tiktok.com?

Ask an AI agent connected to Reduck to run reduck/tiktok.com/get_user_reposts, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tiktok.com/get_user_reposts

### Is there a tiktok.com API to get TikTok user reposts?

You do not need one. "Get TikTok user reposts" drives the real tiktok.com pages in a browser, so it works whether or not tiktok.com offers an API for this.

### What information do I need to provide?

Required: username. Optional: count.

### What does it return?

It returns videos, hasMore, username.

### Do I need to be logged in to tiktok.com?

Yes. It acts as you on tiktok.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the tiktok.com cookies saved by the Reduck extension.

### Does it change anything on tiktok.com, or only read data?

Unknown: its author has not declared whether it changes anything on tiktok.com, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/tiktok.com/get_user_reposts, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tiktok.com/get_user_reposts

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/tiktok.com/get_user_reposts
