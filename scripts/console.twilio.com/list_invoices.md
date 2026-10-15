# Twilio Console: list invoices

Automatically list invoices on console.twilio.com. List the signed-in Twilio account's monthly payment receipts (payments, totals, invoiceId for download_invoice) and usage statements.

- Site: console.twilio.com
- Address: `reduck/console.twilio.com/list_invoices`
- Updated: 2026-10-14 (v6)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/console.twilio.com/list_invoices`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/console.twilio.com/list_invoices
```

## Input

- `maxMonths` (integer, optional): How many months with payment activity to include, newest first.

## Output

- `receipts` (array, required)
- `statements` (array, required)
- `receiptCount` (integer, required)
- `statementCount` (integer, required)
- `monthsWithActivity` (array, optional)

## FAQ

### What does "Twilio Console: list invoices" do?

List the signed-in Twilio account's monthly payment receipts (payments, totals, invoiceId for download_invoice) and usage statements.

### How do I automatically list invoices on console.twilio.com?

Ask an AI agent connected to Reduck to run reduck/console.twilio.com/list_invoices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/console.twilio.com/list_invoices

### Is there a console.twilio.com API to list invoices?

You do not need one. "Twilio Console: list invoices" drives the real console.twilio.com pages in a browser, so it works whether or not console.twilio.com offers an API for this.

### What information do I need to provide?

Optional: maxMonths.

### What does it return?

It returns receipts, statements, receiptCount, statementCount, monthsWithActivity.

### Do I need to be logged in to console.twilio.com?

Yes. It acts as you on console.twilio.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the console.twilio.com cookies saved by the Reduck extension.

### Does it change anything on console.twilio.com, or only read data?

It only reads. It looks things up on console.twilio.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/console.twilio.com/list_invoices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/console.twilio.com/list_invoices

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/console.twilio.com/list_invoices
