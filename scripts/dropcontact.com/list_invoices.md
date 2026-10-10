# List Dropcontact billing invoices

Automatically list Dropcontact billing invoices on dropcontact.com. List the billing invoices of the signed-in Dropcontact account. Returns per invoice: date, amount, status, statusTone and hostedInvoiceUrl (an invoice page with its own download button, so this returns links rather than PDF files). `status` is the wording shown, in whatever language it is served; `statusTone` is the language-independent reading of the same badge ("positive" for a settled invoice). date and amount are nullable. Accounts with no active subscription have no invoices to read and say so.

- Site: dropcontact.com
- Address: `reduck/dropcontact.com/list_invoices`
- Updated: 2026-10-09 (v8)
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

List the billing invoices of the signed-in Dropcontact account. Returns per invoice: date, amount, status, statusTone and hostedInvoiceUrl (an invoice page with its own download button, so this returns links rather than PDF files). `status` is the wording shown, in whatever language it is served; `statusTone` is the language-independent reading of the same badge ("positive" for a settled invoice). date and amount are nullable. Accounts with no active subscription have no invoices to read and say so.

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
