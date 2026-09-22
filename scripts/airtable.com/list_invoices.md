# List Airtable invoices

Automatically list Airtable invoices on airtable.com. List Airtable workspace billing invoices across every workspace you have billing access to. Each invoice resolves to its Stripe hosted invoice URL (download via invoice.stripe.com/download_invoice_pdf). Returns total plus invoices (workspace, date, amount, status, hosted_invoice_url). Billing is per-workspace and only the workspace billing owner sees the Billing tab; workspaces without paid history return no invoices.

- Site: airtable.com
- Address: `reduck/airtable.com/list_invoices`
- Updated: 2026-08-20 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/airtable.com/list_invoices`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/airtable.com/list_invoices
```

## Input

It takes no input.

## Output

- `total` (integer, required)
- `invoices` (array, required)

## FAQ

### What does "List Airtable invoices" do?

List Airtable workspace billing invoices across every workspace you have billing access to. Each invoice resolves to its Stripe hosted invoice URL (download via invoice.stripe.com/download_invoice_pdf). Returns total plus invoices (workspace, date, amount, status, hosted_invoice_url). Billing is per-workspace and only the workspace billing owner sees the Billing tab; workspaces without paid history return no invoices.

### How do I automatically list Airtable invoices on airtable.com?

Ask an AI agent connected to Reduck to run reduck/airtable.com/list_invoices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/airtable.com/list_invoices

### Is there a airtable.com API to list Airtable invoices?

You do not need one. "List Airtable invoices" drives the real airtable.com pages in a browser, so it works whether or not airtable.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns total, invoices.

### Do I need to be logged in to airtable.com?

Yes. It acts as you on airtable.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the airtable.com cookies saved by the Reduck extension.

### Does it change anything on airtable.com, or only read data?

It only reads. It looks things up on airtable.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/airtable.com/list_invoices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/airtable.com/list_invoices

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/airtable.com/list_invoices
