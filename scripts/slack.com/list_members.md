# List Slack members

Automatically list Slack members on slack.com. List the members that Slack's member directory shows, with id, handle, real and display name, title, email and phone (when visible), status, avatar and guest flags, 50 per page. Admin, owner, bot, deleted and timezone are null when the directory does not give them. Pass cursor to read the next page. Requires login.

- Site: slack.com
- Address: `reduck/slack.com/list_members`
- Updated: 2026-11-16 (v6)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/slack.com/list_members`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/slack.com/list_members
```

## Input

- `workspaceDomain` (string, required): Workspace host, e.g. acme.slack.com, from slack.com/list_workspaces.
- `cursor` (string, optional): nextCursor from a previous call (a page number). Slack's member directory pages hold 50 members.

## Output

- `total` (integer | null, required)
- `members` (array, required)
- `workspace` (string, required)
- `nextCursor` (string | null, required)

## FAQ

### What does "List Slack members" do?

List the members that Slack's member directory shows, with id, handle, real and display name, title, email and phone (when visible), status, avatar and guest flags, 50 per page. Admin, owner, bot, deleted and timezone are null when the directory does not give them. Pass cursor to read the next page. Requires login.

### How do I automatically list Slack members on slack.com?

Ask an AI agent connected to Reduck to run reduck/slack.com/list_members, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/list_members

### Is there a slack.com API to list Slack members?

You do not need one. "List Slack members" drives the real slack.com pages in a browser, so it works whether or not slack.com offers an API for this.

### What information do I need to provide?

Required: workspaceDomain. Optional: cursor.

### What does it return?

It returns total, members, workspace, nextCursor.

### Do I need to be logged in to slack.com?

Yes. It acts as you on slack.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the slack.com cookies saved by the Reduck extension.

### Does it change anything on slack.com, or only read data?

It only reads. It looks things up on slack.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/slack.com/list_members, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/list_members

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/slack.com/list_members
