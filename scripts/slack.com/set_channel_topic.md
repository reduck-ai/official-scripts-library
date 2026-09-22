# Set Slack channel topic

Automatically set Slack channel topic on slack.com. Set a channel's topic (the short line shown in the header) by name or id. Topics are limited to 250 characters, and a longer one is refused up front rather than part-way through. Pass an empty string to clear the topic. Returns the applied topic. Requires login.

- Site: slack.com
- Address: `reduck/slack.com/set_channel_topic`
- Updated: 2026-08-10 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/slack.com/set_channel_topic`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/slack.com/set_channel_topic
```

## Input

- `topic` (string, required): New topic text, up to 250 characters (empty clears).
- `channel` (string, required): Channel name/#name or id (C…).
- `workspaceDomain` (string, optional): Workspace host, e.g. acme.slack.com. Defaults to the active workspace.

## Output

- `ok` (boolean, required)
- `channel` (string, required)
- `topic` (string | null, optional)

## FAQ

### What does "Set Slack channel topic" do?

Set a channel's topic (the short line shown in the header) by name or id. Topics are limited to 250 characters, and a longer one is refused up front rather than part-way through. Pass an empty string to clear the topic. Returns the applied topic. Requires login.

### How do I automatically set Slack channel topic on slack.com?

Ask an AI agent connected to Reduck to run reduck/slack.com/set_channel_topic, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/set_channel_topic

### Is there a slack.com API to set Slack channel topic?

You do not need one. "Set Slack channel topic" drives the real slack.com pages in a browser, so it works whether or not slack.com offers an API for this.

### What information do I need to provide?

Required: channel, topic. Optional: workspaceDomain.

### What does it return?

It returns ok, topic, channel.

### Do I need to be logged in to slack.com?

Yes. It acts as you on slack.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the slack.com cookies saved by the Reduck extension.

### Does it change anything on slack.com, or only read data?

It makes changes on slack.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/slack.com/set_channel_topic, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/set_channel_topic

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/slack.com/set_channel_topic
