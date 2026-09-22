# List ChatGPT invoices

Automatically list ChatGPT invoices on chatgpt.com. List the billing history of the signed-in ChatGPT account: every invoice with its date, amount, currency, payment status, the plan it paid for, and a link to the receipt. The full history is returned, not only the most recent entries. Amounts come back in the currency's smallest unit, so 1917 means 19.17 EUR. An account that has never been billed returns an empty list. Feed hosted_invoice_url to invoice.stripe.com/download_invoice_pdf to fetch the PDF.

- Site: chatgpt.com
- Address: `reduck/chatgpt.com/list_invoices`
- Updated: 2026-08-20 (v6)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/chatgpt.com/list_invoices`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/chatgpt.com/list_invoices
```

## Input

It takes no input.

## Output

- `invoices` (array, required)

## FAQ

### What does "List ChatGPT invoices" do?

List the billing history of the signed-in ChatGPT account: every invoice with its date, amount, currency, payment status, the plan it paid for, and a link to the receipt. The full history is returned, not only the most recent entries. Amounts come back in the currency's smallest unit, so 1917 means 19.17 EUR. An account that has never been billed returns an empty list. Feed hosted_invoice_url to invoice.stripe.com/download_invoice_pdf to fetch the PDF.

### How do I automatically list ChatGPT invoices on chatgpt.com?

Ask an AI agent connected to Reduck to run reduck/chatgpt.com/list_invoices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/chatgpt.com/list_invoices

### Is there a chatgpt.com API to list ChatGPT invoices?

You do not need one. "List ChatGPT invoices" drives the real chatgpt.com pages in a browser, so it works whether or not chatgpt.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns invoices.

### Do I need to be logged in to chatgpt.com?

Yes. It acts as you on chatgpt.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the chatgpt.com cookies saved by the Reduck extension.

### Does it change anything on chatgpt.com, or only read data?

Unknown: its author has not declared whether it changes anything on chatgpt.com, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/chatgpt.com/list_invoices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/chatgpt.com/list_invoices

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/chatgpt.com/list_invoices
