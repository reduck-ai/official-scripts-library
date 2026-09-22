# Remove user from Slack workspace

Automatically remove user from Slack workspace on slack.com. Deactivate a member's account, removing them from the entire workspace (not just one channel), identified by email. Their messages/files remain but they can no longer sign in. Requires login and workspace admin/owner permission.

- Site: slack.com
- Address: `reduck/slack.com/delete_user`
- Updated: 2026-08-14 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/slack.com/delete_user`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/slack.com/delete_user
```

## Input

- `email` (string, required): Email of the member to remove/deactivate.
- `workspaceDomain` (string, optional): Workspace host, e.g. acme.slack.com. Defaults to the active workspace.

## Output

- `ok` (boolean, required)
- `email` (string, required)
- `userId` (string, required)
- `deactivated` (boolean, required)

## FAQ

### What does "Remove user from Slack workspace" do?

Deactivate a member's account, removing them from the entire workspace (not just one channel), identified by email. Their messages/files remain but they can no longer sign in. Requires login and workspace admin/owner permission.

### How do I automatically remove user from Slack workspace on slack.com?

Ask an AI agent connected to Reduck to run reduck/slack.com/delete_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/delete_user

### Is there a slack.com API to remove user from Slack workspace?

You do not need one. "Remove user from Slack workspace" drives the real slack.com pages in a browser, so it works whether or not slack.com offers an API for this.

### What information do I need to provide?

Required: email. Optional: workspaceDomain.

### What does it return?

It returns ok, email, userId, deactivated.

### Do I need to be logged in to slack.com?

Yes. It acts as you on slack.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the slack.com cookies saved by the Reduck extension.

### Does it change anything on slack.com, or only read data?

It makes changes on slack.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/slack.com/delete_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/delete_user

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/slack.com/delete_user
