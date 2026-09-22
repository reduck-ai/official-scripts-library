# List Lovable workspace members and roles

Automatically list Lovable workspace members and roles on lovable.dev. List members of your current default Lovable workspace (Settings > People), with email, display name, role (owner/admin/member/viewer), invited/joined status. No scoping arg — operates on whichever workspace is currently active in your browser. Returns the workspace id, total count, hasMore flag (true if more than the first page of ~25 members exist), and the member list.

- Site: lovable.dev
- Address: `reduck/lovable.dev/list-users-and-roles`
- Updated: 2026-08-19 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/lovable.dev/list-users-and-roles`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/lovable.dev/list-users-and-roles
```

## Input

It takes no input.

## Output

- `total` (number, required)
- `hasMore` (boolean, required)
- `members` (array, required)
- `workspaceId` (string, required)

## FAQ

### What does "List Lovable workspace members and roles" do?

List members of your current default Lovable workspace (Settings > People), with email, display name, role (owner/admin/member/viewer), invited/joined status. No scoping arg — operates on whichever workspace is currently active in your browser. Returns the workspace id, total count, hasMore flag (true if more than the first page of ~25 members exist), and the member list.

### How do I automatically list Lovable workspace members and roles on lovable.dev?

Ask an AI agent connected to Reduck to run reduck/lovable.dev/list-users-and-roles, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/lovable.dev/list-users-and-roles

### Is there a lovable.dev API to list Lovable workspace members and roles?

You do not need one. "List Lovable workspace members and roles" drives the real lovable.dev pages in a browser, so it works whether or not lovable.dev offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns total, hasMore, members, workspaceId.

### Do I need to be logged in to lovable.dev?

Yes. It acts as you on lovable.dev: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the lovable.dev cookies saved by the Reduck extension.

### Does it change anything on lovable.dev, or only read data?

Unknown: its author has not declared whether it changes anything on lovable.dev, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/lovable.dev/list-users-and-roles, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/lovable.dev/list-users-and-roles

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/lovable.dev/list-users-and-roles
