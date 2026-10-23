# Download Postmark receipt

Automatically download Postmark receipt on account.postmarkapp.com. Download one Postmark billing receipt as a PDF, by the receiptId from list_invoices. Returns the saved file's name and its path (or a link to it on a managed browser). Fails with a clear error when the receipt does not exist in this account.

- Site: account.postmarkapp.com
- Address: `reduck/account.postmarkapp.com/download_invoice`
- Updated: 2026-10-22 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/account.postmarkapp.com/download_invoice`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/account.postmarkapp.com/download_invoice
```

## Input

- `receiptId` (string, required): Receipt id from list_invoices, e.g. 12627512.

## Output

- `filename` (string, required)
- `receiptId` (string, required)
- `url` (string, optional)
- `path` (string, optional)

## FAQ

### What does "Download Postmark receipt" do?

Download one Postmark billing receipt as a PDF, by the receiptId from list_invoices. Returns the saved file's name and its path (or a link to it on a managed browser). Fails with a clear error when the receipt does not exist in this account.

### How do I automatically download Postmark receipt on account.postmarkapp.com?

Ask an AI agent connected to Reduck to run reduck/account.postmarkapp.com/download_invoice, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/account.postmarkapp.com/download_invoice

### Is there a account.postmarkapp.com API to download Postmark receipt?

You do not need one. "Download Postmark receipt" drives the real account.postmarkapp.com pages in a browser, so it works whether or not account.postmarkapp.com offers an API for this.

### What information do I need to provide?

Required: receiptId.

### What does it return?

It returns url, path, filename, receiptId.

### Do I need to be logged in to account.postmarkapp.com?

Yes. It acts as you on account.postmarkapp.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the account.postmarkapp.com cookies saved by the Reduck extension.

### Does it change anything on account.postmarkapp.com, or only read data?

It only reads. It looks things up on account.postmarkapp.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/account.postmarkapp.com/download_invoice, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/account.postmarkapp.com/download_invoice

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/account.postmarkapp.com/download_invoice
