# Get current Linear user

Automatically get current Linear user on linear.app. Report which Linear account this browser is signed in as: name, email and the workspace slug. Optionally pass `workspaceUrl` to read a specific workspace; a workspace this account does not belong to fails with an error that says so. When the browser is signed out of Linear, the run fails with a signed-out error asking you to sign in to linear.app.

- Site: linear.app
- Address: `reduck/linear.app/get_current_user`
- Updated: 2026-10-22 (v6)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linear.app/get_current_user`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linear.app/get_current_user
```

## Input

- `workspaceUrl` (string, optional): Workspace slug (from its Linear URL). Defaults to whatever workspace the account lands on.

## Output

- `loggedIn` (boolean, required)
- `name` (string | null, optional)
- `email` (string | null, optional)
- `workspace` (string | null, optional): Workspace slug the profile page opened in

## FAQ

### What does "Get current Linear user" do?

Report which Linear account this browser is signed in as: name, email and the workspace slug. Optionally pass `workspaceUrl` to read a specific workspace; a workspace this account does not belong to fails with an error that says so. When the browser is signed out of Linear, the run fails with a signed-out error asking you to sign in to linear.app.

### How do I automatically get current Linear user on linear.app?

Ask an AI agent connected to Reduck to run reduck/linear.app/get_current_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linear.app/get_current_user

### Is there a linear.app API to get current Linear user?

You do not need one. "Get current Linear user" drives the real linear.app pages in a browser, so it works whether or not linear.app offers an API for this.

### What information do I need to provide?

Optional: workspaceUrl.

### What does it return?

It returns name, email, loggedIn, workspace.

### Do I need to be logged in to linear.app?

Yes. It acts as you on linear.app: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linear.app cookies saved by the Reduck extension.

### Does it change anything on linear.app, or only read data?

It only reads. It looks things up on linear.app and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linear.app/get_current_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linear.app/get_current_user

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linear.app/get_current_user
