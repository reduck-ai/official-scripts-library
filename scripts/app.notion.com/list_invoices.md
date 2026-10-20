# List Notion invoices across workspaces

Automatically list Notion invoices across workspaces on app.notion.com. List every Notion invoice across your workspaces. Notion does not email invoices; they are only available in each workspace's billing settings. Returns invoices with space_id, space_name, invoice_id, created_ts, total, currency, status, payment_status, and hosted_invoice_url. Total is in cents and currency is a lowercase ISO code (e.g. eur); feed hosted_invoice_url to app.notion.com/download_invoice_pdf to get the PDF. Workspaces whose billing you cannot read are listed in skipped_spaces with the reason.

- Site: app.notion.com
- Address: `reduck/app.notion.com/list_invoices`
- Updated: 2026-10-19 (v11)
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
- `skipped_spaces` (array, optional): Workspaces whose billing the user cannot read (not owner/billing admin); their invoices are NOT in `invoices`.

## FAQ

### What does "List Notion invoices across workspaces" do?

List every Notion invoice across your workspaces. Notion does not email invoices; they are only available in each workspace's billing settings. Returns invoices with space_id, space_name, invoice_id, created_ts, total, currency, status, payment_status, and hosted_invoice_url. Total is in cents and currency is a lowercase ISO code (e.g. eur); feed hosted_invoice_url to app.notion.com/download_invoice_pdf to get the PDF. Workspaces whose billing you cannot read are listed in skipped_spaces with the reason.

### How do I automatically list Notion invoices across workspaces on app.notion.com?

Ask an AI agent connected to Reduck to run reduck/app.notion.com/list_invoices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.notion.com/list_invoices

### Is there a app.notion.com API to list Notion invoices across workspaces?

You do not need one. "List Notion invoices across workspaces" drives the real app.notion.com pages in a browser, so it works whether or not app.notion.com offers an API for this.

### What information do I need to provide?

Optional: space_id.

### What does it return?

It returns invoices, skipped_spaces.

### Do I need to be logged in to app.notion.com?

Yes. It acts as you on app.notion.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the app.notion.com cookies saved by the Reduck extension.

### Does it change anything on app.notion.com, or only read data?

It only reads. It looks things up on app.notion.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/app.notion.com/list_invoices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.notion.com/list_invoices

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/app.notion.com/list_invoices
