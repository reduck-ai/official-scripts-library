# List Claude invoices

Automatically list Claude invoices on claude.ai. List the Claude (claude.ai) plan invoices of the organization currently open in this browser, as its billing settings show them, newest first. To get another organization's invoices, switch to it in claude.ai, then run this again. Each invoice comes with its number, date, total and total before tax (in the currency's smallest unit, so 10800 means 108.00 EUR), currency, status, seats, payment status and a link to its PDF. When the open organization gives you no billing access, the result lists it in skipped with no invoices. complete is false when claude.ai says the organization has older invoices than its billing page shows; those are not returned. The run fails when the browser is not signed in to claude.ai, or when org_uuid is given and a different organization is open. To save a PDF, pass its link to the Stripe invoice PDF download script.

- Site: claude.ai
- Address: `reduck/claude.ai/list_invoices`
- Updated: 2026-10-19 (v8)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/claude.ai/list_invoices`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/claude.ai/list_invoices
```

## Input

- `org_uuid` (string, optional): Optional check: the uuid of the organization you expect to be open in claude.ai. The run fails if a different organization is open.

## Output

- `skipped` (array, required)
- `complete` (boolean, required): false when claude.ai says the organization has older invoices than its billing page loads.
- `invoices` (array, required)

## FAQ

### What does "List Claude invoices" do?

List the Claude (claude.ai) plan invoices of the organization currently open in this browser, as its billing settings show them, newest first. To get another organization's invoices, switch to it in claude.ai, then run this again. Each invoice comes with its number, date, total and total before tax (in the currency's smallest unit, so 10800 means 108.00 EUR), currency, status, seats, payment status and a link to its PDF. When the open organization gives you no billing access, the result lists it in skipped with no invoices. complete is false when claude.ai says the organization has older invoices than its billing page shows; those are not returned. The run fails when the browser is not signed in to claude.ai, or when org_uuid is given and a different organization is open. To save a PDF, pass its link to the Stripe invoice PDF download script.

### How do I automatically list Claude invoices on claude.ai?

Ask an AI agent connected to Reduck to run reduck/claude.ai/list_invoices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/claude.ai/list_invoices

### Is there a claude.ai API to list Claude invoices?

You do not need one. "List Claude invoices" drives the real claude.ai pages in a browser, so it works whether or not claude.ai offers an API for this.

### What information do I need to provide?

Optional: org_uuid.

### What does it return?

It returns skipped, complete, invoices.

### Do I need to be logged in to claude.ai?

Yes. It acts as you on claude.ai: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the claude.ai cookies saved by the Reduck extension.

### Does it change anything on claude.ai, or only read data?

It only reads. It looks things up on claude.ai and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/claude.ai/list_invoices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/claude.ai/list_invoices

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/claude.ai/list_invoices
