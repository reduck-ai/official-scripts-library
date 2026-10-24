# Notion unofficial API: download a Notion invoice PDF

Automatically download a Notion invoice PDF on app.notion.com. Download a Notion invoice as a PDF, given its hosted_invoice_url from app.notion.com/list_invoices. Notion does not email invoice PDFs. Saves the PDF and returns where it was saved: path (or url when the file is not on the computer running the browser), filename and size. Requires being signed in to the Notion account that owns the invoice.

- Site: app.notion.com
- Address: `reduck/app.notion.com/download_invoice_pdf`
- Updated: 2026-10-23 (v6)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/app.notion.com/download_invoice_pdf`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/app.notion.com/download_invoice_pdf
```

## Input

- `hosted_invoice_url` (string, required): The hosted_invoice_url from list_invoices (https://app.notion.com/invoice/in_...).

## Output

- `filename` (string, required): Name of the saved file, derived from the invoice id (e.g. Notion-in_1TgQCpCcKlYJxALV0wxPYyNd.pdf); it can carry a numbered suffix when a file of that name was already there.
- `size_bytes` (integer, required)
- `url` (string | null, optional): A link to the PDF, when it is not saved on the computer running the browser.
- `path` (string | null, optional): Where the PDF was saved on the computer running the browser.

## FAQ

### What does "Notion unofficial API: download a Notion invoice PDF" do?

Download a Notion invoice as a PDF, given its hosted_invoice_url from app.notion.com/list_invoices. Notion does not email invoice PDFs. Saves the PDF and returns where it was saved: path (or url when the file is not on the computer running the browser), filename and size. Requires being signed in to the Notion account that owns the invoice.

### How do I automatically download a Notion invoice PDF on app.notion.com?

Ask an AI agent connected to Reduck to run reduck/app.notion.com/download_invoice_pdf, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.notion.com/download_invoice_pdf

### Is there a app.notion.com API to download a Notion invoice PDF?

You do not need one. "Notion unofficial API: download a Notion invoice PDF" drives the real app.notion.com pages in a browser, so it works whether or not app.notion.com offers an API for this.

### What information do I need to provide?

Required: hosted_invoice_url.

### What does it return?

It returns url, path, filename, size_bytes.

### Do I need to be logged in to app.notion.com?

Yes. It acts as you on app.notion.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the app.notion.com cookies saved by the Reduck extension.

### Does it change anything on app.notion.com, or only read data?

It only reads. It looks things up on app.notion.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/app.notion.com/download_invoice_pdf, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.notion.com/download_invoice_pdf

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/app.notion.com/download_invoice_pdf
