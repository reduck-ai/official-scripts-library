# List Slack channel bookmarks

Automatically list Slack channel bookmarks on slack.com. List a channel's bookmarks (the links pinned to its header) by channel name or id. Returns each bookmark's id, title, link and type. Requires login.

- Site: slack.com
- Address: `reduck/slack.com/list_bookmarks`
- Updated: 2026-07-10 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/slack.com/list_bookmarks`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/slack.com/list_bookmarks
```

## Input

- `channel` (string, required): Channel name/#name or id (C…).
- `workspaceDomain` (string, optional): Workspace host, e.g. acme.slack.com. Defaults to the active workspace.

## Output

- `channel` (string, required)
- `bookmarks` (array, required)

## FAQ

### What does "List Slack channel bookmarks" do?

List a channel's bookmarks (the links pinned to its header) by channel name or id. Returns each bookmark's id, title, link and type. Requires login.

### How do I automatically list Slack channel bookmarks on slack.com?

Ask an AI agent connected to Reduck to run reduck/slack.com/list_bookmarks, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/list_bookmarks

### Is there a slack.com API to list Slack channel bookmarks?

You do not need one. "List Slack channel bookmarks" drives the real slack.com pages in a browser, so it works whether or not slack.com offers an API for this.

### What information do I need to provide?

Required: channel. Optional: workspaceDomain.

### What does it return?

It returns channel, bookmarks.

### Do I need to be logged in to slack.com?

Yes. It acts as you on slack.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the slack.com cookies saved by the Reduck extension.

### Does it change anything on slack.com, or only read data?

Unknown: its author has not declared whether it changes anything on slack.com, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/slack.com/list_bookmarks, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/list_bookmarks

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/slack.com/list_bookmarks
