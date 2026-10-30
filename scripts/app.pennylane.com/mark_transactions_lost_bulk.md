# Mark many Pennylane bank transactions as having a lost receipt at once

Automatically mark many Pennylane bank transactions as having a lost receipt at once on app.pennylane.com. Marks a list of Pennylane bank transactions as having a lost receipt in one go, with the transactions list's bulk action, so they stop showing as waiting for a receipt. Faster than app.pennylane.com/mark_transactions_lost, which opens each transaction. With dryRun (default true) the bulk action is used but the change is held back. With dryRun false it is saved, then each transaction is read back. Returns, per transaction, its label, amount, date, whether it is still pending at the bank, its attached receipts and whether it is now marked lost. Up to 200 transactions per run. Fails when signed out of Pennylane.

- Site: app.pennylane.com
- Address: `reduck/app.pennylane.com/mark_transactions_lost_bulk`
- Updated: 2026-10-29 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/app.pennylane.com/mark_transactions_lost_bulk`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/app.pennylane.com/mark_transactions_lost_bulk
```

## Input

- `companyId` (string | integer, required): The number in the app URL at /companies/<id>/.
- `transactionIds` (array, required): Bank transaction ids, as app.pennylane.com/find_transactions_for_invoice or get_transactions return them.
- `dryRun` (boolean, optional): true (default): use the bulk action, hold the change back. false: save it.

## Output

- `dryRun` (boolean, required)
- `results` (array, required)
- `markedCount` (number, required)

## FAQ

### What does "Mark many Pennylane bank transactions as having a lost receipt at once" do?

Marks a list of Pennylane bank transactions as having a lost receipt in one go, with the transactions list's bulk action, so they stop showing as waiting for a receipt. Faster than app.pennylane.com/mark_transactions_lost, which opens each transaction. With dryRun (default true) the bulk action is used but the change is held back. With dryRun false it is saved, then each transaction is read back. Returns, per transaction, its label, amount, date, whether it is still pending at the bank, its attached receipts and whether it is now marked lost. Up to 200 transactions per run. Fails when signed out of Pennylane.

### How do I automatically mark many Pennylane bank transactions as having a lost receipt at once on app.pennylane.com?

Ask an AI agent connected to Reduck to run reduck/app.pennylane.com/mark_transactions_lost_bulk, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.pennylane.com/mark_transactions_lost_bulk

### Is there a app.pennylane.com API to mark many Pennylane bank transactions as having a lost receipt at once?

You do not need one. "Mark many Pennylane bank transactions as having a lost receipt at once" drives the real app.pennylane.com pages in a browser, so it works whether or not app.pennylane.com offers an API for this.

### What information do I need to provide?

Required: companyId, transactionIds. Optional: dryRun.

### What does it return?

It returns dryRun, results, markedCount.

### Do I need to be logged in to app.pennylane.com?

Yes. It acts as you on app.pennylane.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the app.pennylane.com cookies saved by the Reduck extension.

### Does it change anything on app.pennylane.com, or only read data?

It makes changes on app.pennylane.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/app.pennylane.com/mark_transactions_lost_bulk, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.pennylane.com/mark_transactions_lost_bulk

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/app.pennylane.com/mark_transactions_lost_bulk
