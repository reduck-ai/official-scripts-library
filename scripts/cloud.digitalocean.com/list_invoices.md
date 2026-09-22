# List DigitalOcean invoices

Automatically list DigitalOcean invoices on cloud.digitalocean.com. List DigitalOcean billing history (invoices + payment receipts) for the signed-in team. Requires an authenticated cloud.digitalocean.com session. Returns count and, per entry, date, amount, type, description, a session-gated invoicePdfUrl and the raw receiptId/invoiceUuid/accountUrn.

- Site: cloud.digitalocean.com
- Address: `reduck/cloud.digitalocean.com/list_invoices`
- Updated: 2026-08-18 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/cloud.digitalocean.com/list_invoices`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/cloud.digitalocean.com/list_invoices
```

## Input

It takes no input.

## Output

- `count` (integer, required)
- `invoices` (array, required)

## FAQ

### What does "List DigitalOcean invoices" do?

List DigitalOcean billing history (invoices + payment receipts) for the signed-in team. Requires an authenticated cloud.digitalocean.com session. Returns count and, per entry, date, amount, type, description, a session-gated invoicePdfUrl and the raw receiptId/invoiceUuid/accountUrn.

### How do I automatically list DigitalOcean invoices on cloud.digitalocean.com?

Ask an AI agent connected to Reduck to run reduck/cloud.digitalocean.com/list_invoices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/cloud.digitalocean.com/list_invoices

### Is there a cloud.digitalocean.com API to list DigitalOcean invoices?

You do not need one. "List DigitalOcean invoices" drives the real cloud.digitalocean.com pages in a browser, so it works whether or not cloud.digitalocean.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns count, invoices.

### Do I need to be logged in to cloud.digitalocean.com?

Yes. It acts as you on cloud.digitalocean.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the cloud.digitalocean.com cookies saved by the Reduck extension.

### Does it change anything on cloud.digitalocean.com, or only read data?

It only reads. It looks things up on cloud.digitalocean.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/cloud.digitalocean.com/list_invoices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/cloud.digitalocean.com/list_invoices

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/cloud.digitalocean.com/list_invoices
