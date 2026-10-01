# Download Dropbox invoice as PDF

Automatically download Dropbox invoice as PDF on dropbox.com. Download one Dropbox invoice or receipt as a PDF, given an invoiceUrl or receiptUrl from dropbox.com/list_invoices. Returns the filename and the PDF as base64.

- Site: dropbox.com
- Address: `reduck/dropbox.com/download_invoice`
- Updated: 2026-09-30 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/dropbox.com/download_invoice`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/dropbox.com/download_invoice
```

## Input

- `url` (string, required): invoiceUrl or receiptUrl returned by dropbox.com/list_invoices

## Output

- `filename` (string, required)
- `contentBase64` (string, required)

## FAQ

### What does "Download Dropbox invoice as PDF" do?

Download one Dropbox invoice or receipt as a PDF, given an invoiceUrl or receiptUrl from dropbox.com/list_invoices. Returns the filename and the PDF as base64.

### How do I automatically download Dropbox invoice as PDF on dropbox.com?

Ask an AI agent connected to Reduck to run reduck/dropbox.com/download_invoice, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/dropbox.com/download_invoice

### Is there a dropbox.com API to download Dropbox invoice as PDF?

You do not need one. "Download Dropbox invoice as PDF" drives the real dropbox.com pages in a browser, so it works whether or not dropbox.com offers an API for this.

### What information do I need to provide?

Required: url.

### What does it return?

It returns filename, contentBase64.

### Do I need to be logged in to dropbox.com?

Yes. It acts as you on dropbox.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the dropbox.com cookies saved by the Reduck extension.

### Does it change anything on dropbox.com, or only read data?

It only reads. It looks things up on dropbox.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/dropbox.com/download_invoice, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/dropbox.com/download_invoice

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/dropbox.com/download_invoice
