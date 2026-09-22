# Invite user(s) to Linear workspace

Automatically invite user(s) to Linear workspace on linear.app. Invite one or more teammates to a Linear workspace by email via the Members settings 'Invite' dialog. Linear memberships are invite-based (not instant-create); everyone lands with the workspace's single default role since per-member role assignment is a Business-plan feature not exposed on Free-plan workspaces. Confirms the 'external domain' warning automatically when it appears. Defaults to the currently active workspace; pass workspaceUrl to target another. Requires login.

- Site: linear.app
- Address: `reduck/linear.app/create_user`
- Updated: 2026-08-27 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linear.app/create_user`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linear.app/create_user
```

## Input

- `emails` (array, required): Email addresses to invite.
- `workspaceUrl` (string, optional): Workspace URL slug (e.g. 'pointandtest'). Defaults to the active workspace.

## Output

- `invited` (array, required)
- `workspaceUrl` (string, required)

## Example output

Shape only: placeholder values generated from the output schema, not a real run.

```json
{
  "invited": [
    {}
  ],
  "workspaceUrl": "https://example.com/item/123"
}
```

## FAQ

### What does "Invite user(s) to Linear workspace" do?

Invite one or more teammates to a Linear workspace by email via the Members settings 'Invite' dialog. Linear memberships are invite-based (not instant-create); everyone lands with the workspace's single default role since per-member role assignment is a Business-plan feature not exposed on Free-plan workspaces. Confirms the 'external domain' warning automatically when it appears. Defaults to the currently active workspace; pass workspaceUrl to target another. Requires login.

### How do I automatically invite user(s) to Linear workspace on linear.app?

Ask an AI agent connected to Reduck to run reduck/linear.app/create_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linear.app/create_user

### Is there a linear.app API to invite user(s) to Linear workspace?

You do not need one. "Invite user(s) to Linear workspace" drives the real linear.app pages in a browser, so it works whether or not linear.app offers an API for this.

### What information do I need to provide?

Required: emails. Optional: workspaceUrl.

### What does it return?

It returns invited, workspaceUrl.

### Do I need to be logged in to linear.app?

Yes. It acts as you on linear.app: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linear.app cookies saved by the Reduck extension.

### Does it change anything on linear.app, or only read data?

It makes changes on linear.app, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linear.app/create_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linear.app/create_user

### Who maintains it?

It is part of Reduck's official curated catalogue.

### Is there a Linear API to invite teammates to a Linear workspace?

Not an official one you can use for this: it needs no Linear API key or OAuth app, only your signed-in browser. This script works as an unofficial Linear API for it: typed input, JSON output, callable from an AI agent over MCP, from the CLI, or over REST.

### How do I invite teammates to a Linear workspace programmatically?

Call this script with its arguments and read the JSON it returns. It drives Linear in a real browser session, so there is no API key to request and nothing to reverse-engineer yourself.

Source: https://reduck.ai/explore/scripts/reduck/linear.app/create_user
