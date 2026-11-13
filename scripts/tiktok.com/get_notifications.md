# Get TikTok notifications

Automatically get TikTok notifications on tiktok.com. List the logged-in account's activity notifications (the Activité inbox): likes, follows, comments and mentions received, newest first. Each notification carries who triggered it, the target video/comment, and read state.

- Site: tiktok.com
- Address: `reduck/tiktok.com/get_notifications`
- Updated: 2026-11-12 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/tiktok.com/get_notifications`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/tiktok.com/get_notifications
```

## Input

- `cursor` (string, optional): The cursor a previous run returned, for the next (older) page. Omit for the newest page.

## Output

- `cursor` (string | null, required): Pass as cursor to get the next (older) page; null on the last page.
- `hasMore` (boolean, required): True when TikTok has older notifications.
- `notifications` (array, required): Newest first, as TikTok gives them.

## FAQ

### What does "Get TikTok notifications" do?

List the logged-in account's activity notifications (the Activité inbox): likes, follows, comments and mentions received, newest first. Each notification carries who triggered it, the target video/comment, and read state.

### How do I automatically get TikTok notifications on tiktok.com?

Ask an AI agent connected to Reduck to run reduck/tiktok.com/get_notifications, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tiktok.com/get_notifications

### Is there a tiktok.com API to get TikTok notifications?

You do not need one. "Get TikTok notifications" drives the real tiktok.com pages in a browser, so it works whether or not tiktok.com offers an API for this.

### What information do I need to provide?

Optional: cursor.

### What does it return?

It returns cursor, hasMore, notifications.

### Do I need to be logged in to tiktok.com?

Yes. It acts as you on tiktok.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the tiktok.com cookies saved by the Reduck extension.

### Does it change anything on tiktok.com, or only read data?

It only reads. It looks things up on tiktok.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/tiktok.com/get_notifications, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tiktok.com/get_notifications

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/tiktok.com/get_notifications
