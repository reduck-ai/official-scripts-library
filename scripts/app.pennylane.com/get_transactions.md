# Read Pennylane bank transactions by id

Automatically read Pennylane bank transactions by id on app.pennylane.com. Reads one or more Pennylane bank transactions by id, as the transaction's detail shows them: date, bank label, amount, account and bank, status, the part still to match, the supplier, and for a card payment the card used and the name of its holder. Use it to know who paid with which company card. Ids come from app.pennylane.com/find_transactions_for_invoice. An id the company does not have comes back with found false. Fails when signed out of Pennylane.

- Site: app.pennylane.com
- Address: `reduck/app.pennylane.com/get_transactions`
- Updated: 2026-10-29 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/app.pennylane.com/get_transactions`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/app.pennylane.com/get_transactions
```

## Input

- `companyId` (string | integer, required): The number in the app URL at /companies/<id>/.
- `transactionIds` (array, required): Bank transaction ids, as app.pennylane.com/find_transactions_for_invoice returns them.

## Output

- `transactions` (array, required)

## FAQ

### What does "Read Pennylane bank transactions by id" do?

Reads one or more Pennylane bank transactions by id, as the transaction's detail shows them: date, bank label, amount, account and bank, status, the part still to match, the supplier, and for a card payment the card used and the name of its holder. Use it to know who paid with which company card. Ids come from app.pennylane.com/find_transactions_for_invoice. An id the company does not have comes back with found false. Fails when signed out of Pennylane.

### How do I automatically read Pennylane bank transactions by id on app.pennylane.com?

Ask an AI agent connected to Reduck to run reduck/app.pennylane.com/get_transactions, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.pennylane.com/get_transactions

### Is there a app.pennylane.com API to read Pennylane bank transactions by id?

You do not need one. "Read Pennylane bank transactions by id" drives the real app.pennylane.com pages in a browser, so it works whether or not app.pennylane.com offers an API for this.

### What information do I need to provide?

Required: companyId, transactionIds.

### What does it return?

It returns transactions.

### Do I need to be logged in to app.pennylane.com?

Yes. It acts as you on app.pennylane.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the app.pennylane.com cookies saved by the Reduck extension.

### Does it change anything on app.pennylane.com, or only read data?

It only reads. It looks things up on app.pennylane.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/app.pennylane.com/get_transactions, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.pennylane.com/get_transactions

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/app.pennylane.com/get_transactions
