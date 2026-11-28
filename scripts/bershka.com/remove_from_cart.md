# Remove Bershka product from cart

Automatically remove Bershka product from cart on bershka.com. Remove one size of a product from the Bershka France (bershka.com/fr) cart of this browser by its offerId, whatever its quantity, and return the cart after the removal (each line, the number of units and the total in euros) with removed true. Give the line id from List Bershka cart items to remove only one line when the size is on several lines. A size that is not in the cart gives removed false and the cart without a change, not an error. Works without sign-in.

- Site: bershka.com
- Address: `reduck/bershka.com/remove_from_cart`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/bershka.com/remove_from_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/bershka.com/remove_from_cart
```

## Input

- `offerId` (string, required): Id of the size to remove (offerId from List Bershka cart items).
- `lineId` (string, optional): Id of one cart line, to remove only that line when the size is on several lines.

## Output

- `count` (integer, required): Number of units in the cart.
- `lines` (array, required)
- `total` (number | null, required): Total of the cart, in euros.
- `removed` (boolean, required): True when a line was removed, false when the size was not in the cart.
- `currency` (string, required): Currency of the amounts, as an ISO code (euro).

## FAQ

### What does "Remove Bershka product from cart" do?

Remove one size of a product from the Bershka France (bershka.com/fr) cart of this browser by its offerId, whatever its quantity, and return the cart after the removal (each line, the number of units and the total in euros) with removed true. Give the line id from List Bershka cart items to remove only one line when the size is on several lines. A size that is not in the cart gives removed false and the cart without a change, not an error. Works without sign-in.

### How do I automatically remove Bershka product from cart on bershka.com?

Ask an AI agent connected to Reduck to run reduck/bershka.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/bershka.com/remove_from_cart

### Is there a bershka.com API to remove Bershka product from cart?

You do not need one. "Remove Bershka product from cart" drives the real bershka.com pages in a browser, so it works whether or not bershka.com offers an API for this.

### What information do I need to provide?

Required: offerId. Optional: lineId.

### What does it return?

It returns count, lines, total, removed, currency.

### Do I need to be logged in to bershka.com?

No. It only uses pages of bershka.com that are reachable without signing in.

### Does it change anything on bershka.com, or only read data?

It makes changes on bershka.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/bershka.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/bershka.com/remove_from_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/bershka.com/remove_from_cart
