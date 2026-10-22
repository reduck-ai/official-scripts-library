# List LinkedIn invoices

Automatically list LinkedIn invoices on linkedin.com. List every LinkedIn billing transaction (Premium, Sales Navigator and other purchases) of the account the Admin Center opens, newest first. For each, you get the invoice number, the time of issue in UTC, the amount and its ISO currency, the status and type as LinkedIn gives them, the product, the payment methods, and whether a receipt PDF is available. Give an invoice number to linkedin.com/download_invoice to get its receipt. The list is always complete, also when the account has more transactions than the page shows at once. If the signed-in member manages no billing account, the run stops with a message that says so.

- Site: linkedin.com
- Address: `reduck/linkedin.com/list_invoices`
- Updated: 2026-10-21 (v5)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/list_invoices`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/list_invoices
```

## Input

It takes no input.

## Output

- `total` (integer, required): The number of transactions LinkedIn states for the account. invoices always holds all of them.
- `invoices` (array, required): Newest first, in the order the Transactions page shows them.

## FAQ

### What does "List LinkedIn invoices" do?

List every LinkedIn billing transaction (Premium, Sales Navigator and other purchases) of the account the Admin Center opens, newest first. For each, you get the invoice number, the time of issue in UTC, the amount and its ISO currency, the status and type as LinkedIn gives them, the product, the payment methods, and whether a receipt PDF is available. Give an invoice number to linkedin.com/download_invoice to get its receipt. The list is always complete, also when the account has more transactions than the page shows at once. If the signed-in member manages no billing account, the run stops with a message that says so.

### How do I automatically list LinkedIn invoices on linkedin.com?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/list_invoices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/list_invoices

### Is there a linkedin.com API to list LinkedIn invoices?

You do not need one. "List LinkedIn invoices" drives the real linkedin.com pages in a browser, so it works whether or not linkedin.com offers an API for this.

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
