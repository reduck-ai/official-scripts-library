# Get Slack thread replies

Automatically get Slack thread replies on slack.com. Read every reply in a thread by channel (name or id) and the parent message ts (thread_ts). Returns the parent plus its replies, authors resolved to display names. Requires login.

- Site: slack.com
- Address: `reduck/slack.com/get_thread_replies`
- Updated: 2026-07-10 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/slack.com/get_thread_replies`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/slack.com/get_thread_replies
```

## Input

- `ts` (string, required): The parent message's ts / thread_ts.
- `channel` (string, required): Channel name (with or without #) or id (C…).
- `limit` (integer, optional): Max replies per page (default 100).
- `cursor` (string, optional): next_cursor from a previous call.
- `workspaceDomain` (string, optional): Workspace host, e.g. acme.slack.com. Defaults to the active workspace.

## Output

- `channel` (string, required)
- `replies` (array, required)
- `parent` (object | null, optional)
- `nextCursor` (string | null, optional)

## FAQ

### What does "Get Slack thread replies" do?

Read every reply in a thread by channel (name or id) and the parent message ts (thread_ts). Returns the parent plus its replies, authors resolved to display names. Requires login.

### How do I automatically get Slack thread replies on slack.com?

Ask an AI agent connected to Reduck to run reduck/slack.com/get_thread_replies, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/get_thread_replies

### Is there a slack.com API to get Slack thread replies?

You do not need one. "Get Slack thread replies" drives the real slack.com pages in a browser, so it works whether or not slack.com offers an API for this.

### What information do I need to provide?

Required: channel, ts. Optional: limit, cursor, workspaceDomain.

### What does it return?

It returns parent, channel, replies, nextCursor.

### Do I need to be logged in to slack.com?

Yes. It acts as you on slack.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the slack.com cookies saved by the Reduck extension.

### Does it change anything on slack.com, or only read data?

Unknown: its author has not declared whether it changes anything on slack.com, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/slack.com/get_thread_replies, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/get_thread_replies

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/slack.com/get_thread_replies
