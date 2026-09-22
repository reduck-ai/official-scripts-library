# List Linear invoices

Automatically list Linear invoices on linear.app. List the invoices on a Linear workspace's billing page (linear.app/<workspace>/settings/billing, "Recent invoices" section). Requires you to already be logged in to Linear in your browser. Each invoice row exposes a public Stripe hosted-invoice URL ("View" link). Returns workspace + invoices[{date, description, amount, url}] exactly as displayed (amount is the shown string e.g. "$12.00"); empty list is a valid result for a workspace with no invoices.

- Site: linear.app
- Address: `reduck/linear.app/list_invoices`
- Updated: 2026-09-04 (v6)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linear.app/list_invoices`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linear.app/list_invoices
```

## Input

- `workspace` (string, optional): Linear workspace URL slug, e.g. "acme" (from linear.app/<workspace>/…). Optional — defaults to the currently active workspace.

## Output

- `invoices` (array, required)
- `workspace` (string, required)

## FAQ

### What does "List Linear invoices" do?

List the invoices on a Linear workspace's billing page (linear.app/<workspace>/settings/billing, "Recent invoices" section). Requires you to already be logged in to Linear in your browser. Each invoice row exposes a public Stripe hosted-invoice URL ("View" link). Returns workspace + invoices[{date, description, amount, url}] exactly as displayed (amount is the shown string e.g. "$12.00"); empty list is a valid result for a workspace with no invoices.

### How do I automatically list Linear invoices on linear.app?

Ask an AI agent connected to Reduck to run reduck/linear.app/list_invoices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linear.app/list_invoices

### Is there a linear.app API to list Linear invoices?

You do not need one. "List Linear invoices" drives the real linear.app pages in a browser, so it works whether or not linear.app offers an API for this.

### What information do I need to provide?

Optional: workspace.

### What does it return?

It returns invoices, workspace.

### Do I need to be logged in to linear.app?

Yes. It acts as you on linear.app: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linear.app cookies saved by the Reduck extension.

### Does it change anything on linear.app, or only read data?

It only reads. It looks things up on linear.app and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linear.app/list_invoices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linear.app/list_invoices

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linear.app/list_invoices
