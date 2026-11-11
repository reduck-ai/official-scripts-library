# List Lovable workspace members and roles

Automatically list Lovable workspace members and roles on lovable.dev. List the members of your current Lovable workspace with email, display name, role, invite and join times (joinedAt null while an invitation is pending) and project access. Acts on the workspace open in the browser. Page with offset and limit while hasMore is true.

- Site: lovable.dev
- Address: `reduck/lovable.dev/list-users-and-roles`
- Updated: 2026-11-10 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/lovable.dev/list-users-and-roles`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/lovable.dev/list-users-and-roles
```

## Input

- `limit` (integer, optional): Members per page.
- `offset` (integer, optional): 0-based offset; pass offset + limit for the next page.

## Output

- `total` (integer | null, required)
- `offset` (integer, required)
- `hasMore` (boolean, required)
- `members` (array, required)
- `workspaceId` (string, required)

## FAQ

### What does "List Lovable workspace members and roles" do?

List the members of your current Lovable workspace with email, display name, role, invite and join times (joinedAt null while an invitation is pending) and project access. Acts on the workspace open in the browser. Page with offset and limit while hasMore is true.

### How do I automatically list Lovable workspace members and roles on lovable.dev?

Ask an AI agent connected to Reduck to run reduck/lovable.dev/list-users-and-roles, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/lovable.dev/list-users-and-roles

### Is there a lovable.dev API to list Lovable workspace members and roles?

You do not need one. "List Lovable workspace members and roles" drives the real lovable.dev pages in a browser, so it works whether or not lovable.dev offers an API for this.

### What information do I need to provide?

Optional: limit, offset.

### What does it return?

It returns total, offset, hasMore, members, workspaceId.

### Do I need to be logged in to lovable.dev?

Yes. It acts as you on lovable.dev: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the lovable.dev cookies saved by the Reduck extension.

### Does it change anything on lovable.dev, or only read data?

It only reads. It looks things up on lovable.dev and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/lovable.dev/list-users-and-roles, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/lovable.dev/list-users-and-roles

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/lovable.dev/list-users-and-roles
