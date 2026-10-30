# Search Pennylane suppliers

Automatically search Pennylane suppliers on app.pennylane.com. Searches a Pennylane company's suppliers by name, as the supplier field of an invoice does, one page at a time. Returns each supplier's id and name, and whether another page may follow. An empty list means no supplier matches. Use the id with app.pennylane.com/set_invoice_supplier. Fails with a sign-in error when the browser is not signed in to Pennylane.

- Site: app.pennylane.com
- Address: `reduck/app.pennylane.com/search_suppliers`
- Updated: 2026-10-29 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/app.pennylane.com/search_suppliers`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/app.pennylane.com/search_suppliers
```

## Input

- `query` (string, required): Words of the supplier name.
- `companyId` (integer | string, required): The number in the app URL at /companies/<id>/.
- `page` (integer, optional): Page, 1-indexed.
- `perPage` (integer, optional): Suppliers per page.

## Output

- `hasMore` (boolean, required): True when the page is full, so another page may follow.
- `suppliers` (array, required)

## FAQ

### What does "Search Pennylane suppliers" do?

Searches a Pennylane company's suppliers by name, as the supplier field of an invoice does, one page at a time. Returns each supplier's id and name, and whether another page may follow. An empty list means no supplier matches. Use the id with app.pennylane.com/set_invoice_supplier. Fails with a sign-in error when the browser is not signed in to Pennylane.

### How do I automatically search Pennylane suppliers on app.pennylane.com?

Ask an AI agent connected to Reduck to run reduck/app.pennylane.com/search_suppliers, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.pennylane.com/search_suppliers

### Is there a app.pennylane.com API to search Pennylane suppliers?

You do not need one. "Search Pennylane suppliers" drives the real app.pennylane.com pages in a browser, so it works whether or not app.pennylane.com offers an API for this.

### What information do I need to provide?

Required: companyId, query. Optional: page, perPage.

### What does it return?

It returns hasMore, suppliers.

### Do I need to be logged in to app.pennylane.com?

Yes. It acts as you on app.pennylane.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the app.pennylane.com cookies saved by the Reduck extension.

### Does it change anything on app.pennylane.com, or only read data?

It only reads. It looks things up on app.pennylane.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/app.pennylane.com/search_suppliers, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.pennylane.com/search_suppliers

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/app.pennylane.com/search_suppliers
