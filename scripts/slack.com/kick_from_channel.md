# Remove member from Slack channel

Automatically remove member from Slack channel on slack.com. Remove (kick) a member from a channel, by channel name/id and user @handle or id (U…). Requires login and permission. Returns the channel and removed user.

- Site: slack.com
- Address: `reduck/slack.com/kick_from_channel`
- Updated: 2026-08-14 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/slack.com/kick_from_channel`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/slack.com/kick_from_channel
```

## Input

- `user` (string, required): User @handle or id (U…) to remove.
- `channel` (string, required): Channel name/#name or id (C…).
- `workspaceDomain` (string, optional): Workspace host, e.g. acme.slack.com. Defaults to the active workspace.

## Output

- `ok` (boolean, required)
- `user` (string, required)
- `channel` (string, required)

## FAQ

### What does "Remove member from Slack channel" do?

Remove (kick) a member from a channel, by channel name/id and user @handle or id (U…). Requires login and permission. Returns the channel and removed user.

### How do I automatically remove member from Slack channel on slack.com?

Ask an AI agent connected to Reduck to run reduck/slack.com/kick_from_channel, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/kick_from_channel

### Is there a slack.com API to remove member from Slack channel?

You do not need one. "Remove member from Slack channel" drives the real slack.com pages in a browser, so it works whether or not slack.com offers an API for this.

### What information do I need to provide?

Required: channel, user. Optional: workspaceDomain.

### What does it return?

It returns ok, user, channel.

### Do I need to be logged in to slack.com?

Yes. It acts as you on slack.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the slack.com cookies saved by the Reduck extension.

### Does it change anything on slack.com, or only read data?

It makes changes on slack.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/slack.com/kick_from_channel, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/kick_from_channel

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/slack.com/kick_from_channel
