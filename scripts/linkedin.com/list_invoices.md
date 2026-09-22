# List LinkedIn invoices/receipts

Automatically list LinkedIn invoices/receipts on linkedin.com. List and download LinkedIn purchase receipts from the Admin Center > Transactions (Premium, Sales Navigator, etc.). Each receipt PDF is downloaded automatically via the row's ... > Download receipt action. Online purchases expose receipts here; sales-rep-assisted contracts expose invoices instead, and this requires billing-management access. Returns total plus invoices (date, amount, payment_method, invoice_number, status, purchase, filename, path).

- Site: linkedin.com
- Address: `reduck/linkedin.com/list_invoices`
- Updated: 2026-08-21 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/list_invoices`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/list_invoices
```

## Input

It takes no input.

## Output

- `total` (integer, required)
- `invoices` (array, required)

## FAQ

### What does "List LinkedIn invoices/receipts" do?

List and download LinkedIn purchase receipts from the Admin Center > Transactions (Premium, Sales Navigator, etc.). Each receipt PDF is downloaded automatically via the row's ... > Download receipt action. Online purchases expose receipts here; sales-rep-assisted contracts expose invoices instead, and this requires billing-management access. Returns total plus invoices (date, amount, payment_method, invoice_number, status, purchase, filename, path).

### How do I automatically list LinkedIn invoices/receipts on linkedin.com?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/list_invoices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/list_invoices

### Is there a linkedin.com API to list LinkedIn invoices/receipts?

You do not need one. "List LinkedIn invoices/receipts" drives the real linkedin.com pages in a browser, so it works whether or not linkedin.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns total, invoices.

### Do I need to be logged in to linkedin.com?

Yes. It acts as you on linkedin.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linkedin.com cookies saved by the Reduck extension.

### Does it change anything on linkedin.com, or only read data?

It only reads. It looks things up on linkedin.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/list_invoices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/list_invoices

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/list_invoices
