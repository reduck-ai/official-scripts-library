# Download Hostinger invoice

Automatically download Hostinger invoice on hostinger.com. Download a single Hostinger (hPanel) invoice PDF by paymentSlug (from hostinger.com/list_invoices). Returns the PDF bytes as base64 plus a filename.

- Site: hostinger.com
- Address: `reduck/hostinger.com/download_invoice`
- Updated: 2026-09-29 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/hostinger.com/download_invoice`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/hostinger.com/download_invoice
```

## Input

- `paymentSlug` (string, required): paymentSlug from hostinger.com/list_invoices.
- `invoice_id` (string, optional): Optional invoice_id from hostinger.com/list_invoices, used only to name the file.

## Output

- `filename` (string, required)
- `contentBase64` (string, required)

## FAQ

### What does "Download Hostinger invoice" do?

Download a single Hostinger (hPanel) invoice PDF by paymentSlug (from hostinger.com/list_invoices). Returns the PDF bytes as base64 plus a filename.

### How do I automatically download Hostinger invoice on hostinger.com?

Ask an AI agent connected to Reduck to run reduck/hostinger.com/download_invoice, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/hostinger.com/download_invoice

### Is there a hostinger.com API to download Hostinger invoice?

You do not need one. "Download Hostinger invoice" drives the real hostinger.com pages in a browser, so it works whether or not hostinger.com offers an API for this.

### What information do I need to provide?

Required: paymentSlug. Optional: invoice_id.

### What does it return?

It returns filename, contentBase64.

### Do I need to be logged in to hostinger.com?

Yes. It acts as you on hostinger.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the hostinger.com cookies saved by the Reduck extension.

### Does it change anything on hostinger.com, or only read data?

It only reads. It looks things up on hostinger.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/hostinger.com/download_invoice, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/hostinger.com/download_invoice

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/hostinger.com/download_invoice
