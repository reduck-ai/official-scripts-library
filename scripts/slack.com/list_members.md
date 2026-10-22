# List Slack members

Automatically list Slack members on slack.com. List a Slack workspace's members with id, handle, real and display name, title, email (when visible), timezone, status and admin, owner, bot and guest flags. Deactivated accounts are included and flagged as deleted. One page per call; pass the returned cursor to read the next page. Requires login.

- Site: slack.com
- Address: `reduck/slack.com/list_members`
- Updated: 2026-10-21 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/slack.com/list_members`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/slack.com/list_members
```

## Input

- `limit` (integer, optional): Max members per page (default 200).
- `cursor` (string, optional): nextCursor from a previous call.
- `workspaceDomain` (string, optional): Workspace host, e.g. acme.slack.com. Defaults to the active workspace.

## Output

- `members` (array, required)
- `workspace` (string, required)
- `nextCursor` (string | null, optional)

## FAQ

### What does "List Slack members" do?

List a Slack workspace's members with id, handle, real and display name, title, email (when visible), timezone, status and admin, owner, bot and guest flags. Deactivated accounts are included and flagged as deleted. One page per call; pass the returned cursor to read the next page. Requires login.

### How do I automatically list Slack members on slack.com?

Ask an AI agent connected to Reduck to run reduck/slack.com/list_members, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/list_members

### Is there a slack.com API to list Slack members?

You do not need one. "List Slack members" drives the real slack.com pages in a browser, so it works whether or not slack.com offers an API for this.

### What information do I need to provide?

Optional: limit, cursor, workspaceDomain.

### What does it return?

It returns members, workspace, nextCursor.

### Do I need to be logged in to slack.com?

Yes. It acts as you on slack.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the slack.com cookies saved by the Reduck extension.

### Does it change anything on slack.com, or only read data?

It only reads. It looks things up on slack.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/slack.com/list_members, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/list_members

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/slack.com/list_members
