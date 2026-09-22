# Unmute Slack channel

Automatically unmute Slack channel on slack.com. Unmute a channel (by name or id), re-enabling its notifications. Idempotent. Requires login.

- Site: slack.com
- Address: `reduck/slack.com/unmute_channel`
- Updated: 2026-07-31 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/slack.com/unmute_channel`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/slack.com/unmute_channel
```

## Input

- `channel` (string, required): Channel name/#name or id (C…).
- `workspaceDomain` (string, optional): Workspace host, e.g. acme.slack.com. Defaults to the active workspace.

## Output

- `ok` (boolean, required)
- `muted` (array, required)
- `channel` (string, required)

## FAQ

### What does "Unmute Slack channel" do?

Unmute a channel (by name or id), re-enabling its notifications. Idempotent. Requires login.

### How do I automatically unmute Slack channel on slack.com?

Ask an AI agent connected to Reduck to run reduck/slack.com/unmute_channel, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/unmute_channel

### Is there a slack.com API to unmute Slack channel?

You do not need one. "Unmute Slack channel" drives the real slack.com pages in a browser, so it works whether or not slack.com offers an API for this.

### What information do I need to provide?

Required: channel. Optional: workspaceDomain.

### What does it return?

It returns ok, muted, channel.

### Do I need to be logged in to slack.com?

Yes. It acts as you on slack.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the slack.com cookies saved by the Reduck extension.

### Does it change anything on slack.com, or only read data?

It makes changes on slack.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/slack.com/unmute_channel, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/unmute_channel

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/slack.com/unmute_channel
