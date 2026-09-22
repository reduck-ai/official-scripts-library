# List Slack direct messages

Automatically list Slack direct messages on slack.com. List direct-message and group-DM conversations, with the counterpart's display name and (by default) the last message. One page per call; pass cursor to paginate. Requires login.

- Site: slack.com
- Address: `reduck/slack.com/list_dms`
- Updated: 2026-07-10 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/slack.com/list_dms`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/slack.com/list_dms
```

## Input

- `limit` (integer, optional): Max conversations per page (default 30).
- `cursor` (string, optional): next_cursor from a previous call.
- `includeLatest` (boolean, optional): Fetch each DM's last message (one extra call per DM). Default true.
- `workspaceDomain` (string, optional): Workspace host, e.g. acme.slack.com. Defaults to the active workspace.

## Output

- `dms` (array, required)
- `workspace` (string, required)
- `nextCursor` (string | null, optional)

## FAQ

### What does "List Slack direct messages" do?

List direct-message and group-DM conversations, with the counterpart's display name and (by default) the last message. One page per call; pass cursor to paginate. Requires login.

### How do I automatically list Slack direct messages on slack.com?

Ask an AI agent connected to Reduck to run reduck/slack.com/list_dms, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/list_dms

### Is there a slack.com API to list Slack direct messages?

You do not need one. "List Slack direct messages" drives the real slack.com pages in a browser, so it works whether or not slack.com offers an API for this.

### What information do I need to provide?

Optional: limit, cursor, includeLatest, workspaceDomain.

### What does it return?

It returns dms, workspace, nextCursor.

### Do I need to be logged in to slack.com?

Yes. It acts as you on slack.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the slack.com cookies saved by the Reduck extension.

### Does it change anything on slack.com, or only read data?

Unknown: its author has not declared whether it changes anything on slack.com, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/slack.com/list_dms, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/list_dms

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/slack.com/list_dms
