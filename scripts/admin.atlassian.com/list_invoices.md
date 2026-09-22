# List Atlassian invoices

Automatically list Atlassian invoices on admin.atlassian.com. List Atlassian (admin.atlassian.com) billing invoices across every transaction account in your org, covering Atlassian and Marketplace apps plus Loom billed through Atlassian. Returns total plus invoices (id, number, date, amount, status, transaction_account, sourceSystem, downloadUrl) — metadata only. Feed a row's downloadUrl to admin.atlassian.com/download_invoice to fetch the PDF. Only an org billing admin sees the billing portal, and admin.atlassian.com must resolve to a single org (no org picker).

- Site: admin.atlassian.com
- Address: `reduck/admin.atlassian.com/list_invoices`
- Updated: 2026-08-21 (v5)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/admin.atlassian.com/list_invoices`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/admin.atlassian.com/list_invoices
```

## Input

It takes no input.

## Output

- `total` (integer, required)
- `invoices` (array, required)

## FAQ

### What does "List Atlassian invoices" do?

List Atlassian (admin.atlassian.com) billing invoices across every transaction account in your org, covering Atlassian and Marketplace apps plus Loom billed through Atlassian. Returns total plus invoices (id, number, date, amount, status, transaction_account, sourceSystem, downloadUrl) — metadata only. Feed a row's downloadUrl to admin.atlassian.com/download_invoice to fetch the PDF. Only an org billing admin sees the billing portal, and admin.atlassian.com must resolve to a single org (no org picker).

### How do I automatically list Atlassian invoices on admin.atlassian.com?

Ask an AI agent connected to Reduck to run reduck/admin.atlassian.com/list_invoices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/admin.atlassian.com/list_invoices

### Is there a admin.atlassian.com API to list Atlassian invoices?

You do not need one. "List Atlassian invoices" drives the real admin.atlassian.com pages in a browser, so it works whether or not admin.atlassian.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns total, invoices.

### Do I need to be logged in to admin.atlassian.com?

Yes. It acts as you on admin.atlassian.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the admin.atlassian.com cookies saved by the Reduck extension.

### Does it change anything on admin.atlassian.com, or only read data?

It only reads. It looks things up on admin.atlassian.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/admin.atlassian.com/list_invoices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/admin.atlassian.com/list_invoices

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/admin.atlassian.com/list_invoices
