# Qonto: attach a receipt to a transaction

Automatically attach a receipt to a transaction on qonto.com. Attach a receipt file to a Qonto transaction by its id. Dry run checks the transaction and the upload control without attaching anything.

- Site: qonto.com
- Address: `reduck/qonto.com/attach_receipt`
- Updated: 2026-10-07 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/qonto.com/attach_receipt`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/qonto.com/attach_receipt
```

## Input

- `transactionId` (string, required): Qonto transaction id, as returned by qonto.com/list_transactions.
- `dry_run` (boolean, optional): When true (default), finds the transaction and its receipt upload control, reports how many receipts it already has, and stops without attaching anything.
- `receipt` (string, optional): The receipt or invoice file (PDF or image) to attach. Required unless dry_run is true.
- `receiptName` (string, optional): File name to show in Qonto, e.g. slack_invoice_SBIE-10873175.pdf. Without it the file is named after the input.
- `counterparty` (string, optional): The transaction's counterparty as returned by qonto.com/list_transactions (e.g. "Slack"). Needed for transactions older than the newest page, which are found by searching it.
- `allowAdditional` (boolean, optional): Attach even when the transaction already has a receipt. Off by default to avoid duplicates.

## Output

- `dryRun` (boolean, required)
- `attached` (boolean, required)
- `transactionId` (string, required)
- `amount` (string | null, optional)
- `fileName` (string | null, optional)
- `counterparty` (string | null, optional)
- `organization` (string, optional)
- `attachmentsAfter` (integer | null, optional): Receipts after the upload, read back from Qonto.
- `attachmentsBefore` (integer | null, optional): Receipts on the transaction before this run.
- `uploadControlReady` (boolean, optional)

## FAQ

### What does "Qonto: attach a receipt to a transaction" do?

Attach a receipt file to a Qonto transaction by its id. Dry run checks the transaction and the upload control without attaching anything.

### How do I automatically attach a receipt to a transaction on qonto.com?

Ask an AI agent connected to Reduck to run reduck/qonto.com/attach_receipt, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/qonto.com/attach_receipt

### Is there a qonto.com API to attach a receipt to a transaction?

You do not need one. "Qonto: attach a receipt to a transaction" drives the real qonto.com pages in a browser, so it works whether or not qonto.com offers an API for this.

### What information do I need to provide?

Required: transactionId. Optional: dry_run, receipt, receiptName, counterparty, allowAdditional.

### What does it return?

It returns amount, dryRun, attached, fileName, counterparty, organization, transactionId, attachmentsAfter, attachmentsBefore, uploadControlReady.

### Do I need to be logged in to qonto.com?

Yes. It acts as you on qonto.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the qonto.com cookies saved by the Reduck extension.

### Does it change anything on qonto.com, or only read data?

It makes changes on qonto.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/qonto.com/attach_receipt, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/qonto.com/attach_receipt

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/qonto.com/attach_receipt
