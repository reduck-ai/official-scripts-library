# Download a Shopify invoice PDF

Automatically download a Shopify invoice PDF on admin.shopify.com. Download one Shopify store invoice PDF, given the invoiceUrl (or number) that admin.shopify.com/list_invoices returns. Exports the invoice as PDF from its billing page and saves the file under Shopify's own filename, returning where the browser saved it (or a link to it on a managed browser). Fails with a clear message when the invoice has no export or Shopify issues no PDF for it.

- Site: admin.shopify.com
- Address: `reduck/admin.shopify.com/download_invoice`
- Updated: 2026-10-09 (v11)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/admin.shopify.com/download_invoice`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/admin.shopify.com/download_invoice
```

## Input

- `store` (string, optional): The store handle (e.g. 0qknc0-kx), as returned in list_invoices' store field. Optional: discovered from the signed-in admin when omitted, and ignored when invoiceUrl is given.
- `number` (string, optional): The invoice number from admin.shopify.com/list_invoices. Required unless invoiceUrl is given.
- `invoiceUrl` (string, optional): The row's invoiceUrl exactly as returned by admin.shopify.com/list_invoices. Preferred — both store and number are read from it.

## Output

- `via` (string, required): How the file was obtained: the signed document link Shopify issues from the invoice page's PDF export, downloaded by the browser.
- `number` (string, required)
- `filename` (string, required): Shopify's own filename for the invoice PDF (e.g. invoice_596948484_2.pdf).
- `url` (string | null, optional): On a managed browser, a link to the PDF bytes (the file is not on the browser's machine); null otherwise.
- `path` (string | null, optional): Where the PDF was saved on the machine running the browser; null on a managed browser.

## FAQ

### What does "Download a Shopify invoice PDF" do?

Download one Shopify store invoice PDF, given the invoiceUrl (or number) that admin.shopify.com/list_invoices returns. Exports the invoice as PDF from its billing page and saves the file under Shopify's own filename, returning where the browser saved it (or a link to it on a managed browser). Fails with a clear message when the invoice has no export or Shopify issues no PDF for it.

### How do I automatically download a Shopify invoice PDF on admin.shopify.com?

Ask an AI agent connected to Reduck to run reduck/admin.shopify.com/download_invoice, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/admin.shopify.com/download_invoice

### Is there a admin.shopify.com API to download a Shopify invoice PDF?

You do not need one. "Download a Shopify invoice PDF" drives the real admin.shopify.com pages in a browser, so it works whether or not admin.shopify.com offers an API for this.

### What information do I need to provide?

Optional: store, number, invoiceUrl.

### What does it return?

It returns url, via, path, number, filename.

### Do I need to be logged in to admin.shopify.com?

Yes. It acts as you on admin.shopify.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the admin.shopify.com cookies saved by the Reduck extension.

### Does it change anything on admin.shopify.com, or only read data?

It only reads. It looks things up on admin.shopify.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/admin.shopify.com/download_invoice, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/admin.shopify.com/download_invoice

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/admin.shopify.com/download_invoice
