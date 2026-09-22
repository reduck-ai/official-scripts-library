# List Slack channels

Automatically list Slack channels on slack.com. List the workspace's channels (public + private) with membership, member count, topic and purpose. One page per call; pass cursor to paginate and types/excludeArchived to filter. Requires login.

- Site: slack.com
- Address: `reduck/slack.com/list_channels`
- Updated: 2026-07-10 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/slack.com/list_channels`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/slack.com/list_channels
```

## Input

- `limit` (integer, optional): Max channels per page (default 200, Slack caps ~1000).
- `types` (string, optional): Comma-separated conversation types. Default 'public_channel,private_channel'.
- `cursor` (string, optional): next_cursor from a previous call to fetch the next page.
- `excludeArchived` (boolean, optional): Hide archived channels. Default true.
- `workspaceDomain` (string, optional): Workspace host to target, e.g. acme.slack.com. Defaults to the active workspace.

## Output

- `channels` (array, required)
- `workspace` (string, required)
- `nextCursor` (string | null, optional)

## FAQ

### What does "List Slack channels" do?

List the workspace's channels (public + private) with membership, member count, topic and purpose. One page per call; pass cursor to paginate and types/excludeArchived to filter. Requires login.

### How do I automatically list Slack channels on slack.com?

Ask an AI agent connected to Reduck to run reduck/slack.com/list_channels, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/list_channels

### Is there a slack.com API to list Slack channels?

You do not need one. "List Slack channels" drives the real slack.com pages in a browser, so it works whether or not slack.com offers an API for this.

### What information do I need to provide?

Optional: limit, types, cursor, excludeArchived, workspaceDomain.

### What does it return?

It returns channels, workspace, nextCursor.

### Do I need to be logged in to slack.com?

Yes. It acts as you on slack.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the slack.com cookies saved by the Reduck extension.

### Does it change anything on slack.com, or only read data?

Unknown: its author has not declared whether it changes anything on slack.com, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/slack.com/list_channels, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/list_channels

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/slack.com/list_channels
