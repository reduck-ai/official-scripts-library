# List Postmark receipts

Automatically list Postmark receipts on account.postmarkapp.com. List the billing receipts of the signed-in Postmark account: receiptId (for download_invoice), invoice date, purchase description and amount. An account with no receipts returns an empty list.

- Site: account.postmarkapp.com
- Address: `reduck/account.postmarkapp.com/list_invoices`
- Updated: 2026-10-22 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/account.postmarkapp.com/list_invoices`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/account.postmarkapp.com/list_invoices
```

## Input

It takes no input.

## Output

- `count` (integer, required)
- `receipts` (array, required)
- `hasMore` (boolean, optional)

## FAQ

### What does "List Postmark receipts" do?

List the billing receipts of the signed-in Postmark account: receiptId (for download_invoice), invoice date, purchase description and amount. An account with no receipts returns an empty list.

### How do I automatically list Postmark receipts on account.postmarkapp.com?

Ask an AI agent connected to Reduck to run reduck/account.postmarkapp.com/list_invoices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/account.postmarkapp.com/list_invoices

### Is there a account.postmarkapp.com API to list Postmark receipts?

You do not need one. "List Postmark receipts" drives the real account.postmarkapp.com pages in a browser, so it works whether or not account.postmarkapp.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns count, hasMore, receipts.

### Do I need to be logged in to account.postmarkapp.com?

Yes. It acts as you on account.postmarkapp.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the account.postmarkapp.com cookies saved by the Reduck extension.

### Does it change anything on account.postmarkapp.com, or only read data?

It only reads. It looks things up on account.postmarkapp.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/account.postmarkapp.com/list_invoices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/account.postmarkapp.com/list_invoices

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/account.postmarkapp.com/list_invoices
