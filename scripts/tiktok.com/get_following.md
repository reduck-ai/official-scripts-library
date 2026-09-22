# Get TikTok following

Automatically get TikTok following on tiktok.com. List who a TikTok user follows, by @username. Accounts that keep their following list hidden, and private accounts, are reported with a clear reason instead of an empty or partial list; a handle nobody owns is reported as such. For third-party accounts, TikTok caps the list and pads short ones with suggested accounts, so check `total` and `truncated`; results are only fully reliable for accounts you can see in full, such as your own.

- Site: tiktok.com
- Address: `reduck/tiktok.com/get_following`
- Updated: 2026-09-08 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/tiktok.com/get_following`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/tiktok.com/get_following
```

## Input

- `username` (string, required): TikTok handle, with or without leading @.
- `count` (integer, optional): Target number to collect. The returned list may include TikTok's suggested accounts when the real following list is short or restricted; `total` is the declared following count.

## Output

- `total` (integer, required): Declared following count. If less than users.length, the list is padded with suggestions.
- `users` (array, required)
- `hasMore` (boolean, required)
- `username` (string, required)
- `truncated` (boolean, optional): True if TikTok flagged the list as visibility-truncated.

## FAQ

### What does "Get TikTok following" do?

List who a TikTok user follows, by @username. Accounts that keep their following list hidden, and private accounts, are reported with a clear reason instead of an empty or partial list; a handle nobody owns is reported as such. For third-party accounts, TikTok caps the list and pads short ones with suggested accounts, so check `total` and `truncated`; results are only fully reliable for accounts you can see in full, such as your own.

### How do I automatically get TikTok following on tiktok.com?

Ask an AI agent connected to Reduck to run reduck/tiktok.com/get_following, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tiktok.com/get_following

### Is there a tiktok.com API to get TikTok following?

You do not need one. "Get TikTok following" drives the real tiktok.com pages in a browser, so it works whether or not tiktok.com offers an API for this.

### What information do I need to provide?

Required: username. Optional: count.

### What does it return?

It returns total, users, hasMore, username, truncated.

### Do I need to be logged in to tiktok.com?

No. It only uses pages of tiktok.com that are reachable without signing in.

### Does it change anything on tiktok.com, or only read data?

It only reads. It looks things up on tiktok.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/tiktok.com/get_following, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tiktok.com/get_following

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/tiktok.com/get_following
