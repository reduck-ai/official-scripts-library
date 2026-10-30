# Set the supplier of a Pennylane supplier invoice

Automatically set the supplier of a Pennylane supplier invoice on app.pennylane.com. Sets which supplier a Pennylane supplier invoice belongs to, by supplier id. An invoice with no supplier cannot be approved, and one grouped with its bank transaction is matched once it has the right supplier. With dryRun (default true) it only reads the invoice and the supplier and returns both. Returns the invoice's supplier before and after. Find the supplier id with app.pennylane.com/search_suppliers, or create one with app.pennylane.com/create_supplier. Fails when the invoice or the supplier does not exist, and when signed out of Pennylane.

- Site: app.pennylane.com
- Address: `reduck/app.pennylane.com/set_invoice_supplier`
- Updated: 2026-10-29 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/app.pennylane.com/set_invoice_supplier`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/app.pennylane.com/set_invoice_supplier
```

## Input

- `companyId` (integer | string, required): The number in the app URL at /companies/<id>/.
- `invoiceId` (integer | string, required): Supplier invoice id, as app.pennylane.com/list_invoices returns it.
- `supplierId` (integer | string, required): Supplier id, as app.pennylane.com/search_suppliers or app.pennylane.com/create_supplier returns it.
- `dryRun` (boolean, optional): true (default): read the invoice and the supplier without changing anything. false: set the supplier.

## Output

- `dryRun` (boolean, required)
- `updated` (boolean, required)
- `invoiceId` (string, required)
- `label` (string | null, optional)
- `amount` (number | null, optional)
- `supplierAfter` (string | null, optional): Supplier name after the run, as read back from Pennylane.
- `supplierBefore` (string | null, optional): Supplier name before the run, null when there was none.

## FAQ

### What does "Set the supplier of a Pennylane supplier invoice" do?

Sets which supplier a Pennylane supplier invoice belongs to, by supplier id. An invoice with no supplier cannot be approved, and one grouped with its bank transaction is matched once it has the right supplier. With dryRun (default true) it only reads the invoice and the supplier and returns both. Returns the invoice's supplier before and after. Find the supplier id with app.pennylane.com/search_suppliers, or create one with app.pennylane.com/create_supplier. Fails when the invoice or the supplier does not exist, and when signed out of Pennylane.

### How do I automatically set the supplier of a Pennylane supplier invoice on app.pennylane.com?

Ask an AI agent connected to Reduck to run reduck/app.pennylane.com/set_invoice_supplier, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.pennylane.com/set_invoice_supplier

### Is there a app.pennylane.com API to set the supplier of a Pennylane supplier invoice?

You do not need one. "Set the supplier of a Pennylane supplier invoice" drives the real app.pennylane.com pages in a browser, so it works whether or not app.pennylane.com offers an API for this.

### What information do I need to provide?

Required: companyId, invoiceId, supplierId. Optional: dryRun.

### What does it return?

It returns label, amount, dryRun, updated, invoiceId, supplierAfter, supplierBefore.

### Do I need to be logged in to app.pennylane.com?

Yes. It acts as you on app.pennylane.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the app.pennylane.com cookies saved by the Reduck extension.

### Does it change anything on app.pennylane.com, or only read data?

It makes changes on app.pennylane.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/app.pennylane.com/set_invoice_supplier, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.pennylane.com/set_invoice_supplier

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/app.pennylane.com/set_invoice_supplier
