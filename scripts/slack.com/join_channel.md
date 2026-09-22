# Join Slack channel

Automatically join Slack channel on slack.com. Join a public channel (by name or id). Returns the channel id and name. Requires login.

- Site: slack.com
- Address: `reduck/slack.com/join_channel`
- Updated: 2026-07-31 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/slack.com/join_channel`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/slack.com/join_channel
```

## Input

- `channel` (string, required): Channel name/#name or id (C…).
- `workspaceDomain` (string, optional): Workspace host, e.g. acme.slack.com. Defaults to the active workspace.

## Output

- `ok` (boolean, required)
- `channel` (string, required)
- `name` (string | null, optional)

## FAQ

### What does "Join Slack channel" do?

Join a public channel (by name or id). Returns the channel id and name. Requires login.

### How do I automatically join Slack channel on slack.com?

Ask an AI agent connected to Reduck to run reduck/slack.com/join_channel, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/join_channel

### Is there a slack.com API to join Slack channel?

You do not need one. "Join Slack channel" drives the real slack.com pages in a browser, so it works whether or not slack.com offers an API for this.

### What information do I need to provide?

Required: channel. Optional: workspaceDomain.

### What does it return?

It returns ok, name, channel.

### Do I need to be logged in to slack.com?

Yes. It acts as you on slack.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the slack.com cookies saved by the Reduck extension.

### Does it change anything on slack.com, or only read data?

It makes changes on slack.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/slack.com/join_channel, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/join_channel

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/slack.com/join_channel
