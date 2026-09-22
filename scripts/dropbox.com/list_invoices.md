# List Dropbox invoices

Automatically list Dropbox invoices on dropbox.com. List Dropbox billing history for the signed-in account (Manage › Billing), with per-entry date, description, status and amount. Returns invoiceUrl and receiptUrl per payment, both session-gated HTML pages. Dropbox exposes no direct PDF, so print-to-PDF to archive.

- Site: dropbox.com
- Address: `reduck/dropbox.com/list_invoices`
- Updated: 2026-08-21 (v5)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/dropbox.com/list_invoices`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/dropbox.com/list_invoices
```

## Input

It takes no input.

## Output

- `count` (integer, required)
- `invoices` (array, required)

## FAQ

### What does "List Dropbox invoices" do?

List Dropbox billing history for the signed-in account (Manage › Billing), with per-entry date, description, status and amount. Returns invoiceUrl and receiptUrl per payment, both session-gated HTML pages. Dropbox exposes no direct PDF, so print-to-PDF to archive.

### How do I automatically list Dropbox invoices on dropbox.com?

Ask an AI agent connected to Reduck to run reduck/dropbox.com/list_invoices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/dropbox.com/list_invoices

### Is there a dropbox.com API to list Dropbox invoices?

You do not need one. "List Dropbox invoices" drives the real dropbox.com pages in a browser, so it works whether or not dropbox.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns count, invoices.

### Do I need to be logged in to dropbox.com?

Yes. It acts as you on dropbox.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the dropbox.com cookies saved by the Reduck extension.

### Does it change anything on dropbox.com, or only read data?

It only reads. It looks things up on dropbox.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/dropbox.com/list_invoices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/dropbox.com/list_invoices

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/dropbox.com/list_invoices
