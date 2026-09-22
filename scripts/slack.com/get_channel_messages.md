# Get Slack channel messages

Automatically get Slack channel messages on slack.com. Read a channel's message history by name (e.g. 'social' or '#social') or id (C…). Newest first; pass cursor to paginate, oldest/latest (unix ts) to bound the range. Authors are resolved to display names. Requires login.

- Site: slack.com
- Address: `reduck/slack.com/get_channel_messages`
- Updated: 2026-07-29 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/slack.com/get_channel_messages`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/slack.com/get_channel_messages
```

## Input

- `channel` (string, required): Channel name (with or without #) or id (C…).
- `limit` (integer, optional): Max messages per page (default 50).
- `cursor` (string, optional): next_cursor from a previous call.
- `latest` (string, optional): Only messages before this unix ts.
- `oldest` (string, optional): Only messages after this unix ts (inclusive).
- `workspaceDomain` (string, optional): Workspace host, e.g. acme.slack.com. Defaults to the active workspace.

## Output

- `channel` (string, required)
- `messages` (array, required)
- `nextCursor` (string | null, optional)

## FAQ

### What does "Get Slack channel messages" do?

Read a channel's message history by name (e.g. 'social' or '#social') or id (C…). Newest first; pass cursor to paginate, oldest/latest (unix ts) to bound the range. Authors are resolved to display names. Requires login.

### How do I automatically get Slack channel messages on slack.com?

Ask an AI agent connected to Reduck to run reduck/slack.com/get_channel_messages, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/get_channel_messages

### Is there a slack.com API to get Slack channel messages?

You do not need one. "Get Slack channel messages" drives the real slack.com pages in a browser, so it works whether or not slack.com offers an API for this.

### What information do I need to provide?

Required: channel. Optional: limit, cursor, latest, oldest, workspaceDomain.

### What does it return?

It returns channel, messages, nextCursor.

### Do I need to be logged in to slack.com?

Yes. It acts as you on slack.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the slack.com cookies saved by the Reduck extension.

### Does it change anything on slack.com, or only read data?

Unknown: its author has not declared whether it changes anything on slack.com, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/slack.com/get_channel_messages, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/get_channel_messages

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/slack.com/get_channel_messages
