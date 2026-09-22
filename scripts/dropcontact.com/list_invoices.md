# List Dropcontact billing invoices

Automatically list Dropcontact billing invoices on dropcontact.com. Lists the Dropcontact billing invoices (Stripe-hosted) for the signed-in account, going from the app's billing settings into the Stripe customer portal and reading its invoice history. Requires an authenticated app.dropcontact.com session. Returns per invoice: date, amount, status, statusTone and hostedInvoiceUrl — an invoice.stripe.com page with its own download button, so this returns links rather than PDF files. `status` is the wording the portal shows, in whatever language it serves it; `statusTone` is the language-independent reading of the same badge ("positive" for a settled invoice). date and amount are nullable. Works in any portal language.

- Site: dropcontact.com
- Address: `reduck/dropcontact.com/list_invoices`
- Updated: 2026-08-24 (v7)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/dropcontact.com/list_invoices`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/dropcontact.com/list_invoices
```

## Input

It takes no input.

## Output

- `invoices` (array, optional)

## FAQ

### What does "List Dropcontact billing invoices" do?

Lists the Dropcontact billing invoices (Stripe-hosted) for the signed-in account, going from the app's billing settings into the Stripe customer portal and reading its invoice history. Requires an authenticated app.dropcontact.com session. Returns per invoice: date, amount, status, statusTone and hostedInvoiceUrl — an invoice.stripe.com page with its own download button, so this returns links rather than PDF files. `status` is the wording the portal shows, in whatever language it serves it; `statusTone` is the language-independent reading of the same badge ("positive" for a settled invoice). date and amount are nullable. Works in any portal language.

### How do I automatically list Dropcontact billing invoices on dropcontact.com?

Ask an AI agent connected to Reduck to run reduck/dropcontact.com/list_invoices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/dropcontact.com/list_invoices

### Is there a dropcontact.com API to list Dropcontact billing invoices?

You do not need one. "List Dropcontact billing invoices" drives the real dropcontact.com pages in a browser, so it works whether or not dropcontact.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns invoices.

### Do I need to be logged in to dropcontact.com?

Yes. It acts as you on dropcontact.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the dropcontact.com cookies saved by the Reduck extension.

### Does it change anything on dropcontact.com, or only read data?

It only reads. It looks things up on dropcontact.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/dropcontact.com/list_invoices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/dropcontact.com/list_invoices

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/dropcontact.com/list_invoices
