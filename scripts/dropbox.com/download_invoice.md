# Download Dropbox invoice as PDF

Automatically download Dropbox invoice as PDF on dropbox.com. Download one Dropbox invoice or receipt as a PDF. Pass the invoiceUrl or receiptUrl from dropbox.com/list_invoices (or either one as url). Returns the file name and where the PDF was saved: a path in the browser's downloads folder, or a url to the file on a managed browser. A browser not signed in to Dropbox fails with a message saying so.

- Site: dropbox.com
- Address: `reduck/dropbox.com/download_invoice`
- Updated: 2026-10-22 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/dropbox.com/download_invoice`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/dropbox.com/download_invoice
```

## Input

- `url` (string, optional): invoiceUrl or receiptUrl returned by dropbox.com/list_invoices.
- `invoiceUrl` (string, optional): An invoiceUrl from dropbox.com/list_invoices: downloads the invoice. Pass exactly one of url, invoiceUrl or receiptUrl.
- `receiptUrl` (string, optional): A receiptUrl from dropbox.com/list_invoices: downloads the receipt. Pass exactly one of url, invoiceUrl or receiptUrl.

## Output

- `filename` (string, required): The saved file name, e.g. Dropbox-invoice-<billId>.pdf. A repeat download can end in (2).
- `url` (string, optional): On a managed browser, a link to the PDF bytes.
- `path` (string, optional): Where the PDF is saved on the machine running the browser (on a paired Chrome, its downloads folder).

## FAQ

### What does "Download Dropbox invoice as PDF" do?

Download one Dropbox invoice or receipt as a PDF. Pass the invoiceUrl or receiptUrl from dropbox.com/list_invoices (or either one as url). Returns the file name and where the PDF was saved: a path in the browser's downloads folder, or a url to the file on a managed browser. A browser not signed in to Dropbox fails with a message saying so.

### How do I automatically download Dropbox invoice as PDF on dropbox.com?

Ask an AI agent connected to Reduck to run reduck/dropbox.com/download_invoice, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/dropbox.com/download_invoice

### Is there a dropbox.com API to download Dropbox invoice as PDF?

You do not need one. "Download Dropbox invoice as PDF" drives the real dropbox.com pages in a browser, so it works whether or not dropbox.com offers an API for this.

### What information do I need to provide?

Optional: url, invoiceUrl, receiptUrl.

### What does it return?

It returns url, path, filename.

### Do I need to be logged in to dropbox.com?

Yes. It acts as you on dropbox.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the dropbox.com cookies saved by the Reduck extension.

### Does it change anything on dropbox.com, or only read data?

It only reads. It looks things up on dropbox.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/dropbox.com/download_invoice, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/dropbox.com/download_invoice

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/dropbox.com/download_invoice
