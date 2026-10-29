# Get Instagram user reels

Automatically get Instagram user reels on instagram.com. Fetch an Instagram user's reels from their profile's Reels tab, in the order the tab shows them. Returns count, complete and reels; each reel has pk, code, url, thumbnail, like_count (null when the owner hides likes), play_count, comment_count and product_type. count=0 returns every reel. complete is true only when the end of the tab was reached, false when count stopped it first. An account with no reels returns an empty list; a username that does not exist fails with an error that says so. Posting date, caption, video link and duration are not in the Reels tab; open a reel to get them.

- Site: instagram.com
- Address: `reduck/instagram.com/get_user_reels`
- Updated: 2026-10-28 (v13)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/instagram.com/get_user_reels`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/instagram.com/get_user_reels
```

## Input

- `username` (string, required): Instagram username without the @, e.g. "nasa"
- `count` (integer, optional): Maximum number of reels to return, in the order the Reels tab shows them. 0 returns all of them.

## Output

- `count` (integer, required): Number of reels returned. 0 when the account has no reels.
- `reels` (array, required)
- `complete` (boolean, required): True when the Reels tab showed its end and every reel is returned. False when count stopped it first.

## FAQ

### What does "Get Instagram user reels" do?

Fetch an Instagram user's reels from their profile's Reels tab, in the order the tab shows them. Returns count, complete and reels; each reel has pk, code, url, thumbnail, like_count (null when the owner hides likes), play_count, comment_count and product_type. count=0 returns every reel. complete is true only when the end of the tab was reached, false when count stopped it first. An account with no reels returns an empty list; a username that does not exist fails with an error that says so. Posting date, caption, video link and duration are not in the Reels tab; open a reel to get them.

### How do I automatically get Instagram user reels on instagram.com?

Ask an AI agent connected to Reduck to run reduck/instagram.com/get_user_reels, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/get_user_reels

### Is there a instagram.com API to get Instagram user reels?

You do not need one. "Get Instagram user reels" drives the real instagram.com pages in a browser, so it works whether or not instagram.com offers an API for this.

### What information do I need to provide?

Required: username. Optional: count.

### What does it return?

It returns count, reels, complete.

### Do I need to be logged in to instagram.com?

Yes. It acts as you on instagram.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the instagram.com cookies saved by the Reduck extension.

### Does it change anything on instagram.com, or only read data?

It only reads. It looks things up on instagram.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/instagram.com/get_user_reels, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/get_user_reels

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/instagram.com/get_user_reels
