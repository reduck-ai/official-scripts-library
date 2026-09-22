# List Numerous.ai invoices

Automatically list Numerous.ai invoices on numerous.ai. List Numerous.ai subscription invoices. Returns total and invoices (date, amount, status, description, and hostedInvoiceUrl - an invoice.stripe.com link you can feed to invoice.stripe.com/download_invoice_pdf). Assumes at least one invoice (a paying account).

- Site: numerous.ai
- Address: `reduck/numerous.ai/list_invoices`
- Updated: 2026-08-19 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/numerous.ai/list_invoices`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/numerous.ai/list_invoices
```

## Input

It takes no input.

## Output

- `total` (integer, required)
- `invoices` (array, required)

## FAQ

### What does "List Numerous.ai invoices" do?

List Numerous.ai subscription invoices. Returns total and invoices (date, amount, status, description, and hostedInvoiceUrl - an invoice.stripe.com link you can feed to invoice.stripe.com/download_invoice_pdf). Assumes at least one invoice (a paying account).

### How do I automatically list Numerous.ai invoices on numerous.ai?

Ask an AI agent connected to Reduck to run reduck/numerous.ai/list_invoices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/numerous.ai/list_invoices

### Is there a numerous.ai API to list Numerous.ai invoices?

You do not need one. "List Numerous.ai invoices" drives the real numerous.ai pages in a browser, so it works whether or not numerous.ai offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns total, invoices.

### Do I need to be logged in to numerous.ai?

Yes. It acts as you on numerous.ai: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the numerous.ai cookies saved by the Reduck extension.

### Does it change anything on numerous.ai, or only read data?

It only reads. It looks things up on numerous.ai and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/numerous.ai/list_invoices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/numerous.ai/list_invoices

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/numerous.ai/list_invoices
