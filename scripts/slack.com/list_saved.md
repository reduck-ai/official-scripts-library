# List Slack saved items

Automatically list Slack saved items on slack.com. List your Saved items (starred messages/files), newest first. One page per call (count/page). Returns each item's type, channel, message ts/text (resolved author) and date saved. Requires login.

- Site: slack.com
- Address: `reduck/slack.com/list_saved`
- Updated: 2026-07-10 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/slack.com/list_saved`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/slack.com/list_saved
```

## Input

- `page` (integer, optional): 1-based page (default 1).
- `count` (integer, optional): Items per page (default 50).
- `workspaceDomain` (string, optional): Workspace host, e.g. acme.slack.com. Defaults to the active workspace.

## Output

- `items` (array, required)

## FAQ

### What does "List Slack saved items" do?

List your Saved items (starred messages/files), newest first. One page per call (count/page). Returns each item's type, channel, message ts/text (resolved author) and date saved. Requires login.

### How do I automatically list Slack saved items on slack.com?

Ask an AI agent connected to Reduck to run reduck/slack.com/list_saved, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/list_saved

### Is there a slack.com API to list Slack saved items?

You do not need one. "List Slack saved items" drives the real slack.com pages in a browser, so it works whether or not slack.com offers an API for this.

### What information do I need to provide?

Optional: page, count, workspaceDomain.

### What does it return?

It returns items.

### Do I need to be logged in to slack.com?

Yes. It acts as you on slack.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the slack.com cookies saved by the Reduck extension.

### Does it change anything on slack.com, or only read data?

Unknown: its author has not declared whether it changes anything on slack.com, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/slack.com/list_saved, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/list_saved

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/slack.com/list_saved
