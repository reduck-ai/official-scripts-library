# ChatGPT billing: list your ChatGPT subscription invoices

Automatically list your ChatGPT subscription invoices on chatgpt.com. ChatGPT subscription invoices, not the OpenAI API platform (that is platform.openai.com/list_invoices). List the billing history of every ChatGPT account the signed-in user belongs to — the personal account and each Business, Team or Enterprise workspace — whichever one the browser currently has open. Each invoice comes with its date, amount, currency, payment status, the plan it paid for, a link to the receipt, and the account it belongs to; a separate accounts list shows each account, how many invoices it has, and whether its billing could be read. The full history is returned, not only the most recent entries. Amounts come back in the currency's smallest unit, so 1917 means 19.17 EUR. When the browser is not signed in to ChatGPT, the result says so with signed_in set to false and empty lists; check it before reading an empty list as an account that was never billed. Feed hosted_invoice_url to invoice.stripe.com/download_invoice_pdf to get the PDF.

- Site: chatgpt.com
- Address: `reduck/chatgpt.com/list_invoices`
- Updated: 2026-09-30 (v10)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/chatgpt.com/list_invoices`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/chatgpt.com/list_invoices
```

## Input

It takes no input.

## Output

- `accounts` (array, required)
- `invoices` (array, required)
- `signed_in` (boolean, required): false when this browser is not signed in to ChatGPT; invoices and accounts are then empty because nothing could be read, not because the account was never billed.

## FAQ

### What does "ChatGPT billing: list your ChatGPT subscription invoices" do?

ChatGPT subscription invoices, not the OpenAI API platform (that is platform.openai.com/list_invoices). List the billing history of every ChatGPT account the signed-in user belongs to — the personal account and each Business, Team or Enterprise workspace — whichever one the browser currently has open. Each invoice comes with its date, amount, currency, payment status, the plan it paid for, a link to the receipt, and the account it belongs to; a separate accounts list shows each account, how many invoices it has, and whether its billing could be read. The full history is returned, not only the most recent entries. Amounts come back in the currency's smallest unit, so 1917 means 19.17 EUR. When the browser is not signed in to ChatGPT, the result says so with signed_in set to false and empty lists; check it before reading an empty list as an account that was never billed. Feed hosted_invoice_url to invoice.stripe.com/download_invoice_pdf to get the PDF.

### How do I automatically list your ChatGPT subscription invoices on chatgpt.com?

Ask an AI agent connected to Reduck to run reduck/chatgpt.com/list_invoices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/chatgpt.com/list_invoices

### Is there a chatgpt.com API to list your ChatGPT subscription invoices?

You do not need one. "ChatGPT billing: list your ChatGPT subscription invoices" drives the real chatgpt.com pages in a browser, so it works whether or not chatgpt.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns accounts, invoices, signed_in.

### Do I need to be logged in to chatgpt.com?

Yes. It acts as you on chatgpt.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the chatgpt.com cookies saved by the Reduck extension.

### Does it change anything on chatgpt.com, or only read data?

It only reads. It looks things up on chatgpt.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/chatgpt.com/list_invoices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/chatgpt.com/list_invoices

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/chatgpt.com/list_invoices
