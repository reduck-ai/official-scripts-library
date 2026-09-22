# Vercel — list invoices

Automatically list invoices on vercel.com. List a Vercel team's billing invoices, newest first: billing period, status, total due, invoiced date, invoice id, a direct PDF download link, and a link to the invoice's detail page. Optionally pass a team URL slug; defaults to the account's own scope.

- Site: vercel.com
- Address: `reduck/vercel.com/list_invoices`
- Updated: 2026-08-20 (v6)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/vercel.com/list_invoices`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/vercel.com/list_invoices
```

## Input

- `team` (string, optional): Vercel team URL slug (e.g. acme-team). Optional -- defaults to the account's default team/scope (resolved from the dashboard redirect).

## Output

- `team` (string, required)
- `count` (integer, required)
- `invoices` (array, required)

## FAQ

### What does "Vercel — list invoices" do?

List a Vercel team's billing invoices, newest first: billing period, status, total due, invoiced date, invoice id, a direct PDF download link, and a link to the invoice's detail page. Optionally pass a team URL slug; defaults to the account's own scope.

### How do I automatically list invoices on vercel.com?

Ask an AI agent connected to Reduck to run reduck/vercel.com/list_invoices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/vercel.com/list_invoices

### Is there a vercel.com API to list invoices?

You do not need one. "Vercel — list invoices" drives the real vercel.com pages in a browser, so it works whether or not vercel.com offers an API for this.

### What information do I need to provide?

Optional: team.

### What does it return?

It returns team, count, invoices.

### Do I need to be logged in to vercel.com?

Yes. It acts as you on vercel.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the vercel.com cookies saved by the Reduck extension.

### Does it change anything on vercel.com, or only read data?

It only reads. It looks things up on vercel.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/vercel.com/list_invoices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/vercel.com/list_invoices

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/vercel.com/list_invoices
