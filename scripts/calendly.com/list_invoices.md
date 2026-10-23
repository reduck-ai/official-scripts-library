# List Calendly invoices

Automatically list Calendly invoices on calendly.com. List Calendly billing invoices (org admin only). Per invoice returns date, title, amount, currency, status, invoiceId, chargeId and downloadUrl (a direct Stripe PDF link; open it in a browser to save). A signed-out browser fails with a signed-out error asking to sign in to calendly.com (calendly.com/login_with_google can do it); an account that is not an org admin fails asking to sign in as one. An account with no charges returns an empty list.

- Site: calendly.com
- Address: `reduck/calendly.com/list_invoices`
- Updated: 2026-10-22 (v6)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/calendly.com/list_invoices`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/calendly.com/list_invoices
```

## Input

It takes no input.

## Output

- `total` (integer, required): Number of invoices (charges) returned.
- `invoices` (array, required)

## FAQ

### What does "List Calendly invoices" do?

List Calendly billing invoices (org admin only). Per invoice returns date, title, amount, currency, status, invoiceId, chargeId and downloadUrl (a direct Stripe PDF link; open it in a browser to save). A signed-out browser fails with a signed-out error asking to sign in to calendly.com (calendly.com/login_with_google can do it); an account that is not an org admin fails asking to sign in as one. An account with no charges returns an empty list.

### How do I automatically list Calendly invoices on calendly.com?

Ask an AI agent connected to Reduck to run reduck/calendly.com/list_invoices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/calendly.com/list_invoices

### Is there a calendly.com API to list Calendly invoices?

You do not need one. "List Calendly invoices" drives the real calendly.com pages in a browser, so it works whether or not calendly.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns total, invoices.

### Do I need to be logged in to calendly.com?

Yes. It acts as you on calendly.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the calendly.com cookies saved by the Reduck extension.

### Does it change anything on calendly.com, or only read data?

It only reads. It looks things up on calendly.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/calendly.com/list_invoices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/calendly.com/list_invoices

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/calendly.com/list_invoices
