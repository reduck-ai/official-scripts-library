# Postman: list invoices

Automatically list invoices on postman.co. List Postman billing invoices. Returns per invoice: invoiceId, date, plan, amount, status, viewUrl (public tokenized page) and pdfUrl (direct PDF endpoint). The PDF is rendered inline by Chrome rather than saved as a file, so open pdfUrl or viewUrl in a browser to keep a copy.

- Site: postman.co
- Address: `reduck/postman.co/list_invoices`
- Updated: 2026-08-26 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/postman.co/list_invoices`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/postman.co/list_invoices
```

## Input

It takes no input.

## Output

- `total` (integer, required): Number of invoices returned.
- `invoices` (array, required)

## FAQ

### What does "Postman: list invoices" do?

List Postman billing invoices. Returns per invoice: invoiceId, date, plan, amount, status, viewUrl (public tokenized page) and pdfUrl (direct PDF endpoint). The PDF is rendered inline by Chrome rather than saved as a file, so open pdfUrl or viewUrl in a browser to keep a copy.

### How do I automatically list invoices on postman.co?

Ask an AI agent connected to Reduck to run reduck/postman.co/list_invoices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/postman.co/list_invoices

### Is there a postman.co API to list invoices?

You do not need one. "Postman: list invoices" drives the real postman.co pages in a browser, so it works whether or not postman.co offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns total, invoices.

### Do I need to be logged in to postman.co?

Yes. It acts as you on postman.co: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the postman.co cookies saved by the Reduck extension.

### Does it change anything on postman.co, or only read data?

It only reads. It looks things up on postman.co and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/postman.co/list_invoices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/postman.co/list_invoices

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/postman.co/list_invoices
