# Download a Google Payments invoice (Google One, YouTube, Google Play)

Automatically download a Google Payments invoice (Google One, YouTube, Google Play) on pay.google.com. Download the invoice PDF of one Google charge, such as a Google One or Google AI plan, YouTube Premium, or a Google Play purchase (pay.google.com > Activity > Transaction details > Download tax invoice). Pass the row's transaction label as returned by pay.google.com/list_transactions (e.g. "12 Mar · 100 GB (Google One)"); the first (newest) matching row wins. Returns Google's filename and the path where the browser saved the PDF (or a url to it on a managed browser), so you can read or move it directly.

- Site: pay.google.com
- Address: `reduck/pay.google.com/download_tax_invoice`
- Updated: 2026-10-06 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/pay.google.com/download_tax_invoice`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/pay.google.com/download_tax_invoice
```

## Input

- `transaction` (string, required): The row's transaction label as list_transactions returns it, e.g. "12 Mar · 100 GB (Google One)". The first (newest) row containing it is used.

## Output

- `filename` (string, required): Google's own filename for the invoice (e.g. 1234567890123456-9.pdf).
- `url` (string, optional): On a managed browser, a link to the PDF bytes (the file is not on your machine).
- `path` (string, optional): Where the PDF is saved on the machine running the browser (on a paired Chrome, its downloads folder). Read or move the file from there.

## FAQ

### What does "Download a Google Payments invoice (Google One, YouTube, Google Play)" do?

Download the invoice PDF of one Google charge, such as a Google One or Google AI plan, YouTube Premium, or a Google Play purchase (pay.google.com > Activity > Transaction details > Download tax invoice). Pass the row's transaction label as returned by pay.google.com/list_transactions (e.g. "12 Mar · 100 GB (Google One)"); the first (newest) matching row wins. Returns Google's filename and the path where the browser saved the PDF (or a url to it on a managed browser), so you can read or move it directly.

### How do I automatically download a Google Payments invoice (Google One, YouTube, Google Play) on pay.google.com?

Ask an AI agent connected to Reduck to run reduck/pay.google.com/download_tax_invoice, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/pay.google.com/download_tax_invoice

### Is there a pay.google.com API to download a Google Payments invoice (Google One, YouTube, Google Play)?

You do not need one. "Download a Google Payments invoice (Google One, YouTube, Google Play)" drives the real pay.google.com pages in a browser, so it works whether or not pay.google.com offers an API for this.

### What information do I need to provide?

Required: transaction.

### What does it return?

It returns url, path, filename.

### Do I need to be logged in to pay.google.com?

Yes. It acts as you on pay.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the pay.google.com cookies saved by the Reduck extension.

### Does it change anything on pay.google.com, or only read data?

It only reads. It looks things up on pay.google.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/pay.google.com/download_tax_invoice, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/pay.google.com/download_tax_invoice

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/pay.google.com/download_tax_invoice
