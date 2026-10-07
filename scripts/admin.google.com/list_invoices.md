# Google Workspace unofficial API: list your invoices by date range

Automatically list your invoices by date range on admin.google.com. An unofficial Google Workspace API for billing invoices. List Google Workspace billing documents from the Admin Console for one date range (This month … All time) and one format (CSV or PDF). Returns account and invoices (label, format, createdDate, invoiceNumber) — metadata only. Feed a row's label, with the same dateRange and format, to admin.google.com/download_invoice to get the file.

- Site: admin.google.com
- Address: `reduck/admin.google.com/list_invoices`
- Updated: 2026-10-06 (v8)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/admin.google.com/list_invoices`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/admin.google.com/list_invoices
```

## Input

- `format` (string, optional): Document format to list. Default: CSV.
- `dateRange` (string, optional): Date range label as shown in the Workspace billing UI. Default: This year.

## Output

- `account` (string, optional)
- `invoices` (array, optional)

## FAQ

### What does "Google Workspace unofficial API: list your invoices by date range" do?

An unofficial Google Workspace API for billing invoices. List Google Workspace billing documents from the Admin Console for one date range (This month … All time) and one format (CSV or PDF). Returns account and invoices (label, format, createdDate, invoiceNumber) — metadata only. Feed a row's label, with the same dateRange and format, to admin.google.com/download_invoice to get the file.

### How do I automatically list your invoices by date range on admin.google.com?

Ask an AI agent connected to Reduck to run reduck/admin.google.com/list_invoices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/admin.google.com/list_invoices

### Is there a admin.google.com API to list your invoices by date range?

You do not need one. "Google Workspace unofficial API: list your invoices by date range" drives the real admin.google.com pages in a browser, so it works whether or not admin.google.com offers an API for this.

### What information do I need to provide?

Optional: format, dateRange.

### What does it return?

It returns account, invoices.

### Do I need to be logged in to admin.google.com?

Yes. It acts as you on admin.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the admin.google.com cookies saved by the Reduck extension.

### Does it change anything on admin.google.com, or only read data?

It only reads. It looks things up on admin.google.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/admin.google.com/list_invoices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/admin.google.com/list_invoices

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/admin.google.com/list_invoices
