# Download Twilio receipt

Automatically download Twilio receipt on console.twilio.com. Download the monthly payment receipt PDF of the signed-in Twilio account, by the invoiceId from list_invoices (e.g. receipt-2026-10). Returns the PDF as base64.

- Site: console.twilio.com
- Address: `reduck/console.twilio.com/download_invoice`
- Updated: 2026-10-12 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/console.twilio.com/download_invoice`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/console.twilio.com/download_invoice
```

## Input

- `invoiceId` (string, required): Receipt id from list_invoices, like receipt-2026-10 (a bare month 2026-10 also works).

## Output

- `month` (string, required)
- `filename` (string, required)
- `invoiceId` (string, required)
- `pdf_base64` (string, required)
- `size_bytes` (integer, required)
- `total` (string | null, optional)

## FAQ

### What does "Download Twilio receipt" do?

Download the monthly payment receipt PDF of the signed-in Twilio account, by the invoiceId from list_invoices (e.g. receipt-2026-10). Returns the PDF as base64.

### How do I automatically download Twilio receipt on console.twilio.com?

Ask an AI agent connected to Reduck to run reduck/console.twilio.com/download_invoice, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/console.twilio.com/download_invoice

### Is there a console.twilio.com API to download Twilio receipt?

You do not need one. "Download Twilio receipt" drives the real console.twilio.com pages in a browser, so it works whether or not console.twilio.com offers an API for this.

### What information do I need to provide?

Required: invoiceId.

### What does it return?

It returns month, total, filename, invoiceId, pdf_base64, size_bytes.

### Do I need to be logged in to console.twilio.com?

Yes. It acts as you on console.twilio.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the console.twilio.com cookies saved by the Reduck extension.

### Does it change anything on console.twilio.com, or only read data?

It only reads. It looks things up on console.twilio.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/console.twilio.com/download_invoice, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/console.twilio.com/download_invoice

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/console.twilio.com/download_invoice
