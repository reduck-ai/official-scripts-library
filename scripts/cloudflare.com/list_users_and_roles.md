# Cloudflare: list members and roles

Automatically list members and roles on cloudflare.com. List members and their roles across every Cloudflare account visible to the signed-in user (matches the existing list_invoices convention: no account scoping arg). Reads the dashboard's own accounts and members JSON APIs rather than scraping the DOM. Returns per account id/name and its members (email, status, roles).

- Site: cloudflare.com
- Address: `reduck/cloudflare.com/list_users_and_roles`
- Updated: 2026-07-27 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/cloudflare.com/list_users_and_roles`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/cloudflare.com/list_users_and_roles
```

## Input

It takes no input.

## Output

- `accounts` (array, required)

## FAQ

### What does "Cloudflare: list members and roles" do?

List members and their roles across every Cloudflare account visible to the signed-in user (matches the existing list_invoices convention: no account scoping arg). Reads the dashboard's own accounts and members JSON APIs rather than scraping the DOM. Returns per account id/name and its members (email, status, roles).

### How do I automatically list members and roles on cloudflare.com?

Ask an AI agent connected to Reduck to run reduck/cloudflare.com/list_users_and_roles, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/cloudflare.com/list_users_and_roles

### Is there a cloudflare.com API to list members and roles?

You do not need one. "Cloudflare: list members and roles" drives the real cloudflare.com pages in a browser, so it works whether or not cloudflare.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns accounts.

### Do I need to be logged in to cloudflare.com?

Yes. It acts as you on cloudflare.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the cloudflare.com cookies saved by the Reduck extension.

### Does it change anything on cloudflare.com, or only read data?

Unknown: its author has not declared whether it changes anything on cloudflare.com, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/cloudflare.com/list_users_and_roles, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/cloudflare.com/list_users_and_roles

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/cloudflare.com/list_users_and_roles
