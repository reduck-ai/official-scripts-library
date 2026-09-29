# Get Wise card transaction detail

Automatically get Wise card transaction detail on wise.com. Fetch the full detail of a Wise card transaction by its transaction id: amount, date, card, merchant, state, recurrence and attachment state.

- Site: wise.com
- Address: `reduck/wise.com/get_transaction`
- Updated: 2026-09-28 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/wise.com/get_transaction`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/wise.com/get_transaction
```

## Input

- `transactionId` (string | integer, required): Wise card transaction id, e.g. "3922786193" (the number shown on the transaction, from search_transactions.transactionId).
- `profileId` (string, optional): Wise profile id. Defaults to 73787841 (Conception AI, Inc).

## Output

- `date` (string, required)
- `state` (string, required)
- `amount` (string, required)
- `hasAttachment` (boolean, required)
- `transactionId` (string, required)
- `cardLastDigits` (string | null, required)
- `type` (string, optional)
- `currency` (string, optional)
- `merchant` (object | null, optional)
- `amountValue` (number, optional)
- `attachments` (array, optional)
- `isRecurring` (boolean, optional)
- `authorisationMethod` (string | null, optional)
- `balanceTransactionId` (string | null, optional)

## FAQ

### What does "Get Wise card transaction detail" do?

Fetch the full detail of a Wise card transaction by its transaction id: amount, date, card, merchant, state, recurrence and attachment state.

### How do I automatically get Wise card transaction detail on wise.com?

Ask an AI agent connected to Reduck to run reduck/wise.com/get_transaction, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/wise.com/get_transaction

### Is there a wise.com API to get Wise card transaction detail?

You do not need one. "Get Wise card transaction detail" drives the real wise.com pages in a browser, so it works whether or not wise.com offers an API for this.

### What information do I need to provide?

Required: transactionId. Optional: profileId.

### What does it return?

It returns date, type, state, amount, currency, merchant, amountValue, attachments, isRecurring, hasAttachment, transactionId, cardLastDigits, authorisationMethod, balanceTransactionId.

### Do I need to be logged in to wise.com?

Yes. It acts as you on wise.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the wise.com cookies saved by the Reduck extension.

### Does it change anything on wise.com, or only read data?

Unknown: its author has not declared whether it changes anything on wise.com, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/wise.com/get_transaction, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/wise.com/get_transaction

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/wise.com/get_transaction
