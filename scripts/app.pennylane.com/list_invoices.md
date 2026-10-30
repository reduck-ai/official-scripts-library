# List Pennylane supplier invoices

Automatically list Pennylane supplier invoices on app.pennylane.com. Lists a Pennylane company's supplier invoices, one tab and one page at a time, in the order the page shows them (newest added first). Tabs are all, inbox, to pay, paid, to approve, in dispute, and archived for the archived invoices; search narrows the list by invoice number, as the page's search box does. Returns each invoice's id, label, supplier, invoice number, date, creation date, deadline, amount in the invoice currency and in euros, invoice and payment status, and paid flag, plus paging totals (use hasNextPage to ask for the next page). An account that only sees its own invoices gets that single list without tabs or search. Requires companyId, the number in the app URL at /companies/<id>/. Fails with a sign-in error when the browser is not signed in to Pennylane.

- Site: app.pennylane.com
- Address: `reduck/app.pennylane.com/list_invoices`
- Updated: 2026-10-29 (v10)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/app.pennylane.com/list_invoices`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/app.pennylane.com/list_invoices
```

## Input

- `companyId` (integer | string, required): Pennylane company id, the number in the app URL at /companies/<id>/supplier_invoices.
- `tab` (string, optional): Tab of the supplier invoices page to list; archived lists the archived invoices. An account that only sees its own invoices has no tabs and takes only all.
- `page` (integer, optional): Page number, 1-indexed.
- `search` (string, optional): Words of the invoice number, as typed in the page's search box.
- `perPage` (integer, optional): Rows per page.

## Output

- `invoices` (array, required)
- `pagination` (object, required)
- `view` (string, optional): company: the supplier invoices page with tabs. own: an account that only sees its own invoices.

## FAQ

### What does "List Pennylane supplier invoices" do?

Lists a Pennylane company's supplier invoices, one tab and one page at a time, in the order the page shows them (newest added first). Tabs are all, inbox, to pay, paid, to approve, in dispute, and archived for the archived invoices; search narrows the list by invoice number, as the page's search box does. Returns each invoice's id, label, supplier, invoice number, date, creation date, deadline, amount in the invoice currency and in euros, invoice and payment status, and paid flag, plus paging totals (use hasNextPage to ask for the next page). An account that only sees its own invoices gets that single list without tabs or search. Requires companyId, the number in the app URL at /companies/<id>/. Fails with a sign-in error when the browser is not signed in to Pennylane.

### How do I automatically list Pennylane supplier invoices on app.pennylane.com?

Ask an AI agent connected to Reduck to run reduck/app.pennylane.com/list_invoices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.pennylane.com/list_invoices

### Is there a app.pennylane.com API to list Pennylane supplier invoices?

You do not need one. "List Pennylane supplier invoices" drives the real app.pennylane.com pages in a browser, so it works whether or not app.pennylane.com offers an API for this.

### What information do I need to provide?

Required: companyId. Optional: tab, page, search, perPage.

### What does it return?

It returns view, invoices, pagination.

### Do I need to be logged in to app.pennylane.com?

Yes. It acts as you on app.pennylane.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the app.pennylane.com cookies saved by the Reduck extension.

### Does it change anything on app.pennylane.com, or only read data?

It only reads. It looks things up on app.pennylane.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/app.pennylane.com/list_invoices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.pennylane.com/list_invoices

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/app.pennylane.com/list_invoices
