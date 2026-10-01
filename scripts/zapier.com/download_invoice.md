# Download Zapier invoice

Automatically download Zapier invoice on zapier.com. Download a single Zapier invoice as a PDF, given its href from zapier.com/list_invoices. Returns the PDF bytes as base64 plus a filename.

- Site: zapier.com
- Address: `reduck/zapier.com/download_invoice`
- Updated: 2026-09-30 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/zapier.com/download_invoice`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/zapier.com/download_invoice
```

## Input

- `href` (string, required): Invoice detail page href from zapier.com/list_invoices.

## Output

- `filename` (string, required)
- `contentBase64` (string, required)

## FAQ

### What does "Download Zapier invoice" do?

Download a single Zapier invoice as a PDF, given its href from zapier.com/list_invoices. Returns the PDF bytes as base64 plus a filename.

### How do I automatically download Zapier invoice on zapier.com?

Ask an AI agent connected to Reduck to run reduck/zapier.com/download_invoice, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/zapier.com/download_invoice

### Is there a zapier.com API to download Zapier invoice?

You do not need one. "Download Zapier invoice" drives the real zapier.com pages in a browser, so it works whether or not zapier.com offers an API for this.

### What information do I need to provide?

Required: href.

### What does it return?

It returns filename, contentBase64.

### Do I need to be logged in to zapier.com?

Yes. It acts as you on zapier.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the zapier.com cookies saved by the Reduck extension.

### Does it change anything on zapier.com, or only read data?

It only reads. It looks things up on zapier.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/zapier.com/download_invoice, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/zapier.com/download_invoice

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/zapier.com/download_invoice
