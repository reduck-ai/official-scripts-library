# Archive Pennylane supplier invoices

Automatically archive Pennylane supplier invoices on app.pennylane.com. Archive one or more supplier invoices from the Pennylane Inbox by id. With dryRun (default true) each invoice is only previewed — selected, its archive confirmation opened and the warning read, then cancelled — so nothing is archived; dryRun:false confirms the archive. Returns, per invoice, whether it was found, its label, its amount and the warning that was shown.

- Site: app.pennylane.com
- Address: `reduck/app.pennylane.com/archive_invoices`
- Updated: 2026-08-31 (v10)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/app.pennylane.com/archive_invoices`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/app.pennylane.com/archive_invoices
```

## Input

- `companyId` (integer | string, required): Pennylane company id, the number in the app URL at /companies/<id>/supplier_invoices.
- `invoiceIds` (array, required): Invoice ids (as returned by list_invoices) to archive.
- `dryRun` (boolean, optional): true (default): select row + open modal + cancel, no archive. false: confirm the archive.

## Output

- `dryRun` (boolean, optional)
- `results` (array, optional)
- `archivedCount` (number, optional)

## FAQ

### What does "Archive Pennylane supplier invoices" do?

Archive one or more supplier invoices from the Pennylane Inbox by id. With dryRun (default true) each invoice is only previewed — selected, its archive confirmation opened and the warning read, then cancelled — so nothing is archived; dryRun:false confirms the archive. Returns, per invoice, whether it was found, its label, its amount and the warning that was shown.

### How do I automatically archive Pennylane supplier invoices on app.pennylane.com?

Ask an AI agent connected to Reduck to run reduck/app.pennylane.com/archive_invoices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.pennylane.com/archive_invoices

### Is there a app.pennylane.com API to archive Pennylane supplier invoices?

You do not need one. "Archive Pennylane supplier invoices" drives the real app.pennylane.com pages in a browser, so it works whether or not app.pennylane.com offers an API for this.

### What information do I need to provide?

Required: companyId, invoiceIds. Optional: dryRun.

### What does it return?

It returns dryRun, results, archivedCount.

### Do I need to be logged in to app.pennylane.com?

Yes. It acts as you on app.pennylane.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the app.pennylane.com cookies saved by the Reduck extension.

### Does it change anything on app.pennylane.com, or only read data?

It makes changes on app.pennylane.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/app.pennylane.com/archive_invoices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.pennylane.com/archive_invoices

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/app.pennylane.com/archive_invoices
