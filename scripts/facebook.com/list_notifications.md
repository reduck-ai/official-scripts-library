# Get your Facebook notifications automatically

Automatically get your Facebook notifications automatically on facebook.com. Get your Facebook notifications automatically as structured rows, instead of turning on push notifications and reading them by hand. List your Facebook notifications, each with a machine-readable type — a group accepted your join request, an admin approved your post, someone commented on your post, a new follower, and so on. Each row carries the text shown, whether it is unread, its displayed age, and a direct link to the item it is about, so one call tells you everything that changed without visiting each group.

- Site: facebook.com
- Address: `reduck/facebook.com/list_notifications`
- Updated: 2026-09-19 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/facebook.com/list_notifications`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/facebook.com/list_notifications
```

## Input

- `limit` (integer, optional): Max notifications to return; the script scrolls the list until it has this many or the feed stops yielding new rows.
- `types` (array, optional): Optional filter on the machine type (e.g. ["group_comment", "group_post_approved"]). Omit for all.

## FAQ

### What does "Get your Facebook notifications automatically" do?

Get your Facebook notifications automatically as structured rows, instead of turning on push notifications and reading them by hand. List your Facebook notifications, each with a machine-readable type — a group accepted your join request, an admin approved your post, someone commented on your post, a new follower, and so on. Each row carries the text shown, whether it is unread, its displayed age, and a direct link to the item it is about, so one call tells you everything that changed without visiting each group.

### How do I automatically get your Facebook notifications automatically on facebook.com?

Ask an AI agent connected to Reduck to run reduck/facebook.com/list_notifications, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/facebook.com/list_notifications

### Is there a facebook.com API to get your Facebook notifications automatically?

You do not need one. "Get your Facebook notifications automatically" drives the real facebook.com pages in a browser, so it works whether or not facebook.com offers an API for this.

### What information do I need to provide?

Optional: limit, types.

### Do I need to be logged in to facebook.com?

Yes. It acts as you on facebook.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the facebook.com cookies saved by the Reduck extension.

### Does it change anything on facebook.com, or only read data?

It only reads. It looks things up on facebook.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/facebook.com/list_notifications, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/facebook.com/list_notifications

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/facebook.com/list_notifications
