# List Zapier invoices

Automatically list Zapier invoices on zapier.com. List Zapier billing invoices from Settings > Billing & usage > Billing settings > Invoices. Returns total and invoices (status, date, amount, invoice_id, href) — metadata only. Feed a row's href to zapier.com/download_invoice to get that invoice as a PDF (Zapier has no native PDF, so that script renders the invoice page to one). An account with no billing history returns an empty list. Requires a Zapier session with billing access.

- Site: zapier.com
- Address: `reduck/zapier.com/list_invoices`
- Updated: 2026-09-29 (v10)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/zapier.com/list_invoices`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/zapier.com/list_invoices
```

## Input

It takes no input.

## Output

- `total` (integer, required)
- `invoices` (array, required)

## FAQ

### What does "List Zapier invoices" do?

List Zapier billing invoices from Settings > Billing & usage > Billing settings > Invoices. Returns total and invoices (status, date, amount, invoice_id, href) — metadata only. Feed a row's href to zapier.com/download_invoice to get that invoice as a PDF (Zapier has no native PDF, so that script renders the invoice page to one). An account with no billing history returns an empty list. Requires a Zapier session with billing access.

### How do I automatically list Zapier invoices on zapier.com?

Ask an AI agent connected to Reduck to run reduck/zapier.com/list_invoices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/zapier.com/list_invoices

### Is there a zapier.com API to list Zapier invoices?

You do not need one. "List Zapier invoices" drives the real zapier.com pages in a browser, so it works whether or not zapier.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns total, invoices.

### Do I need to be logged in to zapier.com?

Yes. It acts as you on zapier.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the zapier.com cookies saved by the Reduck extension.

### Does it change anything on zapier.com, or only read data?

It only reads. It looks things up on zapier.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/zapier.com/list_invoices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/zapier.com/list_invoices

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/zapier.com/list_invoices
