# Delete Slack message

Automatically delete Slack message on slack.com. Delete one of your own messages by channel (name or id) and message ts. Returns the channel and ts deleted. Requires login.

- Site: slack.com
- Address: `reduck/slack.com/delete_message`
- Updated: 2026-11-24 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/slack.com/delete_message`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/slack.com/delete_message
```

## Input

- `ts` (string, required): The message's ts.
- `channel` (string, required): Channel or DM id (C…/D…/G…). Get it from slack.com/list_channels.
- `workspaceDomain` (string, required): Workspace host, e.g. acme.slack.com. Confirm with the user which workspace to target before running.

## Output

- `ok` (boolean, required)
- `ts` (string, required)
- `channel` (string, required)
- `workspace` (string, optional)

## FAQ

### What does "Delete Slack message" do?

Delete one of your own messages by channel (name or id) and message ts. Returns the channel and ts deleted. Requires login.

### How do I automatically delete Slack message on slack.com?

Ask an AI agent connected to Reduck to run reduck/slack.com/delete_message, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/delete_message

### Is there a slack.com API to delete Slack message?

You do not need one. "Delete Slack message" drives the real slack.com pages in a browser, so it works whether or not slack.com offers an API for this.

### What information do I need to provide?

Required: channel, ts, workspaceDomain.

### What does it return?

It returns ok, ts, channel, workspace.

### Do I need to be logged in to slack.com?

Yes. It acts as you on slack.com: in your browser it reuses your session, and on a cloud browser it loads your Auth session cookies for slack.com.

### Does it change anything on slack.com, or only read data?

It makes changes on slack.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/slack.com/delete_message, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/delete_message

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/slack.com/delete_message
