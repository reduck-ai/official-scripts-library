# List Claude invoices

Automatically list Claude invoices on claude.ai. List every invoice across the orgs you have billing access to. Returns invoices (org_uuid, org_name, created_ts, due_date_ts, total, total_excluding_tax, currency, status, num_seats, hosted_invoice_url, invoice_pdf_url, payment_status) and skipped, newest first. Orgs you lack billing access to are reported in skipped rather than raising an error. Feed hosted_invoice_url to invoice.stripe.com/download_invoice_pdf to fetch the PDF (verified public/login-free, no Claude session needed).

- Site: claude.ai
- Address: `reduck/claude.ai/list_invoices`
- Updated: 2026-08-20 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/claude.ai/list_invoices`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/claude.ai/list_invoices
```

## Input

- `org_uuid` (string, optional): Restrict to a single org's invoices by its uuid. Omit to list invoices across every org you have billing access to.

## Output

- `skipped` (array, required)
- `invoices` (array, required)

## FAQ

### What does "List Claude invoices" do?

List every invoice across the orgs you have billing access to. Returns invoices (org_uuid, org_name, created_ts, due_date_ts, total, total_excluding_tax, currency, status, num_seats, hosted_invoice_url, invoice_pdf_url, payment_status) and skipped, newest first. Orgs you lack billing access to are reported in skipped rather than raising an error. Feed hosted_invoice_url to invoice.stripe.com/download_invoice_pdf to fetch the PDF (verified public/login-free, no Claude session needed).

### How do I automatically list Claude invoices on claude.ai?

Ask an AI agent connected to Reduck to run reduck/claude.ai/list_invoices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/claude.ai/list_invoices

### Is there a claude.ai API to list Claude invoices?

You do not need one. "List Claude invoices" drives the real claude.ai pages in a browser, so it works whether or not claude.ai offers an API for this.

### What information do I need to provide?

Optional: org_uuid.

### What does it return?

It returns skipped, invoices.

### Do I need to be logged in to claude.ai?

Yes. It acts as you on claude.ai: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the claude.ai cookies saved by the Reduck extension.

### Does it change anything on claude.ai, or only read data?

It only reads. It looks things up on claude.ai and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/claude.ai/list_invoices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/claude.ai/list_invoices

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/claude.ai/list_invoices
