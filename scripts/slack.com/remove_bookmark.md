# Remove Slack channel bookmark

Automatically remove Slack channel bookmark on slack.com. Remove a bookmark from a channel's header by channel (name or id) and bookmark id (from list_bookmarks). Requires login.

- Site: slack.com
- Address: `reduck/slack.com/remove_bookmark`
- Updated: 2026-07-31 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/slack.com/remove_bookmark`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/slack.com/remove_bookmark
```

## Input

- `channel` (string, required): Channel name/#name or id (C…).
- `bookmarkId` (string, required): Bookmark id (Bk…) from list_bookmarks.
- `workspaceDomain` (string, optional): Workspace host, e.g. acme.slack.com. Defaults to the active workspace.

## Output

- `ok` (boolean, required)
- `channel` (string, optional)
- `bookmarkId` (string, optional)

## FAQ

### What does "Remove Slack channel bookmark" do?

Remove a bookmark from a channel's header by channel (name or id) and bookmark id (from list_bookmarks). Requires login.

### How do I automatically remove Slack channel bookmark on slack.com?

Ask an AI agent connected to Reduck to run reduck/slack.com/remove_bookmark, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/remove_bookmark

### Is there a slack.com API to remove Slack channel bookmark?

You do not need one. "Remove Slack channel bookmark" drives the real slack.com pages in a browser, so it works whether or not slack.com offers an API for this.

### What information do I need to provide?

Required: channel, bookmarkId. Optional: workspaceDomain.

### What does it return?

It returns ok, channel, bookmarkId.

### Do I need to be logged in to slack.com?

Yes. It acts as you on slack.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the slack.com cookies saved by the Reduck extension.

### Does it change anything on slack.com, or only read data?

It makes changes on slack.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/slack.com/remove_bookmark, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/remove_bookmark

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/slack.com/remove_bookmark
