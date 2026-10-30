# Twilio Console: list invoices

Automatically list invoices on console.twilio.com. List the signed-in Twilio account's monthly payment receipts, newest first: for each month with payments, its total, currency, each payment (date, amount, tax, status, masked card) and the receipt id to pass to download_invoice. Reads maxMonths calendar months (12 by default) starting with the current month, or with the month given; monthsRead lists every month read, with or without payments. A signed-out browser is reported as such.

- Site: console.twilio.com
- Address: `reduck/console.twilio.com/list_invoices`
- Updated: 2026-10-29 (v11)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/console.twilio.com/list_invoices`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/console.twilio.com/list_invoices
```

## Input

- `month` (string, optional): The newest month to read, YYYY-MM; earlier months follow. Omit to start with the current month.
- `maxMonths` (integer, optional): How many calendar months to read, newest first.

## Output

- `receipts` (array, required): One receipt per month that holds payments, newest first.
- `monthsRead` (array, required): Every month read, YYYY-MM, newest first, with or without payments.
- `receiptCount` (integer, required)

## FAQ

### What does "Twilio Console: list invoices" do?

List the signed-in Twilio account's monthly payment receipts, newest first: for each month with payments, its total, currency, each payment (date, amount, tax, status, masked card) and the receipt id to pass to download_invoice. Reads maxMonths calendar months (12 by default) starting with the current month, or with the month given; monthsRead lists every month read, with or without payments. A signed-out browser is reported as such.

### How do I automatically list invoices on console.twilio.com?

Ask an AI agent connected to Reduck to run reduck/console.twilio.com/list_invoices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/console.twilio.com/list_invoices

### Is there a console.twilio.com API to list invoices?

You do not need one. "Twilio Console: list invoices" drives the real console.twilio.com pages in a browser, so it works whether or not console.twilio.com offers an API for this.

### What information do I need to provide?

Optional: month, maxMonths.

### What does it return?

It returns receipts, monthsRead, receiptCount.

### Do I need to be logged in to console.twilio.com?

Yes. It acts as you on console.twilio.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the console.twilio.com cookies saved by the Reduck extension.

### Does it change anything on console.twilio.com, or only read data?

It only reads. It looks things up on console.twilio.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/console.twilio.com/list_invoices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/console.twilio.com/list_invoices

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/console.twilio.com/list_invoices
