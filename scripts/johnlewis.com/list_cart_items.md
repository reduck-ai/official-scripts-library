# List John Lewis basket items

Automatically list John Lewis basket items on johnlewis.com. List the items in the John Lewis UK store (johnlewis.com) basket of this browser, as the site holds it: for each line its line id, product id (the sku id of the exact colour or size), offer id (always null), name with the brand, seller (always John Lewis), quantity, unit price and line price, plus the number of items, the basket total before delivery and the currency (GBP). The basket is the guest basket of the browser, so no sign-in is needed. An empty basket returns an empty list and a zero count. Saved-for-later items are not included.

- Site: johnlewis.com
- Address: `reduck/johnlewis.com/list_cart_items`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/johnlewis.com/list_cart_items`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/johnlewis.com/list_cart_items
```

## Input

It takes no input.

## Output

- `count` (integer, required): Number of units in the basket, all lines together.
- `lines` (array, required)
- `total` (number | null, required): Basket subtotal before delivery, in pounds sterling.
- `currency` (string, required): GBP

## FAQ

### What does "List John Lewis basket items" do?

List the items in the John Lewis UK store (johnlewis.com) basket of this browser, as the site holds it: for each line its line id, product id (the sku id of the exact colour or size), offer id (always null), name with the brand, seller (always John Lewis), quantity, unit price and line price, plus the number of items, the basket total before delivery and the currency (GBP). The basket is the guest basket of the browser, so no sign-in is needed. An empty basket returns an empty list and a zero count. Saved-for-later items are not included.

### How do I automatically list John Lewis basket items on johnlewis.com?

Ask an AI agent connected to Reduck to run reduck/johnlewis.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/johnlewis.com/list_cart_items

### Is there a johnlewis.com API to list John Lewis basket items?

You do not need one. "List John Lewis basket items" drives the real johnlewis.com pages in a browser, so it works whether or not johnlewis.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns count, lines, total, currency.

### Do I need to be logged in to johnlewis.com?

No. It only uses pages of johnlewis.com that are reachable without signing in.

### Does it change anything on johnlewis.com, or only read data?

It only reads. It looks things up on johnlewis.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/johnlewis.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/johnlewis.com/list_cart_items

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/johnlewis.com/list_cart_items
