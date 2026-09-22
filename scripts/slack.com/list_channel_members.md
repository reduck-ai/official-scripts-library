# List Slack channel members

Automatically list Slack channel members on slack.com. List the members of a channel (by name or id), each resolved to id + display name. One page per call; pass cursor to paginate. Requires login.

- Site: slack.com
- Address: `reduck/slack.com/list_channel_members`
- Updated: 2026-07-10 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/slack.com/list_channel_members`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/slack.com/list_channel_members
```

## Input

- `channel` (string, required): Channel name/#name or id (C…).
- `limit` (integer, optional): Max members per page (default 200).
- `cursor` (string, optional): next_cursor from a previous call.
- `workspaceDomain` (string, optional): Workspace host, e.g. acme.slack.com. Defaults to the active workspace.

## Output

- `channel` (string, required)
- `members` (array, required)
- `nextCursor` (string | null, optional)

## FAQ

### What does "List Slack channel members" do?

List the members of a channel (by name or id), each resolved to id + display name. One page per call; pass cursor to paginate. Requires login.

### How do I automatically list Slack channel members on slack.com?

Ask an AI agent connected to Reduck to run reduck/slack.com/list_channel_members, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/list_channel_members

### Is there a slack.com API to list Slack channel members?

You do not need one. "List Slack channel members" drives the real slack.com pages in a browser, so it works whether or not slack.com offers an API for this.

### What information do I need to provide?

Required: channel. Optional: limit, cursor, workspaceDomain.

### What does it return?

It returns channel, members, nextCursor.

### Do I need to be logged in to slack.com?

Yes. It acts as you on slack.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the slack.com cookies saved by the Reduck extension.

### Does it change anything on slack.com, or only read data?

Unknown: its author has not declared whether it changes anything on slack.com, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/slack.com/list_channel_members, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/list_channel_members

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/slack.com/list_channel_members
