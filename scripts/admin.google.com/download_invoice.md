# Google Workspace API: download a Google Workspace invoice PDF or CSV

Automatically download a Google Workspace invoice PDF or CSV on admin.google.com. An unofficial Google Workspace API to download billing invoices. Download a single Google Workspace billing document (CSV or PDF) by its line-item label from admin.google.com/list_invoices (pass the same dateRange/format used to list it). Returns the file bytes as base64 plus a filename.

- Site: admin.google.com
- Address: `reduck/admin.google.com/download_invoice`
- Updated: 2026-09-29 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/admin.google.com/download_invoice`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/admin.google.com/download_invoice
```

## Input

- `label` (string, required): The exact `label` field from admin.google.com/list_invoices.
- `format` (string, optional): Must match the format used to list this item. Default: CSV.
- `dateRange` (string, optional): Must match the dateRange used to list this item. Default: This year.

## Output

- `filename` (string, required)
- `contentBase64` (string, required)

## FAQ

### What does "Google Workspace API: download a Google Workspace invoice PDF or CSV" do?

An unofficial Google Workspace API to download billing invoices. Download a single Google Workspace billing document (CSV or PDF) by its line-item label from admin.google.com/list_invoices (pass the same dateRange/format used to list it). Returns the file bytes as base64 plus a filename.

### How do I automatically download a Google Workspace invoice PDF or CSV on admin.google.com?

Ask an AI agent connected to Reduck to run reduck/admin.google.com/download_invoice, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/admin.google.com/download_invoice

### Is there a admin.google.com API to download a Google Workspace invoice PDF or CSV?

You do not need one. "Google Workspace API: download a Google Workspace invoice PDF or CSV" drives the real admin.google.com pages in a browser, so it works whether or not admin.google.com offers an API for this.

### What information do I need to provide?

Required: label. Optional: format, dateRange.

### What does it return?

It returns filename, contentBase64.

### Do I need to be logged in to admin.google.com?

Yes. It acts as you on admin.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the admin.google.com cookies saved by the Reduck extension.

### Does it change anything on admin.google.com, or only read data?

It only reads. It looks things up on admin.google.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/admin.google.com/download_invoice, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/admin.google.com/download_invoice

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/admin.google.com/download_invoice
