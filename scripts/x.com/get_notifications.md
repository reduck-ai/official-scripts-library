# Read your X (Twitter) notifications

Automatically read your X (Twitter) notifications on x.com. Lists the signed-in X account's notifications from the All tab: follows, likes, reposts, replies and other kinds. Each has an id, type, icon, the notification sentence, its link, time and the accounts it names. Returns up to count notifications, with complete true when the feed had no more.

- Site: x.com
- Address: `reduck/x.com/get_notifications`
- Updated: 2026-11-03 (v4)
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
- `complete` (boolean, required): True when the feed had no more notifications; false when count stopped the list first.
- `notifications` (array, required)

## FAQ

### What does "Read your X (Twitter) notifications" do?

Lists the signed-in X account's notifications from the All tab: follows, likes, reposts, replies and other kinds. Each has an id, type, icon, the notification sentence, its link, time and the accounts it names. Returns up to count notifications, with complete true when the feed had no more.

### How do I automatically read your X (Twitter) notifications on x.com?

Ask an AI agent connected to Reduck to run reduck/x.com/get_notifications, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/x.com/get_notifications

### Is there a x.com API to read your X (Twitter) notifications?

You do not need one. "Read your X (Twitter) notifications" drives the real x.com pages in a browser, so it works whether or not x.com offers an API for this.

### What information do I need to provide?

Optional: count.

### What does it return?

It returns count, complete, notifications.

### Do I need to be logged in to x.com?

Yes. It acts as you on x.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the x.com cookies saved by the Reduck extension.

### Does it change anything on x.com, or only read data?

It only reads. It looks things up on x.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/x.com/get_notifications, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/x.com/get_notifications

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/x.com/get_notifications
