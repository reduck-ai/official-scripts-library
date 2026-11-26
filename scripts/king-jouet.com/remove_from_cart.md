# Remove from King Jouet cart

Automatically remove from King Jouet cart on king-jouet.com. Remove a product from the King Jouet cart of this browser, whatever its quantity, by its reference or product page link, and return the cart left: each line with its reference, name, quantity, unit price and line price, plus the item count and total in euros. A product that is not in the cart returns removed false and changes nothing. Works as a guest: the cart lives in the browser.

- Site: king-jouet.com
- Address: `reduck/king-jouet.com/remove_from_cart`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/king-jouet.com/remove_from_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/king-jouet.com/remove_from_cart
```

## Input

- `product` (string, required): King Jouet product reference (ref in List King Jouet cart items, for example 1004781) or its product page link (.../ref-1004781-....htm).

## Output

- `count` (integer, required): Units left in the cart.
- `lines` (array, required)
- `total` (number | null, required): Cart total in euros, taxes included.
- `removed` (boolean, required)

## FAQ

### What does "Remove from King Jouet cart" do?

Remove a product from the King Jouet cart of this browser, whatever its quantity, by its reference or product page link, and return the cart left: each line with its reference, name, quantity, unit price and line price, plus the item count and total in euros. A product that is not in the cart returns removed false and changes nothing. Works as a guest: the cart lives in the browser.

### How do I automatically remove from King Jouet cart on king-jouet.com?

Ask an AI agent connected to Reduck to run reduck/king-jouet.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/king-jouet.com/remove_from_cart

### Is there a king-jouet.com API to remove from King Jouet cart?

You do not need one. "Remove from King Jouet cart" drives the real king-jouet.com pages in a browser, so it works whether or not king-jouet.com offers an API for this.

### What information do I need to provide?

Required: product.

### What does it return?

It returns count, lines, total, removed.

### Do I need to be logged in to king-jouet.com?

No. It only uses pages of king-jouet.com that are reachable without signing in.

### Does it change anything on king-jouet.com, or only read data?

It makes changes on king-jouet.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/king-jouet.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/king-jouet.com/remove_from_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/king-jouet.com/remove_from_cart
