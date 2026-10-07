# List Google Payments activity (Google One, YouTube, Google Play charges)

Automatically list Google Payments activity (Google One, YouTube, Google Play charges) on pay.google.com. List the signed-in Google account's payments activity (pay.google.com > Activity): every Google charge, such as Google One storage and Google AI plans, YouTube Premium, and Google Play purchases and subscriptions. One row per transaction with merchant, transaction label (e.g. "12 Mar · 100 GB (Google One)") and amount, newest first. The transaction label is the join key for pay.google.com/download_tax_invoice, which downloads that charge's invoice. Scrolls until max rows or the list runs out.

- Site: pay.google.com
- Address: `reduck/pay.google.com/list_transactions`
- Updated: 2026-10-06 (v6)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/pay.google.com/list_transactions`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/pay.google.com/list_transactions
```

## Input

- `max` (integer, optional): Maximum rows to return (default 40).

## Output

- `total` (integer, required)
- `transactions` (array, required)

## FAQ

### What does "List Google Payments activity (Google One, YouTube, Google Play charges)" do?

List the signed-in Google account's payments activity (pay.google.com > Activity): every Google charge, such as Google One storage and Google AI plans, YouTube Premium, and Google Play purchases and subscriptions. One row per transaction with merchant, transaction label (e.g. "12 Mar · 100 GB (Google One)") and amount, newest first. The transaction label is the join key for pay.google.com/download_tax_invoice, which downloads that charge's invoice. Scrolls until max rows or the list runs out.

### How do I automatically list Google Payments activity (Google One, YouTube, Google Play charges) on pay.google.com?

Ask an AI agent connected to Reduck to run reduck/pay.google.com/list_transactions, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/pay.google.com/list_transactions

### Is there a pay.google.com API to list Google Payments activity (Google One, YouTube, Google Play charges)?

You do not need one. "List Google Payments activity (Google One, YouTube, Google Play charges)" drives the real pay.google.com pages in a browser, so it works whether or not pay.google.com offers an API for this.

### What information do I need to provide?

Optional: max.

### What does it return?

It returns total, transactions.

### Do I need to be logged in to pay.google.com?

Yes. It acts as you on pay.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the pay.google.com cookies saved by the Reduck extension.

### Does it change anything on pay.google.com, or only read data?

It only reads. It looks things up on pay.google.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/pay.google.com/list_transactions, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/pay.google.com/list_transactions

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/pay.google.com/list_transactions
