# Find Pennylane bank transactions for a supplier invoice

Automatically find Pennylane bank transactions for a supplier invoice on app.pennylane.com. Lists the bank transactions a Pennylane supplier invoice can be matched to: Pennylane's own suggestions for that invoice, with their confidence score, and one page of the company's bank transactions, newest first, which can be narrowed by words of the bank label, an exact amount and a date range. Transactions already grouped with this invoice are left out of both lists; invoice.remainingToMatch says how much of the invoice is still unmatched (0 when fully matched). Amounts of transactions are signed as on the bank statement, so money paid out is negative, and their remainingToMatch is the part Pennylane still counts as unmatched. It only reads and never matches anything. Fails when the invoice does not exist and when signed out of Pennylane.

- Site: app.pennylane.com
- Address: `reduck/app.pennylane.com/find_transactions_for_invoice`
- Updated: 2026-10-29 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/app.pennylane.com/find_transactions_for_invoice`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/app.pennylane.com/find_transactions_for_invoice
```

## Input

- `companyId` (string | integer, required): The number in the app URL at /companies/<id>/.
- `invoiceId` (string | integer, required): Supplier invoice id, as app.pennylane.com/list_invoices returns it.
- `page` (integer, optional): Page of transactions, 1-indexed.
- `label` (string, optional): Words to look for in the bank label of the transaction, such as the supplier name.
- `amount` (number, optional): Exact transaction amount in euros, signed as on the bank statement: an invoice of 276 EUR paid out is -276.
- `dateTo` (string, optional): Latest transaction date, YYYY-MM-DD.
- `perPage` (integer, optional): Transactions per page.
- `dateFrom` (string, optional): Earliest transaction date, YYYY-MM-DD.
- `maxSuggestions` (integer, optional): How many suggestions to ask Pennylane for.

## Output

- `invoice` (object, required)
- `pagination` (object, required)
- `suggestions` (array, required)
- `transactions` (array, required)

## FAQ

### What does "Find Pennylane bank transactions for a supplier invoice" do?

Lists the bank transactions a Pennylane supplier invoice can be matched to: Pennylane's own suggestions for that invoice, with their confidence score, and one page of the company's bank transactions, newest first, which can be narrowed by words of the bank label, an exact amount and a date range. Transactions already grouped with this invoice are left out of both lists; invoice.remainingToMatch says how much of the invoice is still unmatched (0 when fully matched). Amounts of transactions are signed as on the bank statement, so money paid out is negative, and their remainingToMatch is the part Pennylane still counts as unmatched. It only reads and never matches anything. Fails when the invoice does not exist and when signed out of Pennylane.

### How do I automatically find Pennylane bank transactions for a supplier invoice on app.pennylane.com?

Ask an AI agent connected to Reduck to run reduck/app.pennylane.com/find_transactions_for_invoice, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.pennylane.com/find_transactions_for_invoice

### Is there a app.pennylane.com API to find Pennylane bank transactions for a supplier invoice?

You do not need one. "Find Pennylane bank transactions for a supplier invoice" drives the real app.pennylane.com pages in a browser, so it works whether or not app.pennylane.com offers an API for this.

### What information do I need to provide?

Required: companyId, invoiceId. Optional: page, label, amount, dateTo, perPage, dateFrom, maxSuggestions.

### What does it return?

It returns invoice, pagination, suggestions, transactions.

### Do I need to be logged in to app.pennylane.com?

Yes. It acts as you on app.pennylane.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the app.pennylane.com cookies saved by the Reduck extension.

### Does it change anything on app.pennylane.com, or only read data?

It only reads. It looks things up on app.pennylane.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/app.pennylane.com/find_transactions_for_invoice, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.pennylane.com/find_transactions_for_invoice

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/app.pennylane.com/find_transactions_for_invoice
