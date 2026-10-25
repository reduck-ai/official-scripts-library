# Reactivate a suspended Linear workspace member

Automatically reactivate a suspended Linear workspace member on linear.app. Reactivate a suspended member of a Linear workspace, identified by email. Undoes a suspension made with delete_user; a revoked invite cannot be reactivated and needs a new invite instead. Uses the currently active workspace unless workspaceUrl is given. Requires being signed in to Linear as a workspace admin.

- Site: linear.app
- Address: `reduck/linear.app/activate_user`
- Updated: 2026-10-23 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linear.app/activate_user`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linear.app/activate_user
```

## Input

- `email` (string, required): Email of the suspended member to reactivate.
- `workspaceUrl` (string, optional): Workspace URL slug (e.g. 'pointandtest'). Defaults to the active workspace.

## Output

- `email` (string, required)
- `action` (string, required)
- `username` (string, required)
- `workspaceUrl` (string, required)
- `status` (string | null, optional)

## FAQ

### What does "Reactivate a suspended Linear workspace member" do?

Reactivate a suspended member of a Linear workspace, identified by email. Undoes a suspension made with delete_user; a revoked invite cannot be reactivated and needs a new invite instead. Uses the currently active workspace unless workspaceUrl is given. Requires being signed in to Linear as a workspace admin.

### How do I automatically reactivate a suspended Linear workspace member on linear.app?

Ask an AI agent connected to Reduck to run reduck/linear.app/activate_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linear.app/activate_user

### Is there a linear.app API to reactivate a suspended Linear workspace member?

You do not need one. "Reactivate a suspended Linear workspace member" drives the real linear.app pages in a browser, so it works whether or not linear.app offers an API for this.

### What information do I need to provide?

Required: email. Optional: workspaceUrl.

### What does it return?

It returns email, action, status, username, workspaceUrl.

### Do I need to be logged in to linear.app?

Yes. It acts as you on linear.app: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linear.app cookies saved by the Reduck extension.

### Does it change anything on linear.app, or only read data?

It makes changes on linear.app, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linear.app/activate_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linear.app/activate_user

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linear.app/activate_user
