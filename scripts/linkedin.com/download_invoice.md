# Download LinkedIn receipt

Automatically download LinkedIn receipt on linkedin.com. Download the receipt PDF of one LinkedIn billing transaction, by its invoice number from linkedin.com/list_invoices. Returns the PDF base64-encoded, with a file name. Some transactions have no receipt (LinkedIn says the receipt is not available): for those, receipt_available is false and no file comes back. An invoice number the account does not have stops the run with a message that says so.

- Site: linkedin.com
- Address: `reduck/linkedin.com/download_invoice`
- Updated: 2026-10-21 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/download_invoice`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/download_invoice
```

## Input

- `invoice_number` (string, required): The invoice_number of a transaction from linkedin.com/list_invoices.

## Output

- `filename` (string | null, required): A file name for the PDF.
- `contentBase64` (string | null, required): The receipt PDF, base64-encoded.
- `invoice_number` (string, required)
- `receipt_available` (boolean, required): False when LinkedIn has no receipt for this transaction. filename and contentBase64 are then null.

## FAQ

### What does "Download LinkedIn receipt" do?

Download the receipt PDF of one LinkedIn billing transaction, by its invoice number from linkedin.com/list_invoices. Returns the PDF base64-encoded, with a file name. Some transactions have no receipt (LinkedIn says the receipt is not available): for those, receipt_available is false and no file comes back. An invoice number the account does not have stops the run with a message that says so.

### How do I automatically download LinkedIn receipt on linkedin.com?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/download_invoice, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/download_invoice

### Is there a linkedin.com API to download LinkedIn receipt?

You do not need one. "Download LinkedIn receipt" drives the real linkedin.com pages in a browser, so it works whether or not linkedin.com offers an API for this.

### What information do I need to provide?

Required: invoice_number.

### What does it return?

It returns filename, contentBase64, invoice_number, receipt_available.

### Do I need to be logged in to linkedin.com?

Yes. It acts as you on linkedin.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linkedin.com cookies saved by the Reduck extension.

### Does it change anything on linkedin.com, or only read data?

It only reads. It looks things up on linkedin.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/download_invoice, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/download_invoice

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/download_invoice
