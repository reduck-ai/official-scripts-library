# List Qonto transactions

Automatically list Qonto transactions on qonto.com. List the most recent transactions on the signed-in Qonto business account, newest first, paging through the full history up to a limit (default 50, max 500). Each transaction has its date and settlement time, counterparty, signed amount (negative = money out), the amount including Qonto fees as the app shows it, currency and original foreign amount, debit/credit, status (completed, pending, declined, reversed), payment method, category, note, card last 4, who initiated it, attachment count and whether a receipt is required, and the balance after it. totalCount gives the account's full transaction count. Read-only.

- Site: qonto.com
- Address: `reduck/qonto.com/list_transactions`
- Updated: 2026-09-28 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/qonto.com/list_transactions`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/qonto.com/list_transactions
```

## Input

- `limit` (integer, optional): How many of the most recent transactions to return.

## Output

- `returned` (integer, required)
- `totalCount` (integer, required): Total transactions on the account (all pages).
- `organization` (string, required): Qonto organization slug.
- `transactions` (array, required)

## FAQ

### What does "List Qonto transactions" do?

List the most recent transactions on the signed-in Qonto business account, newest first, paging through the full history up to a limit (default 50, max 500). Each transaction has its date and settlement time, counterparty, signed amount (negative = money out), the amount including Qonto fees as the app shows it, currency and original foreign amount, debit/credit, status (completed, pending, declined, reversed), payment method, category, note, card last 4, who initiated it, attachment count and whether a receipt is required, and the balance after it. totalCount gives the account's full transaction count. Read-only.

### How do I automatically list Qonto transactions on qonto.com?

Ask an AI agent connected to Reduck to run reduck/qonto.com/list_transactions, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/qonto.com/list_transactions

### Is there a qonto.com API to list Qonto transactions?

You do not need one. "List Qonto transactions" drives the real qonto.com pages in a browser, so it works whether or not qonto.com offers an API for this.

### What information do I need to provide?

Optional: limit.

### What does it return?

It returns returned, totalCount, organization, transactions.

### Do I need to be logged in to qonto.com?

Yes. It acts as you on qonto.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the qonto.com cookies saved by the Reduck extension.

### Does it change anything on qonto.com, or only read data?

It only reads. It looks things up on qonto.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/qonto.com/list_transactions, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/qonto.com/list_transactions

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/qonto.com/list_transactions
