# Get Slack mentions

Automatically get Slack mentions on slack.com. Read the Activity feed's Mentions tab — messages that @-mention you (direct, @channel/@everyone, user-group and keyword alerts). Newest first. Pass unreadOnly to restrict to unread. Item shape mirrors Slack's activity feed. Requires login.

- Site: slack.com
- Address: `reduck/slack.com/get_mentions`
- Updated: 2026-11-24 (v8)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/slack.com/get_mentions`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/slack.com/get_mentions
```

## Input

- `workspaceDomain` (string, required): Workspace host, e.g. acme.slack.com.
- `limit` (integer, optional): Items per page.
- `cursor` (string, optional): nextCursor from the previous page, to read the next one.
- `unreadOnly` (boolean, optional): Only unread mentions.

## Output

- `count` (integer, required)
- `items` (array, required)
- `hasMore` (boolean, optional)
- `nextCursor` (string | null, optional)

## FAQ

### What does "Get Slack mentions" do?

Read the Activity feed's Mentions tab — messages that @-mention you (direct, @channel/@everyone, user-group and keyword alerts). Newest first. Pass unreadOnly to restrict to unread. Item shape mirrors Slack's activity feed. Requires login.

### How do I automatically get Slack mentions on slack.com?

Ask an AI agent connected to Reduck to run reduck/slack.com/get_mentions, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/get_mentions

### Is there a slack.com API to get Slack mentions?

You do not need one. "Get Slack mentions" drives the real slack.com pages in a browser, so it works whether or not slack.com offers an API for this.

### What information do I need to provide?

Required: workspaceDomain. Optional: limit, cursor, unreadOnly.

### What does it return?

It returns count, items, hasMore, nextCursor.

### Do I need to be logged in to slack.com?

Yes. It acts as you on slack.com: in your browser it reuses your session, and on a cloud browser it loads your Auth session cookies for slack.com.

### Does it change anything on slack.com, or only read data?

It only reads. It looks things up on slack.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/slack.com/get_mentions, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/get_mentions

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/slack.com/get_mentions
