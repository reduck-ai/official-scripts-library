# Invite user to Slack workspace

Automatically invite user to Slack workspace on slack.com. Invite a new person into the workspace by email (workspace-level, not channel-level). New invites join as a Regular Member; use change_role afterward once they accept to promote to Admin/Owner. Requires login and workspace admin permission.

- Site: slack.com
- Address: `reduck/slack.com/create_user`
- Updated: 2026-08-14 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/slack.com/create_user`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/slack.com/create_user
```

## Input

- `email` (string, required): Email address to invite into the workspace.
- `workspaceDomain` (string, optional): Workspace host, e.g. acme.slack.com. Defaults to the active workspace.

## Output

- `ok` (boolean, required)
- `email` (string, required)
- `status` (string, required)
- `inviteId` (string | null, optional)
- `expirationTs` (number | null, optional)

## FAQ

### What does "Invite user to Slack workspace" do?

Invite a new person into the workspace by email (workspace-level, not channel-level). New invites join as a Regular Member; use change_role afterward once they accept to promote to Admin/Owner. Requires login and workspace admin permission.

### How do I automatically invite user to Slack workspace on slack.com?

Ask an AI agent connected to Reduck to run reduck/slack.com/create_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/create_user

### Is there a slack.com API to invite user to Slack workspace?

You do not need one. "Invite user to Slack workspace" drives the real slack.com pages in a browser, so it works whether or not slack.com offers an API for this.

### What information do I need to provide?

Required: email. Optional: workspaceDomain.

### What does it return?

It returns ok, email, status, inviteId, expirationTs.

### Do I need to be logged in to slack.com?

Yes. It acts as you on slack.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the slack.com cookies saved by the Reduck extension.

### Does it change anything on slack.com, or only read data?

It makes changes on slack.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/slack.com/create_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/create_user

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/slack.com/create_user
