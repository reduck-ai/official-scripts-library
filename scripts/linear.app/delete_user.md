# Remove/suspend a Linear workspace member

Remove a member's access to a Linear workspace, identified by email. A pending invite is revoked and an active member is suspended, since Linear has no hard delete; a member who is already suspended is reported as such, and activate_user undoes a suspension. Defaults to the currently active workspace; pass workspaceUrl to target another. Requires being signed in to Linear.

- Site: linear.app
- Address: `reduck/linear.app/delete_user`
- Updated: 2026-11-02 (v7)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linear.app/delete_user`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linear.app/delete_user
```

## Input

- `email` (string, required): Email of the member to remove.
- `workspaceUrl` (string, optional): Workspace URL slug (e.g. 'acme'). Defaults to the active workspace.

## Output

- `email` (string, required)
- `action` (string, required)
- `username` (string, required)
- `workspaceUrl` (string, required)
- `status` (string | null, optional)

## FAQ

### What does "Remove/suspend a Linear workspace member" do?

Remove a member's access to a Linear workspace, identified by email. A pending invite is revoked and an active member is suspended, since Linear has no hard delete; a member who is already suspended is reported as such, and activate_user undoes a suspension. Defaults to the currently active workspace; pass workspaceUrl to target another. Requires being signed in to Linear.

### What information do I need to provide?

Required: email. Optional: workspaceUrl.

### What does it return?

It returns email, action, status, username, workspaceUrl.

### Do I need to be logged in to linear.app?

Yes. It acts as you on linear.app: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linear.app cookies saved by the Reduck extension.

### Does it change anything on linear.app, or only read data?

It makes changes on linear.app, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linear.app/delete_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linear.app/delete_user

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linear.app/delete_user
