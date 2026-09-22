# Edit Slack message

Automatically edit Slack message on slack.com. Edit one of your own messages by channel (name or id) and message ts, replacing its text. Returns the channel, ts and new text. Requires login.

- Site: slack.com
- Address: `reduck/slack.com/update_message`
- Updated: 2026-07-31 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/slack.com/update_message`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/slack.com/update_message
```

## Input

- `ts` (string, required): The message's ts.
- `text` (string, required): New message text.
- `channel` (string, required): Channel name/#name or id (C…/D…).
- `workspaceDomain` (string, optional): Workspace host. Defaults to the active workspace.

## Output

- `ok` (boolean, required)
- `ts` (string, required)
- `channel` (string, required)
- `text` (string | null, optional)

## FAQ

### What does "Edit Slack message" do?

Edit one of your own messages by channel (name or id) and message ts, replacing its text. Returns the channel, ts and new text. Requires login.

### How do I automatically edit Slack message on slack.com?

Ask an AI agent connected to Reduck to run reduck/slack.com/update_message, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/update_message

### Is there a slack.com API to edit Slack message?

You do not need one. "Edit Slack message" drives the real slack.com pages in a browser, so it works whether or not slack.com offers an API for this.

### What information do I need to provide?

Required: channel, ts, text. Optional: workspaceDomain.

### What does it return?

It returns ok, ts, text, channel.

### Do I need to be logged in to slack.com?

Yes. It acts as you on slack.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the slack.com cookies saved by the Reduck extension.

### Does it change anything on slack.com, or only read data?

It makes changes on slack.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/slack.com/update_message, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/update_message

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/slack.com/update_message
