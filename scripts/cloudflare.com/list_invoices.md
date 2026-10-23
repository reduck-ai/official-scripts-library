# List Cloudflare invoices

Automatically list Cloudflare invoices on cloudflare.com. List Cloudflare invoices across every account visible to the signed-in user, one page (50 entries) per account at a time. Returns per account its name, accountId, invoices (date, type, number, amount, status) and hasNextPage; pass page 2, 3… while an account has more. Accounts with no invoices come back with an empty list. A signed-out browser fails with a signed-out error asking to sign in at dash.cloudflare.com.

- Site: cloudflare.com
- Address: `reduck/cloudflare.com/list_invoices`
- Updated: 2026-10-22 (v7)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/cloudflare.com/list_invoices`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/cloudflare.com/list_invoices
```

## Input

- `page` (integer, optional): Page of each account's billing history (50 entries per page). Ask the next page while an account says hasNextPage.

## Output

- `accounts` (array, required)

## FAQ

### What does "List Cloudflare invoices" do?

List Cloudflare invoices across every account visible to the signed-in user, one page (50 entries) per account at a time. Returns per account its name, accountId, invoices (date, type, number, amount, status) and hasNextPage; pass page 2, 3… while an account has more. Accounts with no invoices come back with an empty list. A signed-out browser fails with a signed-out error asking to sign in at dash.cloudflare.com.

### How do I automatically list Cloudflare invoices on cloudflare.com?

Ask an AI agent connected to Reduck to run reduck/cloudflare.com/list_invoices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/cloudflare.com/list_invoices

### Is there a cloudflare.com API to list Cloudflare invoices?

You do not need one. "List Cloudflare invoices" drives the real cloudflare.com pages in a browser, so it works whether or not cloudflare.com offers an API for this.

### What information do I need to provide?

Optional: page.

### What does it return?

It returns accounts.

### Do I need to be logged in to cloudflare.com?

Yes. It acts as you on cloudflare.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the cloudflare.com cookies saved by the Reduck extension.

### Does it change anything on cloudflare.com, or only read data?

It only reads. It looks things up on cloudflare.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/cloudflare.com/list_invoices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/cloudflare.com/list_invoices

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/cloudflare.com/list_invoices
