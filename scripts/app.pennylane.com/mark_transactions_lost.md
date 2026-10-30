# Mark Pennylane bank transactions as having a lost receipt

Automatically mark Pennylane bank transactions as having a lost receipt on app.pennylane.com. Marks one or more Pennylane bank transactions as having a lost receipt, as the transaction's Proof menu does, so they stop showing as waiting for a receipt. With dryRun (default true) each transaction is opened and its Proof menu used, but the change is held back. With dryRun false it is saved, then read back. Returns, per transaction, its label, amount, whether it is still pending at the bank, whether a receipt was already lost or attached before the run, and whether it is now marked lost. A transaction that already has a receipt attached is left as it is, with a warning. Fails when a transaction id does not exist and when signed out of Pennylane.

- Site: app.pennylane.com
- Address: `reduck/app.pennylane.com/mark_transactions_lost`
- Updated: 2026-10-29 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/app.pennylane.com/mark_transactions_lost`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/app.pennylane.com/mark_transactions_lost
```

## Input

- `companyId` (string | integer, required): The number in the app URL at /companies/<id>/.
- `transactionIds` (array, required): Bank transaction ids, as app.pennylane.com/find_transactions_for_invoice or get_transactions return them.
- `dryRun` (boolean, optional): true (default): open each transaction and its Proof menu, hold the change back. false: save it.

## Output

- `dryRun` (boolean, required)
- `results` (array, required)
- `markedCount` (number, required)

## FAQ

### What does "Mark Pennylane bank transactions as having a lost receipt" do?

Marks one or more Pennylane bank transactions as having a lost receipt, as the transaction's Proof menu does, so they stop showing as waiting for a receipt. With dryRun (default true) each transaction is opened and its Proof menu used, but the change is held back. With dryRun false it is saved, then read back. Returns, per transaction, its label, amount, whether it is still pending at the bank, whether a receipt was already lost or attached before the run, and whether it is now marked lost. A transaction that already has a receipt attached is left as it is, with a warning. Fails when a transaction id does not exist and when signed out of Pennylane.

### How do I automatically mark Pennylane bank transactions as having a lost receipt on app.pennylane.com?

Ask an AI agent connected to Reduck to run reduck/app.pennylane.com/mark_transactions_lost, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.pennylane.com/mark_transactions_lost

### Is there a app.pennylane.com API to mark Pennylane bank transactions as having a lost receipt?

You do not need one. "Mark Pennylane bank transactions as having a lost receipt" drives the real app.pennylane.com pages in a browser, so it works whether or not app.pennylane.com offers an API for this.

### What information do I need to provide?

Required: companyId, transactionIds. Optional: dryRun.

### What does it return?

It returns dryRun, results, markedCount.

### Do I need to be logged in to app.pennylane.com?

Yes. It acts as you on app.pennylane.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the app.pennylane.com cookies saved by the Reduck extension.

### Does it change anything on app.pennylane.com, or only read data?

It makes changes on app.pennylane.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/app.pennylane.com/mark_transactions_lost, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.pennylane.com/mark_transactions_lost

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/app.pennylane.com/mark_transactions_lost
