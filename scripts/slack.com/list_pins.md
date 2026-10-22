# List Slack pinned items

Automatically list Slack pinned items on slack.com. List a Slack channel's pinned items by channel id (get it from List Slack channels). Returns each pin's message timestamp, author id and name, text and type; a pinned file has no message, so those fields are empty. A channel with no pins returns an empty list. Requires login.

- Site: slack.com
- Address: `reduck/slack.com/list_pins`
- Updated: 2026-10-21 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/slack.com/list_pins`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/slack.com/list_pins
```

## Input

- `channel` (string, required): Channel id (C… or G…). Get it from slack.com/list_channels.
- `workspaceDomain` (string, optional): Workspace host, e.g. acme.slack.com. Defaults to the active workspace.

## Output

- `pins` (array, required)
- `channel` (string, required)

## FAQ

### What does "List Slack pinned items" do?

List a Slack channel's pinned items by channel id (get it from List Slack channels). Returns each pin's message timestamp, author id and name, text and type; a pinned file has no message, so those fields are empty. A channel with no pins returns an empty list. Requires login.

### How do I automatically list Slack pinned items on slack.com?

Ask an AI agent connected to Reduck to run reduck/slack.com/list_pins, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/list_pins

### Is there a slack.com API to list Slack pinned items?

You do not need one. "List Slack pinned items" drives the real slack.com pages in a browser, so it works whether or not slack.com offers an API for this.

### What information do I need to provide?

Required: channel. Optional: workspaceDomain.

### What does it return?

It returns pins, channel.

### Do I need to be logged in to slack.com?

Yes. It acts as you on slack.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the slack.com cookies saved by the Reduck extension.

### Does it change anything on slack.com, or only read data?

It only reads. It looks things up on slack.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/slack.com/list_pins, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/list_pins

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/slack.com/list_pins
