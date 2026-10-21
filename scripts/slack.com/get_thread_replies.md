# Get Slack thread replies

Automatically get Slack thread replies on slack.com. Read a Slack thread by channel id (get it from slack.com/list_channels) and the parent message ts (thread_ts). Returns the parent plus one page of its replies, with authors' display names when Slack provides them, and nextCursor to pass for the next page (null on the last page). Reading does not mark the thread as read. Fails with a signed-out error when the browser is not signed in to Slack.

- Site: slack.com
- Address: `reduck/slack.com/get_thread_replies`
- Updated: 2026-10-20 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/slack.com/get_thread_replies`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/slack.com/get_thread_replies
```

## Input

- `channel` (string, required): Channel id (C…, G… or D…). Get it from slack.com/list_channels.
- `ts` (string, optional): The parent message's ts (same value as thread_ts). Pass this OR thread_ts.
- `limit` (integer, optional): Max messages per page (default 100).
- `cursor` (string, optional): nextCursor from a previous call.
- `thread_ts` (string, optional): Alias of ts: the parent message's thread_ts. Pass this OR ts.
- `workspaceDomain` (string, optional): Workspace host, e.g. acme.slack.com. Omit to use the workspace this browser last used.

## Output

- `channel` (string, required)
- `replies` (array, required)
- `parent` (object | null, optional)
- `nextCursor` (string | null, optional)

## FAQ

### What does "Get Slack thread replies" do?

Read a Slack thread by channel id (get it from slack.com/list_channels) and the parent message ts (thread_ts). Returns the parent plus one page of its replies, with authors' display names when Slack provides them, and nextCursor to pass for the next page (null on the last page). Reading does not mark the thread as read. Fails with a signed-out error when the browser is not signed in to Slack.

### How do I automatically get Slack thread replies on slack.com?

Ask an AI agent connected to Reduck to run reduck/slack.com/get_thread_replies, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/get_thread_replies

### Is there a slack.com API to get Slack thread replies?

You do not need one. "Get Slack thread replies" drives the real slack.com pages in a browser, so it works whether or not slack.com offers an API for this.

### What information do I need to provide?

Required: channel. Optional: ts, limit, cursor, thread_ts, workspaceDomain.

### What does it return?

It returns parent, channel, replies, nextCursor.

### Do I need to be logged in to slack.com?

Yes. It acts as you on slack.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the slack.com cookies saved by the Reduck extension.

### Does it change anything on slack.com, or only read data?

It only reads. It looks things up on slack.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/slack.com/get_thread_replies, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/get_thread_replies

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/slack.com/get_thread_replies
