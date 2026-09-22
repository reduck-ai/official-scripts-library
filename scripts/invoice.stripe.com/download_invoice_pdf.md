# Download Stripe invoice/receipt PDF

Automatically download Stripe invoice/receipt PDF on invoice.stripe.com. Download a Stripe-hosted invoice or payment receipt PDF from its hosted_invoice_url. Returns the PDF bytes as base64 (decode + write it yourself) plus the real filename. Vendor-agnostic and login-free: the hosted_invoice_url is a public tokenized link, so it works for any Stripe-billed service (Claude, ChatGPT, Notion, Slack, Lovable, ...). An expired or dead URL fails cleanly.

- Site: invoice.stripe.com
- Address: `reduck/invoice.stripe.com/download_invoice_pdf`
- Updated: 2026-08-20 (v5)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/invoice.stripe.com/download_invoice_pdf`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/invoice.stripe.com/download_invoice_pdf
```

## Input

- `hosted_invoice_url` (string, required): A Stripe-related invoice URL from a vendor's list_invoices script -- any of: a Stripe hosted invoice page (invoice.stripe.com/i/...), an HTML receipt page with Download invoice/receipt links (e.g. pay.stripe.com/receipts/invoices/...), or a direct file URL that downloads immediately (pay.stripe.com/invoice/.../pdf, a presigned S3/Orb link). The script detects which shape it is from the page itself.
- `doc_type` (string, optional): Which PDF to download: 'invoice' (the formal invoice, default) or 'receipt' (the payment receipt, only present once paid). For a direct-file-URL page there is only ever one document available -- requesting the one that isn't there fails loud rather than silently returning the wrong one mislabeled.

## Output

- `doc_type` (string, required): Which document was downloaded: invoice or receipt.
- `filename` (string, required): The real suggested filename (e.g. Invoice-V1L1VMU8-0001.pdf or Receipt-2415-5423.pdf), taken from the file's Content-Disposition.
- `pdf_base64` (string, required): The PDF file bytes, base64-encoded. Decode and write to a .pdf file at a location of your choosing (the script is sandboxed and cannot write to disk itself).

## FAQ

### What does "Download Stripe invoice/receipt PDF" do?

Download a Stripe-hosted invoice or payment receipt PDF from its hosted_invoice_url. Returns the PDF bytes as base64 (decode + write it yourself) plus the real filename. Vendor-agnostic and login-free: the hosted_invoice_url is a public tokenized link, so it works for any Stripe-billed service (Claude, ChatGPT, Notion, Slack, Lovable, ...). An expired or dead URL fails cleanly.

### How do I automatically download Stripe invoice/receipt PDF on invoice.stripe.com?

Ask an AI agent connected to Reduck to run reduck/invoice.stripe.com/download_invoice_pdf, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/invoice.stripe.com/download_invoice_pdf

### Is there a invoice.stripe.com API to download Stripe invoice/receipt PDF?

You do not need one. "Download Stripe invoice/receipt PDF" drives the real invoice.stripe.com pages in a browser, so it works whether or not invoice.stripe.com offers an API for this.

### What information do I need to provide?

Required: hosted_invoice_url. Optional: doc_type.

### What does it return?

It returns doc_type, filename, pdf_base64.

### Do I need to be logged in to invoice.stripe.com?

No. It only uses pages of invoice.stripe.com that are reachable without signing in.

### Does it change anything on invoice.stripe.com, or only read data?

It only reads. It looks things up on invoice.stripe.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/invoice.stripe.com/download_invoice_pdf, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/invoice.stripe.com/download_invoice_pdf

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/invoice.stripe.com/download_invoice_pdf
