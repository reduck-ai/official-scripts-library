# List Surfshark invoices/receipts

Automatically list Surfshark invoices/receipts on surfshark.com. List and download Surfshark payment receipts from your account's subscription payments page. Returns total and invoices (purchase, date, amount, status, filename, PDF content); each successful payment's receipt PDF is included as base64, while cancelled or failed payments have none and are skipped. Works regardless of the account's display language.

- Site: surfshark.com
- Address: `reduck/surfshark.com/list_invoices`
- Updated: 2026-08-21 (v9)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/surfshark.com/list_invoices`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/surfshark.com/list_invoices
```

## Input

It takes no input.

## Output

- `total` (integer, required)
- `invoices` (array, required)

## FAQ

### What does "List Surfshark invoices/receipts" do?

List and download Surfshark payment receipts from your account's subscription payments page. Returns total and invoices (purchase, date, amount, status, filename, PDF content); each successful payment's receipt PDF is included as base64, while cancelled or failed payments have none and are skipped. Works regardless of the account's display language.

### How do I automatically list Surfshark invoices/receipts on surfshark.com?

Ask an AI agent connected to Reduck to run reduck/surfshark.com/list_invoices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/surfshark.com/list_invoices

### Is there a surfshark.com API to list Surfshark invoices/receipts?

You do not need one. "List Surfshark invoices/receipts" drives the real surfshark.com pages in a browser, so it works whether or not surfshark.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns total, invoices.

### Do I need to be logged in to surfshark.com?

Yes. It acts as you on surfshark.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the surfshark.com cookies saved by the Reduck extension.

### Does it change anything on surfshark.com, or only read data?

It only reads. It looks things up on surfshark.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/surfshark.com/list_invoices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/surfshark.com/list_invoices

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/surfshark.com/list_invoices
