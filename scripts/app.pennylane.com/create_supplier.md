# Create a Pennylane supplier

Automatically create a Pennylane supplier on app.pennylane.com. Creates a supplier in a Pennylane company, by name, and returns its id and name. It does not check for an existing supplier with the same name: search first with app.pennylane.com/search_suppliers to avoid a duplicate. Use the id with app.pennylane.com/set_invoice_supplier. Fails with a sign-in error when the browser is not signed in to Pennylane.

- Site: app.pennylane.com
- Address: `reduck/app.pennylane.com/create_supplier`
- Updated: 2026-10-29 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/app.pennylane.com/create_supplier`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/app.pennylane.com/create_supplier
```

## Input

- `name` (string, required): Supplier name, as it should appear in Pennylane.
- `companyId` (integer | string, required): The number in the app URL at /companies/<id>/.

## Output

- `supplier` (object, required)

## FAQ

### What does "Create a Pennylane supplier" do?

Creates a supplier in a Pennylane company, by name, and returns its id and name. It does not check for an existing supplier with the same name: search first with app.pennylane.com/search_suppliers to avoid a duplicate. Use the id with app.pennylane.com/set_invoice_supplier. Fails with a sign-in error when the browser is not signed in to Pennylane.

### How do I automatically create a Pennylane supplier on app.pennylane.com?

Ask an AI agent connected to Reduck to run reduck/app.pennylane.com/create_supplier, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.pennylane.com/create_supplier

### Is there a app.pennylane.com API to create a Pennylane supplier?

You do not need one. "Create a Pennylane supplier" drives the real app.pennylane.com pages in a browser, so it works whether or not app.pennylane.com offers an API for this.

### What information do I need to provide?

Required: companyId, name.

### What does it return?

It returns supplier.

### Do I need to be logged in to app.pennylane.com?

Yes. It acts as you on app.pennylane.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the app.pennylane.com cookies saved by the Reduck extension.

### Does it change anything on app.pennylane.com, or only read data?

It makes changes on app.pennylane.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/app.pennylane.com/create_supplier, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.pennylane.com/create_supplier

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/app.pennylane.com/create_supplier
