# Cloudflare: list invoices

Automatically list invoices on cloudflare.com. List Cloudflare invoices across every account visible to the signed-in user. Returns per account name, accountId, and invoices with date, type, number, amount, status. Accounts with no invoices come back with an empty invoices array rather than an error.

- Site: cloudflare.com
- Address: `reduck/cloudflare.com/list_invoices`
- Updated: 2026-08-21 (v5)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/cloudflare.com/list_invoices`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/cloudflare.com/list_invoices
```

## Input

It takes no input.

## Output

- `accounts` (array, required)

## FAQ

### What does "Cloudflare: list invoices" do?

List Cloudflare invoices across every account visible to the signed-in user. Returns per account name, accountId, and invoices with date, type, number, amount, status. Accounts with no invoices come back with an empty invoices array rather than an error.

### How do I automatically list invoices on cloudflare.com?

Ask an AI agent connected to Reduck to run reduck/cloudflare.com/list_invoices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/cloudflare.com/list_invoices

### Is there a cloudflare.com API to list invoices?

You do not need one. "Cloudflare: list invoices" drives the real cloudflare.com pages in a browser, so it works whether or not cloudflare.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

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
