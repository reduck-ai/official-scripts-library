# List Descript invoices

Automatically list Descript invoices on web.descript.com. List Descript billing invoices for the signed-in drive. Returns id, number, date, total (in cents), currency, paid and receiptUrl (a Stripe receipt page linking to the invoice PDF) per invoice.

- Site: web.descript.com
- Address: `reduck/web.descript.com/list_invoices`
- Updated: 2026-08-20 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/web.descript.com/list_invoices`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/web.descript.com/list_invoices
```

## Input

- `limit` (integer, optional): Max invoices to list (page size).

## Output

- `count` (integer, required)
- `invoices` (array, required)

## FAQ

### What does "List Descript invoices" do?

List Descript billing invoices for the signed-in drive. Returns id, number, date, total (in cents), currency, paid and receiptUrl (a Stripe receipt page linking to the invoice PDF) per invoice.

### How do I automatically list Descript invoices on web.descript.com?

Ask an AI agent connected to Reduck to run reduck/web.descript.com/list_invoices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.descript.com/list_invoices

### Is there a web.descript.com API to list Descript invoices?

You do not need one. "List Descript invoices" drives the real web.descript.com pages in a browser, so it works whether or not web.descript.com offers an API for this.

### What information do I need to provide?

Optional: limit.

### What does it return?

It returns count, invoices.

### Do I need to be logged in to web.descript.com?

Yes. It acts as you on web.descript.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the web.descript.com cookies saved by the Reduck extension.

### Does it change anything on web.descript.com, or only read data?

It only reads. It looks things up on web.descript.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/web.descript.com/list_invoices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.descript.com/list_invoices

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/web.descript.com/list_invoices
