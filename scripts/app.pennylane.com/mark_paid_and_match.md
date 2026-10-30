# Match a Pennylane supplier invoice to a bank transaction

Links one Pennylane supplier invoice to a bank transaction that already happened on the company's account, which marks the invoice as paid in the books. It never sends a payment. With dryRun (default true) it only reads the invoice and the transaction and returns both, without linking them; dryRun false links them and returns the amount left to match (0 when the amounts agree, a small value for a currency gap, the difference when the transaction is larger than the invoice). Find the transaction with app.pennylane.com/find_transactions_for_invoice. Fails when the invoice or the transaction does not exist, and when signed out of Pennylane.

- Site: app.pennylane.com
- Address: `reduck/app.pennylane.com/mark_paid_and_match`
- Updated: 2026-10-29 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/app.pennylane.com/mark_paid_and_match`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/app.pennylane.com/mark_paid_and_match
```

## Input

- `companyId` (string | integer, required): The number in the app URL at /companies/<id>/.
- `invoiceId` (string | integer, required): Supplier invoice id, as app.pennylane.com/list_invoices returns it.
- `transactionId` (string, required): Bank transaction id, as app.pennylane.com/find_transactions_for_invoice returns it.
- `dryRun` (boolean, optional): When true, read both records and return them without linking.

## Output

- `dryRun` (boolean, required)
- `invoice` (object, required)
- `matched` (boolean, required)
- `transaction` (object, required)
- `remainingToMatch` (string | null, optional)

## FAQ

### What does "Match a Pennylane supplier invoice to a bank transaction" do?

Links one Pennylane supplier invoice to a bank transaction that already happened on the company's account, which marks the invoice as paid in the books. It never sends a payment. With dryRun (default true) it only reads the invoice and the transaction and returns both, without linking them; dryRun false links them and returns the amount left to match (0 when the amounts agree, a small value for a currency gap, the difference when the transaction is larger than the invoice). Find the transaction with app.pennylane.com/find_transactions_for_invoice. Fails when the invoice or the transaction does not exist, and when signed out of Pennylane.

### What information do I need to provide?

Required: companyId, invoiceId, transactionId. Optional: dryRun.

### What does it return?

It returns dryRun, invoice, matched, transaction, remainingToMatch.

### Do I need to be logged in to app.pennylane.com?

Yes. It acts as you on app.pennylane.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the app.pennylane.com cookies saved by the Reduck extension.

### Does it change anything on app.pennylane.com, or only read data?

It makes changes on app.pennylane.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/app.pennylane.com/mark_paid_and_match, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.pennylane.com/mark_paid_and_match

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/app.pennylane.com/mark_paid_and_match
