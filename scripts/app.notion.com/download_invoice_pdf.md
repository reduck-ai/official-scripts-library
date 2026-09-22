# Download Notion invoice PDF

Automatically download Notion invoice PDF on app.notion.com. Download a Notion-hosted invoice as a PDF from its hosted_invoice_url (from list_invoices). Renders the page and returns the PDF bytes as base64 (decode + write it yourself) plus a filename — the script is sandboxed and can't write to disk directly.

- Site: app.notion.com
- Address: `reduck/app.notion.com/download_invoice_pdf`
- Updated: 2026-08-24 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/app.notion.com/download_invoice_pdf`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/app.notion.com/download_invoice_pdf
```

## Input

- `hosted_invoice_url` (string, required): The hosted_invoice_url from list_invoices (https://app.notion.com/invoice/in_...).

## Output

- `filename` (string, required): A filename derived from the invoice id in hosted_invoice_url (e.g. Notion-in_1TgQCpCcKlYJxALV0wxPYyNd.pdf).
- `pdf_base64` (string, required): The PDF file bytes, base64-encoded. Decode and write to a .pdf file at a location of your choosing.
- `size_bytes` (integer, required)

## FAQ

### What does "Download Notion invoice PDF" do?

Download a Notion-hosted invoice as a PDF from its hosted_invoice_url (from list_invoices). Renders the page and returns the PDF bytes as base64 (decode + write it yourself) plus a filename — the script is sandboxed and can't write to disk directly.

### How do I automatically download Notion invoice PDF on app.notion.com?

Ask an AI agent connected to Reduck to run reduck/app.notion.com/download_invoice_pdf, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.notion.com/download_invoice_pdf

### Is there a app.notion.com API to download Notion invoice PDF?

You do not need one. "Download Notion invoice PDF" drives the real app.notion.com pages in a browser, so it works whether or not app.notion.com offers an API for this.

### What information do I need to provide?

Required: hosted_invoice_url.

### What does it return?

It returns filename, pdf_base64, size_bytes.

### Do I need to be logged in to app.notion.com?

Yes. It acts as you on app.notion.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the app.notion.com cookies saved by the Reduck extension.

### Does it change anything on app.notion.com, or only read data?

It only reads. It looks things up on app.notion.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/app.notion.com/download_invoice_pdf, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.notion.com/download_invoice_pdf

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/app.notion.com/download_invoice_pdf
