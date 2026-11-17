# Get TikTok user favorites

Automatically get TikTok user favorites on tiktok.com. List the videos a TikTok user has added to their Favorites, by @username, one page per run (pass the returned cursor for the next). Fails with an error when the account keeps its Favorites private (the default).

- Site: tiktok.com
- Address: `reduck/tiktok.com/get_user_favorites`
- Updated: 2026-11-16 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/tiktok.com/get_user_favorites`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/tiktok.com/get_user_favorites
```

## Input

- `username` (string, required): TikTok handle, with or without the leading @.
- `cursor` (string, optional): The cursor a previous run returned, for the next page. Omit for the first page.

## Output

- `cursor` (string | null, required): Pass as cursor to get the next page; null on the last page.
- `videos` (array, required): Favourited videos in TikTok's order. Each author is the original creator.
- `hasMore` (boolean, required): True when TikTok has another page.
- `username` (string, required)

## FAQ

### What does "Get TikTok user favorites" do?

List the videos a TikTok user has added to their Favorites, by @username, one page per run (pass the returned cursor for the next). Fails with an error when the account keeps its Favorites private (the default).

### How do I automatically get TikTok user favorites on tiktok.com?

Ask an AI agent connected to Reduck to run reduck/tiktok.com/get_user_favorites, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tiktok.com/get_user_favorites

### Is there a tiktok.com API to get TikTok user favorites?

You do not need one. "Get TikTok user favorites" drives the real tiktok.com pages in a browser, so it works whether or not tiktok.com offers an API for this.

### What information do I need to provide?

Required: username. Optional: cursor.

### What does it return?

It returns cursor, videos, hasMore, username.

### Do I need to be logged in to tiktok.com?

Yes. It acts as you on tiktok.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the tiktok.com cookies saved by the Reduck extension.

### Does it change anything on tiktok.com, or only read data?

It only reads. It looks things up on tiktok.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/tiktok.com/get_user_favorites, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tiktok.com/get_user_favorites

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/tiktok.com/get_user_favorites
