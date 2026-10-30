# Restore archived Pennylane supplier invoices

Restores one or more archived Pennylane supplier invoices by id, so they show again in their tab. With dryRun (default true) each invoice is found and selected among the archived invoices, but not restored. With dryRun false it is restored, then read back. Returns, per invoice, whether it was found, its label and amount, whether it was restored, and a warning when it is not archived or shares its number or amount with too many archived invoices to be singled out. Fails with a sign-in error when the browser is not signed in to Pennylane.

- Site: app.pennylane.com
- Address: `reduck/app.pennylane.com/unarchive_invoices`
- Updated: 2026-10-29 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/app.pennylane.com/unarchive_invoices`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/app.pennylane.com/unarchive_invoices
```

## Input

- `companyId` (integer | string, required): Pennylane company id, the number in the app URL at /companies/<id>/supplier_invoices.
- `invoiceIds` (array, required): Archived invoice ids, as app.pennylane.com/list_invoices returns them with tab archived.
- `dryRun` (boolean, optional): true (default): find and select each invoice without restoring it. false: restore.

## Output

- `dryRun` (boolean, required)
- `results` (array, required)
- `restoredCount` (number, required)

## FAQ

### What does "Restore archived Pennylane supplier invoices" do?

Restores one or more archived Pennylane supplier invoices by id, so they show again in their tab. With dryRun (default true) each invoice is found and selected among the archived invoices, but not restored. With dryRun false it is restored, then read back. Returns, per invoice, whether it was found, its label and amount, whether it was restored, and a warning when it is not archived or shares its number or amount with too many archived invoices to be singled out. Fails with a sign-in error when the browser is not signed in to Pennylane.

### What information do I need to provide?

Required: companyId, invoiceIds. Optional: dryRun.

### What does it return?

It returns dryRun, results, restoredCount.

### Do I need to be logged in to app.pennylane.com?

Yes. It acts as you on app.pennylane.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the app.pennylane.com cookies saved by the Reduck extension.

### Does it change anything on app.pennylane.com, or only read data?

It makes changes on app.pennylane.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/app.pennylane.com/unarchive_invoices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.pennylane.com/unarchive_invoices

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/app.pennylane.com/unarchive_invoices
