# List Linear workspace members and roles

Automatically list Linear workspace members and roles on linear.app. List the workspace's members (name, username, email, role/status, teams, joined, last seen) from the Members settings page, including pending invites, suspended accounts, and app installs. Defaults to the currently active workspace; pass workspaceUrl to target another. Requires login.

- Site: linear.app
- Address: `reduck/linear.app/list_users_and_roles`
- Updated: 2026-09-07 (v17)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linear.app/list_users_and_roles`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linear.app/list_users_and_roles
```

## Input

- `workspaceUrl` (string, optional): Workspace URL slug (e.g. 'acme' from linear.app/acme/...). Defaults to the active workspace.

## Output

- `members` (array, required)
- `workspaceUrl` (string, required)

## FAQ

### What does "List Linear workspace members and roles" do?

List the workspace's members (name, username, email, role/status, teams, joined, last seen) from the Members settings page, including pending invites, suspended accounts, and app installs. Defaults to the currently active workspace; pass workspaceUrl to target another. Requires login.

### How do I automatically list Linear workspace members and roles on linear.app?

Ask an AI agent connected to Reduck to run reduck/linear.app/list_users_and_roles, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linear.app/list_users_and_roles

### Is there a linear.app API to list Linear workspace members and roles?

You do not need one. "List Linear workspace members and roles" drives the real linear.app pages in a browser, so it works whether or not linear.app offers an API for this.

### What information do I need to provide?

Optional: workspaceUrl.

### What does it return?

It returns members, workspaceUrl.

### Do I need to be logged in to linear.app?

Yes. It acts as you on linear.app: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linear.app cookies saved by the Reduck extension.

### Does it change anything on linear.app, or only read data?

It only reads. It looks things up on linear.app and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linear.app/list_users_and_roles, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linear.app/list_users_and_roles

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linear.app/list_users_and_roles
