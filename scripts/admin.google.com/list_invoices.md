# List Google Workspace invoices (CSV/PDF) over a date range

Automatically list Google Workspace invoices (CSV/PDF) over a date range on admin.google.com. Lists Google Workspace billing invoices from the Admin Console over a date range and returns each invoice's document content in CSV or PDF format.

- Site: admin.google.com
- Address: `reduck/admin.google.com/list_invoices`
- Updated: 2026-08-21 (v8)
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

### What does "List Google Workspace invoices (CSV/PDF) over a date range" do?

Lists Google Workspace billing invoices from the Admin Console over a date range and returns each invoice's document content in CSV or PDF format.

### How do I automatically list Google Workspace invoices (CSV/PDF) over a date range on admin.google.com?

Ask an AI agent connected to Reduck to run reduck/admin.google.com/list_invoices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/admin.google.com/list_invoices

### Is there a admin.google.com API to list Google Workspace invoices (CSV/PDF) over a date range?

You do not need one. "List Google Workspace invoices (CSV/PDF) over a date range" drives the real admin.google.com pages in a browser, so it works whether or not admin.google.com offers an API for this.

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
