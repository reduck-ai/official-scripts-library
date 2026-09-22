# Set Slack channel purpose

Automatically set Slack channel purpose on slack.com. Set a channel's purpose/description by name or id. Pass an empty string to clear it. Returns the applied purpose. Requires login.

- Site: slack.com
- Address: `reduck/slack.com/set_channel_purpose`
- Updated: 2026-07-31 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/slack.com/set_channel_purpose`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/slack.com/set_channel_purpose
```

## Input

- `channel` (string, required): Channel name/#name or id (C…).
- `purpose` (string, required): New purpose text (empty clears).
- `workspaceDomain` (string, optional): Workspace host, e.g. acme.slack.com. Defaults to the active workspace.

## Output

- `ok` (boolean, required)
- `channel` (string, required)
- `purpose` (string | null, optional)

## FAQ

### What does "Set Slack channel purpose" do?

Set a channel's purpose/description by name or id. Pass an empty string to clear it. Returns the applied purpose. Requires login.

### How do I automatically set Slack channel purpose on slack.com?

Ask an AI agent connected to Reduck to run reduck/slack.com/set_channel_purpose, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/set_channel_purpose

### Is there a slack.com API to set Slack channel purpose?

You do not need one. "Set Slack channel purpose" drives the real slack.com pages in a browser, so it works whether or not slack.com offers an API for this.

### What information do I need to provide?

Required: channel, purpose. Optional: workspaceDomain.

### What does it return?

It returns ok, channel, purpose.

### Do I need to be logged in to slack.com?

Yes. It acts as you on slack.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the slack.com cookies saved by the Reduck extension.

### Does it change anything on slack.com, or only read data?

It makes changes on slack.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/slack.com/set_channel_purpose, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/set_channel_purpose

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/slack.com/set_channel_purpose
