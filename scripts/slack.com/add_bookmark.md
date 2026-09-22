# Add Slack channel bookmark

Automatically add Slack channel bookmark on slack.com. Add a link bookmark to a channel's header by channel name or id. Returns the new bookmark's id. Requires login.

- Site: slack.com
- Address: `reduck/slack.com/add_bookmark`
- Updated: 2026-07-31 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/slack.com/add_bookmark`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/slack.com/add_bookmark
```

## Input

- `link` (string, required): URL to bookmark.
- `title` (string, required): Bookmark label.
- `channel` (string, required): Channel name/#name or id (C…).
- `emoji` (string, optional): Optional emoji with colons, e.g. ':link:'.
- `workspaceDomain` (string, optional): Workspace host, e.g. acme.slack.com. Defaults to the active workspace.

## Output

- `id` (string, required)
- `ok` (boolean, required)
- `channel` (string, optional)

## FAQ

### What does "Add Slack channel bookmark" do?

Add a link bookmark to a channel's header by channel name or id. Returns the new bookmark's id. Requires login.

### How do I automatically add Slack channel bookmark on slack.com?

Ask an AI agent connected to Reduck to run reduck/slack.com/add_bookmark, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/add_bookmark

### Is there a slack.com API to add Slack channel bookmark?

You do not need one. "Add Slack channel bookmark" drives the real slack.com pages in a browser, so it works whether or not slack.com offers an API for this.

### What information do I need to provide?

Required: channel, title, link. Optional: emoji, workspaceDomain.

### What does it return?

It returns id, ok, channel.

### Do I need to be logged in to slack.com?

Yes. It acts as you on slack.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the slack.com cookies saved by the Reduck extension.

### Does it change anything on slack.com, or only read data?

It makes changes on slack.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/slack.com/add_bookmark, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/add_bookmark

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/slack.com/add_bookmark
