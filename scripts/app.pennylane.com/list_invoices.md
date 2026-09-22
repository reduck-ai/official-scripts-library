# List supplier invoices

Automatically list supplier invoices on app.pennylane.com. Lists Pennylane supplier invoices from one tab (All / Inbox / To pay / Paid / To approve). Returns each invoice's id, provider (best-effort, parsed from the site-generated label), invoice number, dates, amount/currency, payment status and paid flag. Requires companyId (the number in the app URL at /companies/<id>/supplier_invoices); defaults to the Inbox tab, the invoices needing reconciliation.

- Site: app.pennylane.com
- Address: `reduck/app.pennylane.com/list_invoices`
- Updated: 2026-08-31 (v6)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/app.pennylane.com/list_invoices`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/app.pennylane.com/list_invoices
```

## Input

- `companyId` (integer | string, required): Pennylane company id, the number in the app URL at /companies/<id>/supplier_invoices.
- `page` (integer, optional): Page number, 1-indexed. Defaults to 1.
- `perPage` (integer, optional): Rows per page. Defaults to 50.

## Output

- `invoices` (array, required)
- `pagination` (object, required)

## FAQ

### What does "List supplier invoices" do?

Lists Pennylane supplier invoices from one tab (All / Inbox / To pay / Paid / To approve). Returns each invoice's id, provider (best-effort, parsed from the site-generated label), invoice number, dates, amount/currency, payment status and paid flag. Requires companyId (the number in the app URL at /companies/<id>/supplier_invoices); defaults to the Inbox tab, the invoices needing reconciliation.

### How do I automatically list supplier invoices on app.pennylane.com?

Ask an AI agent connected to Reduck to run reduck/app.pennylane.com/list_invoices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.pennylane.com/list_invoices

### Is there a app.pennylane.com API to list supplier invoices?

You do not need one. "List supplier invoices" drives the real app.pennylane.com pages in a browser, so it works whether or not app.pennylane.com offers an API for this.

### What information do I need to provide?

Required: companyId. Optional: page, perPage.

### What does it return?

It returns invoices, pagination.

### Do I need to be logged in to app.pennylane.com?

Yes. It acts as you on app.pennylane.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the app.pennylane.com cookies saved by the Reduck extension.

### Does it change anything on app.pennylane.com, or only read data?

It only reads. It looks things up on app.pennylane.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/app.pennylane.com/list_invoices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.pennylane.com/list_invoices

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/app.pennylane.com/list_invoices
