# Cursor — list invoices

Automatically list invoices on cursor.com. List Cursor billing invoices for the logged-in team. Returns each invoice's date, status, amount, a link to view it, and a direct PDF download link.

- Site: cursor.com
- Address: `reduck/cursor.com/list_invoices`
- Updated: 2026-08-20 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/cursor.com/list_invoices`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/cursor.com/list_invoices
```

## Input

It takes no input.

## Output

- `count` (integer, required)
- `invoices` (array, required)

## FAQ

### What does "Cursor — list invoices" do?

List Cursor billing invoices for the logged-in team. Returns each invoice's date, status, amount, a link to view it, and a direct PDF download link.

### How do I automatically list invoices on cursor.com?

Ask an AI agent connected to Reduck to run reduck/cursor.com/list_invoices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/cursor.com/list_invoices

### Is there a cursor.com API to list invoices?

You do not need one. "Cursor — list invoices" drives the real cursor.com pages in a browser, so it works whether or not cursor.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns count, invoices.

### Do I need to be logged in to cursor.com?

Yes. It acts as you on cursor.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the cursor.com cookies saved by the Reduck extension.

### Does it change anything on cursor.com, or only read data?

It only reads. It looks things up on cursor.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/cursor.com/list_invoices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/cursor.com/list_invoices

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/cursor.com/list_invoices
