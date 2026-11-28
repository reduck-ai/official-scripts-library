# Remove a product from the Hot Topic cart

Automatically remove a product from the Hot Topic cart on hottopic.com. Remove lines from the Hot Topic (hottopic.com, US) shopping bag of this browser and return the bag as the site holds it afterwards. Give lineId to remove one line, or offerId to remove every line of that size or color, whatever its quantity. Both come from List the items in the Hot Topic cart. Returns removed (true when lines were removed, false when no line matched, and then nothing is changed), the number of units, the estimated subtotal before shipping and tax, and each line left with its line id, product id, offer id, name, seller, quantity, unit price and line price in US dollars. Works as a guest, with no account.

- Site: hottopic.com
- Address: `reduck/hottopic.com/remove_from_cart`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/hottopic.com/remove_from_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/hottopic.com/remove_from_cart
```

## Input

- `lineId` (string, optional): Id of the line to remove, from List the items in the Hot Topic cart.
- `offerId` (string, optional): Id of the size or color whose lines to remove, from List the items in the Hot Topic cart.

## Output

- `count` (integer, required): Number of units in the bag.
- `lines` (array, required)
- `total` (number | null, required): Estimated subtotal in US dollars, before shipping and tax.
- `removed` (boolean, required): True when lines were removed; false when no line matched.

## FAQ

### What does "Remove a product from the Hot Topic cart" do?

Remove lines from the Hot Topic (hottopic.com, US) shopping bag of this browser and return the bag as the site holds it afterwards. Give lineId to remove one line, or offerId to remove every line of that size or color, whatever its quantity. Both come from List the items in the Hot Topic cart. Returns removed (true when lines were removed, false when no line matched, and then nothing is changed), the number of units, the estimated subtotal before shipping and tax, and each line left with its line id, product id, offer id, name, seller, quantity, unit price and line price in US dollars. Works as a guest, with no account.

### How do I automatically remove a product from the Hot Topic cart on hottopic.com?

Ask an AI agent connected to Reduck to run reduck/hottopic.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/hottopic.com/remove_from_cart

### Is there a hottopic.com API to remove a product from the Hot Topic cart?

You do not need one. "Remove a product from the Hot Topic cart" drives the real hottopic.com pages in a browser, so it works whether or not hottopic.com offers an API for this.

### What information do I need to provide?

Optional: lineId, offerId.

### What does it return?

It returns count, lines, total, removed.

### Do I need to be logged in to hottopic.com?

No. It only uses pages of hottopic.com that are reachable without signing in.

### Does it change anything on hottopic.com, or only read data?

It makes changes on hottopic.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/hottopic.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/hottopic.com/remove_from_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/hottopic.com/remove_from_cart
