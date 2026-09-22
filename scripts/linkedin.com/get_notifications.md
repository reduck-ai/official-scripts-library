# Get LinkedIn notifications

Automatically get LinkedIn notifications on linkedin.com. Reads the LinkedIn notifications tab and returns each item's text, link, relative time, and read/unread state. Supports filtering by the same sub-tabs LinkedIn shows (all, jobs, my posts, mentions) and paginates via "load more" up to a requested count.

- Site: linkedin.com
- Address: `reduck/linkedin.com/get_notifications`
- Updated: 2026-09-03 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/get_notifications`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_notifications
```

## Input

- `limit` (number, optional): Max number of notifications to return; will click "load more" as needed to reach it. Defaults to 20.
- `filter` (string, optional): Which notifications sub-tab to read. Defaults to "all".

## Output

- `filter` (string, required)
- `notifications` (array, required)

## FAQ

### What does "Get LinkedIn notifications" do?

Reads the LinkedIn notifications tab and returns each item's text, link, relative time, and read/unread state. Supports filtering by the same sub-tabs LinkedIn shows (all, jobs, my posts, mentions) and paginates via "load more" up to a requested count.

### How do I automatically get LinkedIn notifications on linkedin.com?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/get_notifications, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_notifications

### Is there a linkedin.com API to get LinkedIn notifications?

You do not need one. "Get LinkedIn notifications" drives the real linkedin.com pages in a browser, so it works whether or not linkedin.com offers an API for this.

### What information do I need to provide?

Optional: limit, filter.

### What does it return?

It returns filter, notifications.

### Do I need to be logged in to linkedin.com?

Yes. It acts as you on linkedin.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linkedin.com cookies saved by the Reduck extension.

### Does it change anything on linkedin.com, or only read data?

It only reads. It looks things up on linkedin.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/get_notifications, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_notifications

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/get_notifications
