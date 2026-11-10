# List Slack channel members

Automatically list Slack channel members on slack.com. List the members of a Slack channel by channel id (get it from List Slack channels), each with their id and display name, as Slack's member list shows them. Returns the first page Slack loads; nextCursor is set when Slack has more members than that page. Requires login and the workspace host.

- Site: slack.com
- Address: `reduck/slack.com/list_channel_members`
- Updated: 2026-11-09 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/slack.com/list_channel_members`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/slack.com/list_channel_members
```

## Input

- `channel` (string, required): Channel id (C… or G…). Get it from slack.com/list_channels.
- `workspaceDomain` (string, required): Workspace host, e.g. acme.slack.com.

## Output

- `channel` (string, required)
- `members` (array, required)
- `nextCursor` (string | null, optional)

## FAQ

### What does "List Slack channel members" do?

List the members of a Slack channel by channel id (get it from List Slack channels), each with their id and display name, as Slack's member list shows them. Returns the first page Slack loads; nextCursor is set when Slack has more members than that page. Requires login and the workspace host.

### How do I automatically list Slack channel members on slack.com?

Ask an AI agent connected to Reduck to run reduck/slack.com/list_channel_members, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/list_channel_members

### Is there a slack.com API to list Slack channel members?

You do not need one. "List Slack channel members" drives the real slack.com pages in a browser, so it works whether or not slack.com offers an API for this.

### What information do I need to provide?

Required: channel, workspaceDomain.

### What does it return?

It returns channel, members, nextCursor.

### Do I need to be logged in to slack.com?

Yes. It acts as you on slack.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the slack.com cookies saved by the Reduck extension.

### Does it change anything on slack.com, or only read data?

It only reads. It looks things up on slack.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/slack.com/list_channel_members, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/list_channel_members

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/slack.com/list_channel_members
