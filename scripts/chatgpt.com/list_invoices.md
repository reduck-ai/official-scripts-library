# ChatGPT billing: list your ChatGPT subscription invoices

Automatically list your ChatGPT subscription invoices on chatgpt.com. ChatGPT subscription invoices, not the OpenAI API platform. Lists the billing history of the ChatGPT account currently open in this browser, as its Billing page shows it: only that account's invoices, never those of the user's other accounts. To get another account's invoices, switch ChatGPT to that account, then run this again. A Business, Team or Enterprise workspace open in the browser has no personal Billing page, and the run fails saying so. Each invoice comes with its date, amount, currency, payment status, plan and a link to the invoice; the result also names the active account and lists every account the user belongs to. Amounts are in the currency's smallest unit, so 1917 means 19.17 EUR. The Billing page shows the most recent invoices first and this script cannot page further: when ChatGPT says older invoices exist, complete is false and next_cursor holds the cursor ChatGPT gave, but those older invoices are not returned. When the browser is not signed in to ChatGPT, the run fails with a not-signed-in error. Pass hosted_invoice_url to the Stripe invoice PDF download script to get the PDF.

- Site: chatgpt.com
- Address: `reduck/chatgpt.com/list_invoices`
- Updated: 2026-10-19 (v13)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/chatgpt.com/list_invoices`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/chatgpt.com/list_invoices
```

## Input

It takes no input.

## Output

- `account` (any, required): The account open in this browser, whose invoices are listed.
- `accounts` (array, required): Every ChatGPT account the user belongs to; only the active one's invoices are listed.
- `complete` (boolean, required): false when ChatGPT says the account has older invoices than the ones its Billing page loads.
- `invoices` (array, required)
- `signed_in` (boolean, required): Always true: a browser that is not signed in to ChatGPT makes the run fail with a not-signed-in error.
- `next_cursor` (string | null, required): The cursor ChatGPT gave for its older invoices when complete is false; null otherwise. This script cannot page with it.

## FAQ

### What does "ChatGPT billing: list your ChatGPT subscription invoices" do?

ChatGPT subscription invoices, not the OpenAI API platform. Lists the billing history of the ChatGPT account currently open in this browser, as its Billing page shows it: only that account's invoices, never those of the user's other accounts. To get another account's invoices, switch ChatGPT to that account, then run this again. A Business, Team or Enterprise workspace open in the browser has no personal Billing page, and the run fails saying so. Each invoice comes with its date, amount, currency, payment status, plan and a link to the invoice; the result also names the active account and lists every account the user belongs to. Amounts are in the currency's smallest unit, so 1917 means 19.17 EUR. The Billing page shows the most recent invoices first and this script cannot page further: when ChatGPT says older invoices exist, complete is false and next_cursor holds the cursor ChatGPT gave, but those older invoices are not returned. When the browser is not signed in to ChatGPT, the run fails with a not-signed-in error. Pass hosted_invoice_url to the Stripe invoice PDF download script to get the PDF.

### How do I automatically list your ChatGPT subscription invoices on chatgpt.com?

Ask an AI agent connected to Reduck to run reduck/chatgpt.com/list_invoices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/chatgpt.com/list_invoices

### Is there a chatgpt.com API to list your ChatGPT subscription invoices?

You do not need one. "ChatGPT billing: list your ChatGPT subscription invoices" drives the real chatgpt.com pages in a browser, so it works whether or not chatgpt.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns account, accounts, complete, invoices, signed_in, next_cursor.

### Do I need to be logged in to chatgpt.com?

Yes. It acts as you on chatgpt.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the chatgpt.com cookies saved by the Reduck extension.

### Does it change anything on chatgpt.com, or only read data?

It only reads. It looks things up on chatgpt.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/chatgpt.com/list_invoices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/chatgpt.com/list_invoices

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/chatgpt.com/list_invoices
