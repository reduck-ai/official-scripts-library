# Edit Slack message

Automatically edit Slack message on slack.com. Edit one of your own messages, given the channel (name '#social' or id C…/D…) and the message ts. Pass the new text (supports Slack mrkdwn). Defaults to the active workspace; pass workspaceDomain (e.g. acme.slack.com) to target another. Confirm the target workspace with the user before running. Returns the edited ts, channel id and new text. Requires login.

- Site: slack.com
- Address: `reduck/slack.com/edit_message`
- Updated: 2026-09-01 (v5)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/slack.com/edit_message`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/slack.com/edit_message
```

## Input

- `ts` (string, required): ts of the message to edit (must be your own message).
- `text` (string, required): New message text (supports Slack mrkdwn, including <url|label> links). Replaces the whole message.
- `channel` (string, required): Target: channel name/#name, or channel/DM id (C…/D…/G…).
- `workspaceDomain` (string, optional): Workspace host, e.g. acme.slack.com. Defaults to the active workspace. Confirm with the user which workspace to target before running this script.

## Output

- `ok` (boolean, required)
- `ts` (string, required)
- `text` (string, required)
- `channel` (string, required)
- `workspace` (string, optional)

## FAQ

### What does "Edit Slack message" do?

Edit one of your own messages, given the channel (name '#social' or id C…/D…) and the message ts. Pass the new text (supports Slack mrkdwn). Defaults to the active workspace; pass workspaceDomain (e.g. acme.slack.com) to target another. Confirm the target workspace with the user before running. Returns the edited ts, channel id and new text. Requires login.

### How do I automatically edit Slack message on slack.com?

Ask an AI agent connected to Reduck to run reduck/slack.com/edit_message, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/edit_message

### Is there a slack.com API to edit Slack message?

You do not need one. "Edit Slack message" drives the real slack.com pages in a browser, so it works whether or not slack.com offers an API for this.

### What information do I need to provide?

Required: channel, ts, text. Optional: workspaceDomain.

### What does it return?

It returns ok, ts, text, channel, workspace.

### Do I need to be logged in to slack.com?

Yes. It acts as you on slack.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the slack.com cookies saved by the Reduck extension.

### Does it change anything on slack.com, or only read data?

It makes changes on slack.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/slack.com/edit_message, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/edit_message

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/slack.com/edit_message
