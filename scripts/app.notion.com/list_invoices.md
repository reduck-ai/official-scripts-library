# Notion API: list your Notion invoices across workspaces

Automatically list your Notion invoices across workspaces on app.notion.com. An unofficial Notion API for billing invoices: Notion does not email invoices, so they are only available under Settings > Billing. List every Notion invoice across your workspaces. Returns invoices with space_id, space_name, invoice_id, created_ts, total, currency, status, payment_status, and hosted_invoice_url. Total is in cents and currency is a lowercase ISO code (e.g. eur); feed hosted_invoice_url to app.notion.com/download_invoice_pdf to get the PDF.

- Site: app.notion.com
- Address: `reduck/app.notion.com/list_invoices`
- Updated: 2026-09-29 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/app.notion.com/list_invoices`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/app.notion.com/list_invoices
```

## Input

- `space_id` (string, optional): Restrict to one workspace UUID. Omit to fetch every workspace.

## Output

- `invoices` (array, required)

## FAQ

### What does "Notion API: list your Notion invoices across workspaces" do?

An unofficial Notion API for billing invoices: Notion does not email invoices, so they are only available under Settings > Billing. List every Notion invoice across your workspaces. Returns invoices with space_id, space_name, invoice_id, created_ts, total, currency, status, payment_status, and hosted_invoice_url. Total is in cents and currency is a lowercase ISO code (e.g. eur); feed hosted_invoice_url to app.notion.com/download_invoice_pdf to get the PDF.

### How do I automatically list your Notion invoices across workspaces on app.notion.com?

Ask an AI agent connected to Reduck to run reduck/app.notion.com/list_invoices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.notion.com/list_invoices

### Is there a app.notion.com API to list your Notion invoices across workspaces?

You do not need one. "Notion API: list your Notion invoices across workspaces" drives the real app.notion.com pages in a browser, so it works whether or not app.notion.com offers an API for this.

### What information do I need to provide?

Optional: space_id.

### What does it return?

It returns invoices.

### Do I need to be logged in to app.notion.com?

Yes. It acts as you on app.notion.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the app.notion.com cookies saved by the Reduck extension.

### Does it change anything on app.notion.com, or only read data?

Unknown: its author has not declared whether it changes anything on app.notion.com, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/app.notion.com/list_invoices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.notion.com/list_invoices

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/app.notion.com/list_invoices
