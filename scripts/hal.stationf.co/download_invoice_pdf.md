# Download a Station F (HAL) invoice as PDF

Automatically download a Station F (HAL) invoice as PDF on hal.stationf.co. Download a Station F / HAL invoice (by its id from list_invoices) as a PDF, returned base64-encoded.

- Site: hal.stationf.co
- Address: `reduck/hal.stationf.co/download_invoice_pdf`
- Updated: 2026-07-31 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/hal.stationf.co/download_invoice_pdf`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/hal.stationf.co/download_invoice_pdf
```

## Input

- `invoiceId` (string, required): HAL invoice id (the 'id' field / view-URL segment from list_invoices, e.g. "6a447d38369cb4395acd3203").

## Output

- `bytes` (integer, required)
- `base64` (string, required)
- `invoiceId` (string, required)
- `head` (string, optional)

## FAQ

### What does "Download a Station F (HAL) invoice as PDF" do?

Download a Station F / HAL invoice (by its id from list_invoices) as a PDF, returned base64-encoded.

### How do I automatically download a Station F (HAL) invoice as PDF on hal.stationf.co?

Ask an AI agent connected to Reduck to run reduck/hal.stationf.co/download_invoice_pdf, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/hal.stationf.co/download_invoice_pdf

### Is there a hal.stationf.co API to download a Station F (HAL) invoice as PDF?

You do not need one. "Download a Station F (HAL) invoice as PDF" drives the real hal.stationf.co pages in a browser, so it works whether or not hal.stationf.co offers an API for this.

### What information do I need to provide?

Required: invoiceId.

### What does it return?

It returns head, bytes, base64, invoiceId.

### Do I need to be logged in to hal.stationf.co?

Yes. It acts as you on hal.stationf.co: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the hal.stationf.co cookies saved by the Reduck extension.

### Does it change anything on hal.stationf.co, or only read data?

Unknown: its author has not declared whether it changes anything on hal.stationf.co, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/hal.stationf.co/download_invoice_pdf, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/hal.stationf.co/download_invoice_pdf

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/hal.stationf.co/download_invoice_pdf
