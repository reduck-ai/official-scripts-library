# Approve Pennylane supplier invoices

Approve one or more Pennylane supplier invoices that are waiting for approval, by id. With dryRun (default true) each invoice is found and selected in the list, but not approved. With dryRun false it is approved, then read back. Approving an invoice already matched to a bank transaction marks it paid. Returns, per invoice, whether it was found, its label and amount, its status after the run, whether it was approved, and a warning when it is not waiting for approval or has no invoice number to single it out. Fails with a sign-in error when the browser is not signed in to Pennylane.

- Site: app.pennylane.com
- Address: `reduck/app.pennylane.com/approve_invoices`
- Updated: 2026-10-29 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/app.pennylane.com/approve_invoices`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/app.pennylane.com/approve_invoices
```

## Input

- `companyId` (integer | string, required): Pennylane company id, the number in the app URL at /companies/<id>/supplier_invoices.
- `invoiceIds` (array, required): Invoice ids (as returned by list_invoices) to approve.
- `dryRun` (boolean, optional): true (default): find and select each invoice without approving it. false: approve.

## Output

- `dryRun` (boolean, required)
- `results` (array, required)
- `approvedCount` (number, required)

## FAQ

### What does "Approve Pennylane supplier invoices" do?

Approve one or more Pennylane supplier invoices that are waiting for approval, by id. With dryRun (default true) each invoice is found and selected in the list, but not approved. With dryRun false it is approved, then read back. Approving an invoice already matched to a bank transaction marks it paid. Returns, per invoice, whether it was found, its label and amount, its status after the run, whether it was approved, and a warning when it is not waiting for approval or has no invoice number to single it out. Fails with a sign-in error when the browser is not signed in to Pennylane.

### What information do I need to provide?

Required: companyId, invoiceIds. Optional: dryRun.

### What does it return?

It returns dryRun, results, approvedCount.

### Do I need to be logged in to app.pennylane.com?

Yes. It acts as you on app.pennylane.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the app.pennylane.com cookies saved by the Reduck extension.

### Does it change anything on app.pennylane.com, or only read data?

It makes changes on app.pennylane.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/app.pennylane.com/approve_invoices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.pennylane.com/approve_invoices

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/app.pennylane.com/approve_invoices
