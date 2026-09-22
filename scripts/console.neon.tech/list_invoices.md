# List Neon invoices

Automatically list Neon invoices on console.neon.tech. List the signed-in Neon organization's billing invoices, read directly from the console's own invoices API. Neon bills via Orb, so each invoice's pdfUrl is its Orb-hosted PDF (assets.withorb.com/invoice/...?token=, a public tokenized link). Returns org, total, and invoices (reference, issued, total, status, pdfUrl). Reads the default organization the console lands on; an account with multiple orgs sees only that one.

- Site: console.neon.tech
- Address: `reduck/console.neon.tech/list_invoices`
- Updated: 2026-08-19 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/console.neon.tech/list_invoices`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/console.neon.tech/list_invoices
```

## Input

It takes no input.

## Output

- `total` (integer, required)
- `invoices` (array, required)
- `org` (string, optional)

## FAQ

### What does "List Neon invoices" do?

List the signed-in Neon organization's billing invoices, read directly from the console's own invoices API. Neon bills via Orb, so each invoice's pdfUrl is its Orb-hosted PDF (assets.withorb.com/invoice/...?token=, a public tokenized link). Returns org, total, and invoices (reference, issued, total, status, pdfUrl). Reads the default organization the console lands on; an account with multiple orgs sees only that one.

### How do I automatically list Neon invoices on console.neon.tech?

Ask an AI agent connected to Reduck to run reduck/console.neon.tech/list_invoices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/console.neon.tech/list_invoices

### Is there a console.neon.tech API to list Neon invoices?

You do not need one. "List Neon invoices" drives the real console.neon.tech pages in a browser, so it works whether or not console.neon.tech offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns org, total, invoices.

### Do I need to be logged in to console.neon.tech?

Yes. It acts as you on console.neon.tech: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the console.neon.tech cookies saved by the Reduck extension.

### Does it change anything on console.neon.tech, or only read data?

It only reads. It looks things up on console.neon.tech and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/console.neon.tech/list_invoices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/console.neon.tech/list_invoices

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/console.neon.tech/list_invoices
