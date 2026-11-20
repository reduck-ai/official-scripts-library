# Cloudflare: list members and roles

Automatically list members and roles on cloudflare.com. List members and their roles across the Cloudflare accounts visible to the signed-in user, one page at a time (50 accounts, 50 members per account). Returns, per account, its id, name and members (email, status, roles), plus hasMore when a next page exists.

- Site: cloudflare.com
- Address: `reduck/cloudflare.com/list_users_and_roles`
- Updated: 2026-11-19 (v6)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/cloudflare.com/list_users_and_roles`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/cloudflare.com/list_users_and_roles
```

## Input

- `page` (integer, optional): Page to read (1-based, 50 accounts and 50 members per account per page). Call again with page+1 while hasMore is true.

## Output

- `page` (integer, required)
- `hasMore` (boolean, required)
- `accounts` (array, required)

## FAQ

### What does "Cloudflare: list members and roles" do?

List members and their roles across the Cloudflare accounts visible to the signed-in user, one page at a time (50 accounts, 50 members per account). Returns, per account, its id, name and members (email, status, roles), plus hasMore when a next page exists.

### How do I automatically list members and roles on cloudflare.com?

Ask an AI agent connected to Reduck to run reduck/cloudflare.com/list_users_and_roles, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/cloudflare.com/list_users_and_roles

### Is there a cloudflare.com API to list members and roles?

You do not need one. "Cloudflare: list members and roles" drives the real cloudflare.com pages in a browser, so it works whether or not cloudflare.com offers an API for this.

### What information do I need to provide?

Optional: page.

### What does it return?

It returns page, hasMore, accounts.

### Do I need to be logged in to cloudflare.com?

Yes. It acts as you on cloudflare.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the cloudflare.com cookies saved by the Reduck extension.

### Does it change anything on cloudflare.com, or only read data?

Unknown: its author has not declared whether it changes anything on cloudflare.com, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/cloudflare.com/list_users_and_roles, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/cloudflare.com/list_users_and_roles

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/cloudflare.com/list_users_and_roles
