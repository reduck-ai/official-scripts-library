# Download Surfshark receipt

Automatically download Surfshark receipt on surfshark.com. Download a single Surfshark payment receipt PDF by order id (from surfshark.com/list_invoices). Returns the PDF bytes as base64 plus a filename.

- Site: surfshark.com
- Address: `reduck/surfshark.com/download_invoice`
- Updated: 2026-09-29 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/surfshark.com/download_invoice`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/surfshark.com/download_invoice
```

## Input

- `id` (string, required): Order id from surfshark.com/list_invoices.

## Output

- `filename` (string, required)
- `contentBase64` (string, required)

## FAQ

### What does "Download Surfshark receipt" do?

Download a single Surfshark payment receipt PDF by order id (from surfshark.com/list_invoices). Returns the PDF bytes as base64 plus a filename.

### How do I automatically download Surfshark receipt on surfshark.com?

Ask an AI agent connected to Reduck to run reduck/surfshark.com/download_invoice, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/surfshark.com/download_invoice

### Is there a surfshark.com API to download Surfshark receipt?

You do not need one. "Download Surfshark receipt" drives the real surfshark.com pages in a browser, so it works whether or not surfshark.com offers an API for this.

### What information do I need to provide?

Required: id.

### What does it return?

It returns filename, contentBase64.

### Do I need to be logged in to surfshark.com?

Yes. It acts as you on surfshark.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the surfshark.com cookies saved by the Reduck extension.

### Does it change anything on surfshark.com, or only read data?

It only reads. It looks things up on surfshark.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/surfshark.com/download_invoice, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/surfshark.com/download_invoice

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/surfshark.com/download_invoice
