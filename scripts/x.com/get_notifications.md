# Get X notifications

Automatically get X notifications on x.com. List the logged-in account's Notifications > All tab (not just mentions) — follows, likes, retweets, replies and other notification types X surfaces there. Returns per notification: id, type (a stable X-internal event key, e.g. users_followed_you), icon, text (the rendered notification sentence), url (the notification's target link, if any), timestamp_ms, and users (the accounts referenced in the notification text, with id/handle/name). Scrolls until count is met or the feed dries up.

- Site: x.com
- Address: `reduck/x.com/get_notifications`
- Updated: 2026-09-03 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/x.com/get_notifications`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/x.com/get_notifications
```

## Input

- `count` (integer, optional): Max notifications to return. Default 50.

## Output

- `count` (integer, required): Number of notifications returned. 0 is a first-class outcome (no notifications).
- `notifications` (array, required)

## FAQ

### What does "Get X notifications" do?

List the logged-in account's Notifications > All tab (not just mentions) — follows, likes, retweets, replies and other notification types X surfaces there. Returns per notification: id, type (a stable X-internal event key, e.g. users_followed_you), icon, text (the rendered notification sentence), url (the notification's target link, if any), timestamp_ms, and users (the accounts referenced in the notification text, with id/handle/name). Scrolls until count is met or the feed dries up.

### How do I automatically get X notifications on x.com?

Ask an AI agent connected to Reduck to run reduck/x.com/get_notifications, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/x.com/get_notifications

### Is there a x.com API to get X notifications?

You do not need one. "Get X notifications" drives the real x.com pages in a browser, so it works whether or not x.com offers an API for this.

### What information do I need to provide?

Optional: count.

### What does it return?

It returns count, notifications.

### Do I need to be logged in to x.com?

Yes. It acts as you on x.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the x.com cookies saved by the Reduck extension.

### Does it change anything on x.com, or only read data?

It only reads. It looks things up on x.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/x.com/get_notifications, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/x.com/get_notifications

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/x.com/get_notifications
