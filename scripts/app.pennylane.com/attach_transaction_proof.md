# Attach a receipt to a Pennylane bank transaction

Automatically attach a receipt to a Pennylane bank transaction on app.pennylane.com. Attaches a receipt file (PDF or image) to one Pennylane bank transaction, as the Proof drop zone of the transaction does, so the payment is justified. With dryRun (default true) the file is handed to the page but nothing is sent: the run returns the requests the page would have sent. With dryRun false it is uploaded, then the transaction is read back. Returns the transaction's label, amount and date, its receipts before and after, and whether the file was attached. Fails when the transaction does not exist and when signed out of Pennylane.

- Site: app.pennylane.com
- Address: `reduck/app.pennylane.com/attach_transaction_proof`
- Updated: 2026-10-29 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/app.pennylane.com/attach_transaction_proof`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/app.pennylane.com/attach_transaction_proof
```

## Input

- `proof` (string, required): The receipt to attach: a PDF, JPEG, PNG or HEIC file.
- `companyId` (string | integer, required): The number in the app URL at /companies/<id>/.
- `proofName` (string, required): The name the receipt gets in Pennylane, with its extension (.pdf, .jpg, .png or .heic), e.g. apple-store-2026-03-28.pdf.
- `transactionId` (string | integer, required): Bank transaction id, as app.pennylane.com/find_transactions_for_invoice or get_transactions return it.
- `dryRun` (boolean, optional): true (default): hand the file to the page and hold back what it sends. false: upload it.

## Output

- `dryRun` (boolean, required)
- `attached` (boolean, required): true when the transaction holds one more receipt after the run (dryRun: when the page started sending the file).
- `transactionId` (string, required)
- `date` (string | null, optional)
- `label` (string | null, optional)
- `amount` (number | null, optional)
- `heldBack` (array, optional): dryRun: the requests the page started to send, held back.
- `proofCountAfter` (number | null, optional)
- `proofCountBefore` (number | null, optional)

## FAQ

### What does "Attach a receipt to a Pennylane bank transaction" do?

Attaches a receipt file (PDF or image) to one Pennylane bank transaction, as the Proof drop zone of the transaction does, so the payment is justified. With dryRun (default true) the file is handed to the page but nothing is sent: the run returns the requests the page would have sent. With dryRun false it is uploaded, then the transaction is read back. Returns the transaction's label, amount and date, its receipts before and after, and whether the file was attached. Fails when the transaction does not exist and when signed out of Pennylane.

### How do I automatically attach a receipt to a Pennylane bank transaction on app.pennylane.com?

Ask an AI agent connected to Reduck to run reduck/app.pennylane.com/attach_transaction_proof, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.pennylane.com/attach_transaction_proof

### Is there a app.pennylane.com API to attach a receipt to a Pennylane bank transaction?

You do not need one. "Attach a receipt to a Pennylane bank transaction" drives the real app.pennylane.com pages in a browser, so it works whether or not app.pennylane.com offers an API for this.

### What information do I need to provide?

Required: companyId, transactionId, proof, proofName. Optional: dryRun.

### What does it return?

It returns date, label, amount, dryRun, attached, heldBack, transactionId, proofCountAfter, proofCountBefore.

### Do I need to be logged in to app.pennylane.com?

Yes. It acts as you on app.pennylane.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the app.pennylane.com cookies saved by the Reduck extension.

### Does it change anything on app.pennylane.com, or only read data?

It makes changes on app.pennylane.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/app.pennylane.com/attach_transaction_proof, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.pennylane.com/attach_transaction_proof

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/app.pennylane.com/attach_transaction_proof
