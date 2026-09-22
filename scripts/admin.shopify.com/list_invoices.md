# Shopify: list invoices

Automatically list invoices on admin.shopify.com. List a Shopify store's billing invoices — number, date, type, status, amount and invoiceUrl — for the store the signed-in account lands on. Metadata only: feed a row's invoiceUrl to admin.shopify.com/download_invoice to fetch that invoice's PDF. A store that has never been invoiced returns an empty list. Because listing no longer depends on the documents, a store whose PDFs Shopify withholds (for example one it has deactivated) still returns its full invoice list.

- Site: admin.shopify.com
- Address: `reduck/admin.shopify.com/list_invoices`
- Updated: 2026-08-21 (v9)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/admin.shopify.com/list_invoices`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/admin.shopify.com/list_invoices
```

## Input

It takes no input.

## Output

- `store` (string, required)
- `invoices` (array, required)

## FAQ

### What does "Shopify: list invoices" do?

List a Shopify store's billing invoices — number, date, type, status, amount and invoiceUrl — for the store the signed-in account lands on. Metadata only: feed a row's invoiceUrl to admin.shopify.com/download_invoice to fetch that invoice's PDF. A store that has never been invoiced returns an empty list. Because listing no longer depends on the documents, a store whose PDFs Shopify withholds (for example one it has deactivated) still returns its full invoice list.

### How do I automatically list invoices on admin.shopify.com?

Ask an AI agent connected to Reduck to run reduck/admin.shopify.com/list_invoices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/admin.shopify.com/list_invoices

### Is there a admin.shopify.com API to list invoices?

You do not need one. "Shopify: list invoices" drives the real admin.shopify.com pages in a browser, so it works whether or not admin.shopify.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns store, invoices.

### Do I need to be logged in to admin.shopify.com?

Yes. It acts as you on admin.shopify.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the admin.shopify.com cookies saved by the Reduck extension.

### Does it change anything on admin.shopify.com, or only read data?

It only reads. It looks things up on admin.shopify.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/admin.shopify.com/list_invoices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/admin.shopify.com/list_invoices

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/admin.shopify.com/list_invoices
