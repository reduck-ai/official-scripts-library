# Download Stripe invoice/receipt PDF

Automatically download Stripe invoice/receipt PDF on invoice.stripe.com. Download a Stripe-hosted invoice or payment receipt PDF from its hosted_invoice_url. Returns the file's real name and the path where the browser saved it (or a url to it on a managed browser), so you can read or move the PDF directly. Vendor-agnostic and login-free: the hosted_invoice_url is a public tokenized link, so it works for any Stripe-billed service (Claude, ChatGPT, X, Notion, Slack, Lovable, ...). An expired or dead URL fails cleanly.

- Site: invoice.stripe.com
- Address: `reduck/invoice.stripe.com/download_invoice_pdf`
- Updated: 2026-09-26 (v6)
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
- `filename` (string, required): The file's name as Stripe serves it (e.g. Invoice-V1L1VMU8-0001.pdf or Receipt-2415-5423.pdf).
- `url` (string, optional): On a managed browser, a link to the PDF bytes (the file is not on your machine).
- `path` (string, optional): Where the PDF is saved on the machine running the browser (on a paired Chrome, its downloads folder). Read or move the file from there.

## FAQ

### What does "Download Stripe invoice/receipt PDF" do?

Download a Stripe-hosted invoice or payment receipt PDF from its hosted_invoice_url. Returns the file's real name and the path where the browser saved it (or a url to it on a managed browser), so you can read or move the PDF directly. Vendor-agnostic and login-free: the hosted_invoice_url is a public tokenized link, so it works for any Stripe-billed service (Claude, ChatGPT, X, Notion, Slack, Lovable, ...). An expired or dead URL fails cleanly.

### How do I automatically download Stripe invoice/receipt PDF on invoice.stripe.com?

Ask an AI agent connected to Reduck to run reduck/invoice.stripe.com/download_invoice_pdf, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/invoice.stripe.com/download_invoice_pdf

### Is there a invoice.stripe.com API to download Stripe invoice/receipt PDF?

You do not need one. "Download Stripe invoice/receipt PDF" drives the real invoice.stripe.com pages in a browser, so it works whether or not invoice.stripe.com offers an API for this.

### What information do I need to provide?

Required: hosted_invoice_url. Optional: doc_type.

### What does it return?

It returns url, path, doc_type, filename.

### Do I need to be logged in to invoice.stripe.com?

No. It only uses pages of invoice.stripe.com that are reachable without signing in.

### Does it change anything on invoice.stripe.com, or only read data?

It only reads. It looks things up on invoice.stripe.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/invoice.stripe.com/download_invoice_pdf, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/invoice.stripe.com/download_invoice_pdf

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/invoice.stripe.com/download_invoice_pdf
