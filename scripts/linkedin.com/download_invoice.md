# Download LinkedIn receipt

Automatically download LinkedIn receipt on linkedin.com. Download a single LinkedIn purchase receipt PDF, matched by invoice_number (or purchase+date) from linkedin.com/list_invoices. Returns the PDF bytes as base64 plus a filename.

- Site: linkedin.com
- Address: `reduck/linkedin.com/download_invoice`
- Updated: 2026-09-29 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/download_invoice`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/download_invoice
```

## Input

- `date` (string, optional): Optional, used with purchase to disambiguate rows with the same purchase description.
- `purchase` (string, optional): Fallback matcher when invoice_number is blank: the purchase description from linkedin.com/list_invoices.
- `invoice_number` (string, optional): invoice_number from linkedin.com/list_invoices. Preferred matcher.

## Output

- `filename` (string, required)
- `contentBase64` (string, required)

## FAQ

### What does "Download LinkedIn receipt" do?

Download a single LinkedIn purchase receipt PDF, matched by invoice_number (or purchase+date) from linkedin.com/list_invoices. Returns the PDF bytes as base64 plus a filename.

### How do I automatically download LinkedIn receipt on linkedin.com?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/download_invoice, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/download_invoice

### Is there a linkedin.com API to download LinkedIn receipt?

You do not need one. "Download LinkedIn receipt" drives the real linkedin.com pages in a browser, so it works whether or not linkedin.com offers an API for this.

### What information do I need to provide?

Optional: date, purchase, invoice_number.

### What does it return?

It returns filename, contentBase64.

### Do I need to be logged in to linkedin.com?

Yes. It acts as you on linkedin.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linkedin.com cookies saved by the Reduck extension.

### Does it change anything on linkedin.com, or only read data?

It only reads. It looks things up on linkedin.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/download_invoice, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/download_invoice

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/download_invoice
