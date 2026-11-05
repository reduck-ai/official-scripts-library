# List King Jouet cart items

Automatically list King Jouet cart items on king-jouet.com. List the items in the King Jouet cart of this browser, as the site holds it: for each line the product reference, name, quantity, unit price and line price, plus the number of items and the cart total in euros. The cart is the guest cart of the browser, so no sign-in is needed. An empty cart returns an empty list and a zero total.

- Site: king-jouet.com
- Address: `reduck/king-jouet.com/list_cart_items`
- Updated: 2026-11-04 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/king-jouet.com/list_cart_items`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/king-jouet.com/list_cart_items
```

## Input

It takes no input.

## Output

- `count` (integer, required): Units in the cart.
- `lines` (array, required)
- `total` (number | null, required): Cart total in euros, taxes included.

## FAQ

### What does "List King Jouet cart items" do?

List the items in the King Jouet cart of this browser, as the site holds it: for each line the product reference, name, quantity, unit price and line price, plus the number of items and the cart total in euros. The cart is the guest cart of the browser, so no sign-in is needed. An empty cart returns an empty list and a zero total.

### How do I automatically list King Jouet cart items on king-jouet.com?

Ask an AI agent connected to Reduck to run reduck/king-jouet.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/king-jouet.com/list_cart_items

### Is there a king-jouet.com API to list King Jouet cart items?

You do not need one. "List King Jouet cart items" drives the real king-jouet.com pages in a browser, so it works whether or not king-jouet.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns count, lines, total.

### Do I need to be logged in to king-jouet.com?

No. It only uses pages of king-jouet.com that are reachable without signing in.

### Does it change anything on king-jouet.com, or only read data?

It only reads. It looks things up on king-jouet.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/king-jouet.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/king-jouet.com/list_cart_items

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/king-jouet.com/list_cart_items
