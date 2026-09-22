# List Supabase invoices

Automatically list Supabase invoices on supabase.com. List invoices for a Supabase organization's billing (supabase.com/dashboard/org/<slug>/billing). Requires login. Auto-resolves the org from the picker when no slug is given (pass `org` to target a specific one; needed for multi-org accounts). Honors `limit`. Returns org + invoices[{id, number, status, subtotal, amount_due, period_end_ts, invoice_pdf}]. invoice_pdf is a public tokenized URL downloadable without auth. amount fields are raw integers from the API; free-plan invoices are 0.

- Site: supabase.com
- Address: `reduck/supabase.com/list_invoices`
- Updated: 2026-07-31 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/supabase.com/list_invoices`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/supabase.com/list_invoices
```

## Input

- `org` (string, optional): Organization slug (from the /dashboard/org/<slug>/ URL). Omit to auto-pick the org from the picker (first one).
- `limit` (integer, optional): Max invoices to return (most recent first). Default 25.

## Output

- `org` (string, required)
- `invoices` (array, required)

## FAQ

### What does "List Supabase invoices" do?

List invoices for a Supabase organization's billing (supabase.com/dashboard/org/<slug>/billing). Requires login. Auto-resolves the org from the picker when no slug is given (pass `org` to target a specific one; needed for multi-org accounts). Honors `limit`. Returns org + invoices[{id, number, status, subtotal, amount_due, period_end_ts, invoice_pdf}]. invoice_pdf is a public tokenized URL downloadable without auth. amount fields are raw integers from the API; free-plan invoices are 0.

### How do I automatically list Supabase invoices on supabase.com?

Ask an AI agent connected to Reduck to run reduck/supabase.com/list_invoices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/supabase.com/list_invoices

### Is there a supabase.com API to list Supabase invoices?

You do not need one. "List Supabase invoices" drives the real supabase.com pages in a browser, so it works whether or not supabase.com offers an API for this.

### What information do I need to provide?

Optional: org, limit.

### What does it return?

It returns org, invoices.

### Do I need to be logged in to supabase.com?

Yes. It acts as you on supabase.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the supabase.com cookies saved by the Reduck extension.

### Does it change anything on supabase.com, or only read data?

Unknown: its author has not declared whether it changes anything on supabase.com, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/supabase.com/list_invoices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/supabase.com/list_invoices

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/supabase.com/list_invoices
