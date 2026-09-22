# Get Slack mentions

Automatically get Slack mentions on slack.com. Read the Activity feed's Mentions tab — messages that @-mention you (direct, @channel/@everyone, user-group and keyword alerts). Newest first. Pass unreadOnly to restrict to unread. Item shape mirrors Slack's activity feed. Requires login.

- Site: slack.com
- Address: `reduck/slack.com/get_mentions`
- Updated: 2026-07-10 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/slack.com/get_mentions`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/slack.com/get_mentions
```

## Input

- `limit` (integer, optional): Max items (default 20).
- `unreadOnly` (boolean, optional): Only unread mentions. Default false.
- `workspaceDomain` (string, optional): Workspace host, e.g. acme.slack.com. Defaults to the active workspace.

## Output

- `count` (integer, required)
- `items` (array, required)
- `nextTs` (string | null, optional)
- `hasMore` (boolean, optional)

## FAQ

### What does "Get Slack mentions" do?

Read the Activity feed's Mentions tab — messages that @-mention you (direct, @channel/@everyone, user-group and keyword alerts). Newest first. Pass unreadOnly to restrict to unread. Item shape mirrors Slack's activity feed. Requires login.

### How do I automatically get Slack mentions on slack.com?

Ask an AI agent connected to Reduck to run reduck/slack.com/get_mentions, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/get_mentions

### Is there a slack.com API to get Slack mentions?

You do not need one. "Get Slack mentions" drives the real slack.com pages in a browser, so it works whether or not slack.com offers an API for this.

### What information do I need to provide?

Optional: limit, unreadOnly, workspaceDomain.

### What does it return?

It returns count, items, nextTs, hasMore.

### Do I need to be logged in to slack.com?

Yes. It acts as you on slack.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the slack.com cookies saved by the Reduck extension.

### Does it change anything on slack.com, or only read data?

Unknown: its author has not declared whether it changes anything on slack.com, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/slack.com/get_mentions, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/get_mentions

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/slack.com/get_mentions
