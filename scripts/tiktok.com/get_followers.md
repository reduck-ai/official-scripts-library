# Get TikTok followers

Automatically get TikTok followers on tiktok.com. List a TikTok user's followers by @username, one page at a time, newest first as TikTok gives them, with the total count. Pass the returned cursor to get the next page; cursor is null on the last page. A username nobody owns, or an account whose followers TikTok does not show (a private account), is an error with the reason.

- Site: tiktok.com
- Address: `reduck/tiktok.com/get_followers`
- Updated: 2026-11-19 (v8)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/tiktok.com/get_followers`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/tiktok.com/get_followers
```

## Input

- `username` (string, required): TikTok handle, with or without leading @.
- `count` (integer, optional): How many followers to ask TikTok for on this page.
- `cursor` (string, optional): Where the page starts: "0" for the first page, then the cursor a previous run returned.

## Output

- `total` (integer, required): Total follower count reported by TikTok.
- `users` (array, required)
- `cursor` (string | null, required): Pass as cursor for the next page; null when there is none.
- `hasMore` (boolean, required)
- `username` (string, required)
- `truncated` (boolean, optional): True if TikTok flagged the list as truncated (visibility-limited).

## FAQ

### What does "Get TikTok followers" do?

List a TikTok user's followers by @username, one page at a time, newest first as TikTok gives them, with the total count. Pass the returned cursor to get the next page; cursor is null on the last page. A username nobody owns, or an account whose followers TikTok does not show (a private account), is an error with the reason.

### How do I automatically get TikTok followers on tiktok.com?

Ask an AI agent connected to Reduck to run reduck/tiktok.com/get_followers, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tiktok.com/get_followers

### Is there a tiktok.com API to get TikTok followers?

You do not need one. "Get TikTok followers" drives the real tiktok.com pages in a browser, so it works whether or not tiktok.com offers an API for this.

### What information do I need to provide?

Required: username. Optional: count, cursor.

### What does it return?

It returns total, users, cursor, hasMore, username, truncated.

### Do I need to be logged in to tiktok.com?

No. It only uses pages of tiktok.com that are reachable without signing in.

### Does it change anything on tiktok.com, or only read data?

It only reads. It looks things up on tiktok.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/tiktok.com/get_followers, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tiktok.com/get_followers

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/tiktok.com/get_followers
