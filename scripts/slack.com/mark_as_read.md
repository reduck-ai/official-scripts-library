# Mark Slack channel read

Automatically mark Slack channel read on slack.com. Mark a channel (by name or id) read up to a given message ts (defaults to the latest message). Clears the unread badge. Requires login.

- Site: slack.com
- Address: `reduck/slack.com/mark_as_read`
- Updated: 2026-07-31 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/slack.com/mark_as_read`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/slack.com/mark_as_read
```

## Input

- `channel` (string, required): Channel name/#name or id (C…).
- `ts` (string, optional): Mark read up to this ts. Defaults to the channel's latest message.
- `workspaceDomain` (string, optional): Workspace host, e.g. acme.slack.com. Defaults to the active workspace.

## Output

- `ok` (boolean, required)
- `ts` (string, required)
- `channel` (string, required)

## FAQ

### What does "Mark Slack channel read" do?

Mark a channel (by name or id) read up to a given message ts (defaults to the latest message). Clears the unread badge. Requires login.

### How do I automatically mark Slack channel read on slack.com?

Ask an AI agent connected to Reduck to run reduck/slack.com/mark_as_read, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/mark_as_read

### Is there a slack.com API to mark Slack channel read?

You do not need one. "Mark Slack channel read" drives the real slack.com pages in a browser, so it works whether or not slack.com offers an API for this.

### What information do I need to provide?

Required: channel. Optional: ts, workspaceDomain.

### What does it return?

It returns ok, ts, channel.

### Do I need to be logged in to slack.com?

Yes. It acts as you on slack.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the slack.com cookies saved by the Reduck extension.

### Does it change anything on slack.com, or only read data?

It makes changes on slack.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/slack.com/mark_as_read, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/mark_as_read

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/slack.com/mark_as_read
