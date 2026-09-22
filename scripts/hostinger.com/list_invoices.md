# List Hostinger invoices

Automatically list Hostinger invoices on hostinger.com. List Hostinger (hPanel) billing invoices from Billing > Payment history. Returns total plus each invoice's payment_id, invoice_id, service, paid_at, amount, filename, and the invoice PDF included as base64. Reads the Paid tab only (not Refund history).

- Site: hostinger.com
- Address: `reduck/hostinger.com/list_invoices`
- Updated: 2026-08-21 (v7)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/hostinger.com/list_invoices`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/hostinger.com/list_invoices
```

## Input

It takes no input.

## Output

- `total` (integer, required)
- `invoices` (array, required)

## FAQ

### What does "List Hostinger invoices" do?

List Hostinger (hPanel) billing invoices from Billing > Payment history. Returns total plus each invoice's payment_id, invoice_id, service, paid_at, amount, filename, and the invoice PDF included as base64. Reads the Paid tab only (not Refund history).

### How do I automatically list Hostinger invoices on hostinger.com?

Ask an AI agent connected to Reduck to run reduck/hostinger.com/list_invoices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/hostinger.com/list_invoices

### Is there a hostinger.com API to list Hostinger invoices?

You do not need one. "List Hostinger invoices" drives the real hostinger.com pages in a browser, so it works whether or not hostinger.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns total, invoices.

### Do I need to be logged in to hostinger.com?

Yes. It acts as you on hostinger.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the hostinger.com cookies saved by the Reduck extension.

### Does it change anything on hostinger.com, or only read data?

It only reads. It looks things up on hostinger.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/hostinger.com/list_invoices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/hostinger.com/list_invoices

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/hostinger.com/list_invoices
