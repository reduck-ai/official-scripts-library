# Download Cloudflare invoice/receipt

Automatically download Cloudflare invoice/receipt on cloudflare.com. Download a single Cloudflare billing-history entry's PDF by accountId + invoiceId (from cloudflare.com/list_invoices). Returns the PDF bytes as base64 plus a filename.

- Site: cloudflare.com
- Address: `reduck/cloudflare.com/download_invoice`
- Updated: 2026-08-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/cloudflare.com/download_invoice`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/cloudflare.com/download_invoice
```

## Input

- `accountId` (string, required): 32-char account id from cloudflare.com/list_invoices.
- `invoiceId` (string, required): Billing-history entry UUID from cloudflare.com/list_invoices.
- `type` (string, optional): The entry's `type` field from cloudflare.com/list_invoices, e.g. "invoice". Defaults to "invoice" if omitted.

## Output

- `filename` (string, required)
- `contentBase64` (string, required)

## FAQ

### What does "Download Cloudflare invoice/receipt" do?

Download a single Cloudflare billing-history entry's PDF by accountId + invoiceId (from cloudflare.com/list_invoices). Returns the PDF bytes as base64 plus a filename.

### How do I automatically download Cloudflare invoice/receipt on cloudflare.com?

Ask an AI agent connected to Reduck to run reduck/cloudflare.com/download_invoice, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/cloudflare.com/download_invoice

### Is there a cloudflare.com API to download Cloudflare invoice/receipt?

You do not need one. "Download Cloudflare invoice/receipt" drives the real cloudflare.com pages in a browser, so it works whether or not cloudflare.com offers an API for this.

### What information do I need to provide?

Required: accountId, invoiceId. Optional: type.

### What does it return?

It returns filename, contentBase64.

### Do I need to be logged in to cloudflare.com?

Yes. It acts as you on cloudflare.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the cloudflare.com cookies saved by the Reduck extension.

### Does it change anything on cloudflare.com, or only read data?

It only reads. It looks things up on cloudflare.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/cloudflare.com/download_invoice, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/cloudflare.com/download_invoice

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/cloudflare.com/download_invoice
