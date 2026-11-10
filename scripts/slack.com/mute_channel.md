# Mute Slack channel

Automatically mute Slack channel on slack.com. Mute a Slack channel by id so it stops notifying and greys out in the sidebar. Returns muted, and alreadyMuted when it was muted before. Requires login and the workspace host.

- Site: slack.com
- Address: `reduck/slack.com/mute_channel`
- Updated: 2026-11-09 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/slack.com/mute_channel`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/slack.com/mute_channel
```

## Input

- `channel` (string, required): Channel id (C… or G…). Get it from slack.com/list_channels.
- `workspaceDomain` (string, required): Workspace host, e.g. acme.slack.com.

## Output

- `ok` (boolean, required)
- `muted` (boolean, required)
- `channel` (string, required)
- `alreadyMuted` (boolean, optional)

## FAQ

### What does "Mute Slack channel" do?

Mute a Slack channel by id so it stops notifying and greys out in the sidebar. Returns muted, and alreadyMuted when it was muted before. Requires login and the workspace host.

### How do I automatically mute Slack channel on slack.com?

Ask an AI agent connected to Reduck to run reduck/slack.com/mute_channel, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/mute_channel

### Is there a slack.com API to mute Slack channel?

You do not need one. "Mute Slack channel" drives the real slack.com pages in a browser, so it works whether or not slack.com offers an API for this.

### What information do I need to provide?

Required: channel, workspaceDomain.

### What does it return?

It returns ok, muted, channel, alreadyMuted.

### Do I need to be logged in to slack.com?

Yes. It acts as you on slack.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the slack.com cookies saved by the Reduck extension.

### Does it change anything on slack.com, or only read data?

It makes changes on slack.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/slack.com/mute_channel, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/mute_channel

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/slack.com/mute_channel
