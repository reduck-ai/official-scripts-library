# List Wise refunded transactions

Automatically list Wise refunded transactions on wise.com. Scans a Wise account's transaction history over a date range and returns the ones that were refunded, so you can flag charges that were reimbursed.

- Site: wise.com
- Address: `reduck/wise.com/list_refunds`
- Updated: 2026-09-28 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/wise.com/list_refunds`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/wise.com/list_refunds
```

## Input

- `to` (string, optional): Inclusive end date ISO (YYYY-MM-DD).
- `from` (string, optional): Inclusive start date ISO (YYYY-MM-DD). Scrolls back until reached.
- `onlyRefunds` (boolean, optional): If true (default), return only activities flagged as refunded.

## Output

- `count` (integer, required)
- `transactions` (array, required)

## FAQ

### What does "List Wise refunded transactions" do?

Scans a Wise account's transaction history over a date range and returns the ones that were refunded, so you can flag charges that were reimbursed.

### How do I automatically list Wise refunded transactions on wise.com?

Ask an AI agent connected to Reduck to run reduck/wise.com/list_refunds, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/wise.com/list_refunds

### Is there a wise.com API to list Wise refunded transactions?

You do not need one. "List Wise refunded transactions" drives the real wise.com pages in a browser, so it works whether or not wise.com offers an API for this.

### What information do I need to provide?

Optional: to, from, onlyRefunds.

### What does it return?

It returns count, transactions.

### Do I need to be logged in to wise.com?

Yes. It acts as you on wise.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the wise.com cookies saved by the Reduck extension.

### Does it change anything on wise.com, or only read data?

It only reads. It looks things up on wise.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/wise.com/list_refunds, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/wise.com/list_refunds

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/wise.com/list_refunds
