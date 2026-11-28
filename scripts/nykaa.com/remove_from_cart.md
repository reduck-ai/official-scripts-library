# Remove a line from the Nykaa bag

Automatically remove a line from the Nykaa bag on nykaa.com. Remove one line from the bag of this browser in the Nykaa India store (nykaa.com), by its lineId or productId from list_cart_items. It returns removed and the bag after the change (lines, units, grand total in Indian rupees). When the bag has no such line, it changes nothing and returns removed false. It works on the guest bag when nobody is signed in.

- Site: nykaa.com
- Address: `reduck/nykaa.com/remove_from_cart`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/nykaa.com/remove_from_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/nykaa.com/remove_from_cart
```

## Input

- `lineId` (string, optional): lineId of the bag line, from list_cart_items.
- `productId` (string, optional): productId of the bag line, from list_cart_items. Give lineId or productId.

## Output

- `count` (integer, required): Number of units in the bag.
- `lines` (array, required)
- `total` (number | null, required): Grand total of the bag in Indian rupees. Null when the bag is empty.
- `removed` (boolean, required): False when the bag had no such line: nothing changed.
- `currency` (string, required): INR

## FAQ

### What does "Remove a line from the Nykaa bag" do?

Remove one line from the bag of this browser in the Nykaa India store (nykaa.com), by its lineId or productId from list_cart_items. It returns removed and the bag after the change (lines, units, grand total in Indian rupees). When the bag has no such line, it changes nothing and returns removed false. It works on the guest bag when nobody is signed in.

### How do I automatically remove a line from the Nykaa bag on nykaa.com?

Ask an AI agent connected to Reduck to run reduck/nykaa.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/nykaa.com/remove_from_cart

### Is there a nykaa.com API to remove a line from the Nykaa bag?

You do not need one. "Remove a line from the Nykaa bag" drives the real nykaa.com pages in a browser, so it works whether or not nykaa.com offers an API for this.

### What information do I need to provide?

Optional: lineId, productId.

### What does it return?

It returns count, lines, total, removed, currency.

### Do I need to be logged in to nykaa.com?

No. It only uses pages of nykaa.com that are reachable without signing in.

### Does it change anything on nykaa.com, or only read data?

It makes changes on nykaa.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/nykaa.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/nykaa.com/remove_from_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/nykaa.com/remove_from_cart
