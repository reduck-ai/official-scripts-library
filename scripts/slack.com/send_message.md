# Send Slack message

Automatically send Slack message on slack.com. Post a message to a channel or DM, identified by name ('social', '#social'), channel/DM id (C…/D…), or a user (@handle or U…) for a direct message. Pass threadTs to reply inside a thread (with broadcast to also send it to the channel). Returns the new message ts, channel id and permalink. Requires login.

- Site: slack.com
- Address: `reduck/slack.com/send_message`
- Updated: 2026-08-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/slack.com/send_message`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/slack.com/send_message
```

## Input

- `text` (string, required): Message text (supports Slack mrkdwn).
- `channel` (string, required): Target: channel name/#name, channel/DM id (C…/D…), @handle or user id (U…) for a DM.
- `threadTs` (string, optional): Parent message ts to reply in its thread.
- `broadcast` (boolean, optional): When replying in a thread, also post to the channel. Default false.
- `workspaceDomain` (string, optional): Workspace host, e.g. acme.slack.com. Defaults to the active workspace.

## Output

- `ok` (boolean, required)
- `ts` (string, required)
- `channel` (string, required)
- `permalink` (string | null, optional)

## FAQ

### What does "Send Slack message" do?

Post a message to a channel or DM, identified by name ('social', '#social'), channel/DM id (C…/D…), or a user (@handle or U…) for a direct message. Pass threadTs to reply inside a thread (with broadcast to also send it to the channel). Returns the new message ts, channel id and permalink. Requires login.

### How do I automatically send Slack message on slack.com?

Ask an AI agent connected to Reduck to run reduck/slack.com/send_message, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/send_message

### Is there a slack.com API to send Slack message?

You do not need one. "Send Slack message" drives the real slack.com pages in a browser, so it works whether or not slack.com offers an API for this.

### What information do I need to provide?

Required: channel, text. Optional: threadTs, broadcast, workspaceDomain.

### What does it return?

It returns ok, ts, channel, permalink.

### Do I need to be logged in to slack.com?

Yes. It acts as you on slack.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the slack.com cookies saved by the Reduck extension.

### Does it change anything on slack.com, or only read data?

It makes changes on slack.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/slack.com/send_message, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/send_message

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/slack.com/send_message
