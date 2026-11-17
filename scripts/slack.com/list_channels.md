# List Slack channels

Automatically list Slack channels on slack.com. List the channels that Slack's channel browser shows (archived channels excluded), with id, name, member count, purpose and whether you are a member, 50 per page. Pass cursor to read the next page. Requires login.

- Site: slack.com
- Address: `reduck/slack.com/list_channels`
- Updated: 2026-11-16 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/slack.com/list_channels`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/slack.com/list_channels
```

## Input

- `workspaceDomain` (string, required): Workspace host, e.g. acme.slack.com, from slack.com/list_workspaces.
- `cursor` (string, optional): nextCursor from a previous call (a page number). Slack's channel browser pages hold 50 channels.

## Output

- `total` (integer | null, required)
- `channels` (array, required)
- `workspace` (string, required)
- `nextCursor` (string | null, required)

## FAQ

### What does "List Slack channels" do?

List the channels that Slack's channel browser shows (archived channels excluded), with id, name, member count, purpose and whether you are a member, 50 per page. Pass cursor to read the next page. Requires login.

### How do I automatically list Slack channels on slack.com?

Ask an AI agent connected to Reduck to run reduck/slack.com/list_channels, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/list_channels

### Is there a slack.com API to list Slack channels?

You do not need one. "List Slack channels" drives the real slack.com pages in a browser, so it works whether or not slack.com offers an API for this.

### What information do I need to provide?

Required: workspaceDomain. Optional: cursor.

### What does it return?

It returns total, channels, workspace, nextCursor.

### Do I need to be logged in to slack.com?

Yes. It acts as you on slack.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the slack.com cookies saved by the Reduck extension.

### Does it change anything on slack.com, or only read data?

It only reads. It looks things up on slack.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/slack.com/list_channels, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/list_channels

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/slack.com/list_channels
