# Change Slack workspace member's role

Automatically change Slack workspace member's role on slack.com. Change a workspace member's account type (owner/admin/member), identified by email. Requires login and workspace admin/owner permission. Returns the role before and after the change.

- Site: slack.com
- Address: `reduck/slack.com/change_role`
- Updated: 2026-08-14 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/slack.com/change_role`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/slack.com/change_role
```

## Input

- `role` (string, required): New account type: owner (Workspace Owner), admin (Workspace Admin), or member (Regular Member).
- `email` (string, required): Email of the member to change.
- `workspaceDomain` (string, optional): Workspace host, e.g. acme.slack.com. Defaults to the active workspace.

## Output

- `ok` (boolean, required)
- `email` (string, required)
- `userId` (string, required)
- `newRole` (string, required)
- `previousRole` (string, required)

## FAQ

### What does "Change Slack workspace member's role" do?

Change a workspace member's account type (owner/admin/member), identified by email. Requires login and workspace admin/owner permission. Returns the role before and after the change.

### How do I automatically change Slack workspace member's role on slack.com?

Ask an AI agent connected to Reduck to run reduck/slack.com/change_role, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/change_role

### Is there a slack.com API to change Slack workspace member's role?

You do not need one. "Change Slack workspace member's role" drives the real slack.com pages in a browser, so it works whether or not slack.com offers an API for this.

### What information do I need to provide?

Required: email, role. Optional: workspaceDomain.

### What does it return?

It returns ok, email, userId, newRole, previousRole.

### Do I need to be logged in to slack.com?

Yes. It acts as you on slack.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the slack.com cookies saved by the Reduck extension.

### Does it change anything on slack.com, or only read data?

It makes changes on slack.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/slack.com/change_role, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/change_role

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/slack.com/change_role
