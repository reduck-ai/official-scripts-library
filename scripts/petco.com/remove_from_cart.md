# Remove a product from the Petco cart

Automatically remove a product from the Petco cart on petco.com. Remove one line from the Petco (petco.com, US) cart of this browser and return the cart as the site holds it afterwards. Give the lineId of the line, from List the items in the Petco cart. Removes the line whatever its quantity. Returns removed (true when the line was removed, false when the cart has no such line, and then nothing is changed), the number of units, the subtotal before shipping and tax, and each line left with its line id, offer id, name, seller, quantity, unit price and line price in US dollars. Works as a guest, with no account. Use a managed browser with country US.

- Site: petco.com
- Address: `reduck/petco.com/remove_from_cart`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/petco.com/remove_from_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/petco.com/remove_from_cart
```

## Input

- `lineId` (string, required): Id of the line to remove, from List the items in the Petco cart.

## Output

- `count` (integer, required): Number of units in the cart.
- `lines` (array, required)
- `total` (number | null, required): Subtotal in US dollars, before shipping and tax.
- `removed` (boolean, required): True when lines were removed; false when no line matched.

## FAQ

### What does "Remove a product from the Petco cart" do?

Remove one line from the Petco (petco.com, US) cart of this browser and return the cart as the site holds it afterwards. Give the lineId of the line, from List the items in the Petco cart. Removes the line whatever its quantity. Returns removed (true when the line was removed, false when the cart has no such line, and then nothing is changed), the number of units, the subtotal before shipping and tax, and each line left with its line id, offer id, name, seller, quantity, unit price and line price in US dollars. Works as a guest, with no account. Use a managed browser with country US.

### How do I automatically remove a product from the Petco cart on petco.com?

Ask an AI agent connected to Reduck to run reduck/petco.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/petco.com/remove_from_cart

### Is there a petco.com API to remove a product from the Petco cart?

You do not need one. "Remove a product from the Petco cart" drives the real petco.com pages in a browser, so it works whether or not petco.com offers an API for this.

### What information do I need to provide?

Required: lineId.

### What does it return?

It returns count, lines, total, removed.

### Do I need to be logged in to petco.com?

No. It only uses pages of petco.com that are reachable without signing in.

### Does it change anything on petco.com, or only read data?

It makes changes on petco.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/petco.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/petco.com/remove_from_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/petco.com/remove_from_cart
