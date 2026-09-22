# List Asana invoices

Automatically list Asana invoices on asana.com. List all Asana invoices from the admin billing panel. Returns each invoice's date, invoiceNumber, amount, currency, status, and a temporary download link. Needs an account with billing access; without it the "Invoice history" affordance is absent and the script raises an error rather than returning an empty list.

- Site: asana.com
- Address: `reduck/asana.com/list_invoices`
- Updated: 2026-08-20 (v11)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/asana.com/list_invoices`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/asana.com/list_invoices
```

## Input

It takes no input.

## Output

- `total` (integer, required)
- `invoices` (array, required)

## FAQ

### What does "List Asana invoices" do?

List all Asana invoices from the admin billing panel. Returns each invoice's date, invoiceNumber, amount, currency, status, and a temporary download link. Needs an account with billing access; without it the "Invoice history" affordance is absent and the script raises an error rather than returning an empty list.

### How do I automatically list Asana invoices on asana.com?

Ask an AI agent connected to Reduck to run reduck/asana.com/list_invoices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/asana.com/list_invoices

### Is there a asana.com API to list Asana invoices?

You do not need one. "List Asana invoices" drives the real asana.com pages in a browser, so it works whether or not asana.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns total, invoices.

### Do I need to be logged in to asana.com?

Yes. It acts as you on asana.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the asana.com cookies saved by the Reduck extension.

### Does it change anything on asana.com, or only read data?

It only reads. It looks things up on asana.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/asana.com/list_invoices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/asana.com/list_invoices

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/asana.com/list_invoices
