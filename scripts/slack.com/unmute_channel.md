# Unmute Slack channel

Automatically unmute Slack channel on slack.com. Unmute a Slack channel by id, choosing what it notifies about afterwards (all new posts or just mentions). Returns muted, and alreadyUnmuted when it was not muted. Requires login and the workspace host.

- Site: slack.com
- Address: `reduck/slack.com/unmute_channel`
- Updated: 2026-11-09 (v5)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/slack.com/unmute_channel`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/slack.com/unmute_channel
```

## Input

- `notify` (string, required): What the channel notifies about once unmuted: all new posts, or just mentions.
- `channel` (string, required): Channel id (C... or G...). Get it from slack.com/list_channels.
- `workspaceDomain` (string, required): Workspace host, e.g. acme.slack.com.

## Output

- `ok` (boolean, required)
- `muted` (boolean, required)
- `channel` (string, required)
- `notify` (string | null, optional)
- `alreadyUnmuted` (boolean, optional)

## FAQ

### What does "Unmute Slack channel" do?

Unmute a Slack channel by id, choosing what it notifies about afterwards (all new posts or just mentions). Returns muted, and alreadyUnmuted when it was not muted. Requires login and the workspace host.

### How do I automatically unmute Slack channel on slack.com?

Ask an AI agent connected to Reduck to run reduck/slack.com/unmute_channel, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/unmute_channel

### Is there a slack.com API to unmute Slack channel?

You do not need one. "Unmute Slack channel" drives the real slack.com pages in a browser, so it works whether or not slack.com offers an API for this.

### What information do I need to provide?

Required: channel, workspaceDomain, notify.

### What does it return?

It returns ok, muted, notify, channel, alreadyUnmuted.

### Do I need to be logged in to slack.com?

Yes. It acts as you on slack.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the slack.com cookies saved by the Reduck extension.

### Does it change anything on slack.com, or only read data?

It makes changes on slack.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/slack.com/unmute_channel, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/unmute_channel

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/slack.com/unmute_channel
