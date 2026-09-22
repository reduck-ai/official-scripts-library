# Search Slack messages

Automatically search Slack messages on slack.com. Full-text search across the workspace's messages, supporting Slack's modifiers (from:@user, in:#channel, before:/after:date, "exact phrase"). One page per call. Requires login.

- Site: slack.com
- Address: `reduck/slack.com/search_messages`
- Updated: 2026-08-21 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/slack.com/search_messages`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/slack.com/search_messages
```

## Input

- `query` (string, required): Search query, incl. Slack modifiers like from:@alice in:#general after:2026-01-01.
- `page` (integer, optional): 1-based page number (default 1).
- `sort` (string, optional): 'timestamp' (default) or 'score' (relevance).
- `count` (integer, optional): Results per page (default 20).
- `sortDir` (string, optional): 'desc' (default) or 'asc'.
- `workspaceDomain` (string, optional): Workspace host, e.g. acme.slack.com. Defaults to the active workspace.

## Output

- `query` (string, required)
- `total` (integer, required)
- `matches` (array, required)
- `page` (integer, optional)
- `pageCount` (integer | null, optional)

## FAQ

### What does "Search Slack messages" do?

Full-text search across the workspace's messages, supporting Slack's modifiers (from:@user, in:#channel, before:/after:date, "exact phrase"). One page per call. Requires login.

### How do I automatically search Slack messages on slack.com?

Ask an AI agent connected to Reduck to run reduck/slack.com/search_messages, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/search_messages

### Is there a slack.com API to search Slack messages?

You do not need one. "Search Slack messages" drives the real slack.com pages in a browser, so it works whether or not slack.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: page, sort, count, sortDir, workspaceDomain.

### What does it return?

It returns page, query, total, matches, pageCount.

### Do I need to be logged in to slack.com?

Yes. It acts as you on slack.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the slack.com cookies saved by the Reduck extension.

### Does it change anything on slack.com, or only read data?

It only reads. It looks things up on slack.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/slack.com/search_messages, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/search_messages

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/slack.com/search_messages
